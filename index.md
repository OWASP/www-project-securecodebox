---
layout: col-sidebar
title: OWASP secureCodeBox
tags: scanner
level: 2
type: tool
region: Unknown
pitch: Automate all your security and vulnerability scanners.
---

![logo](assets/images/logo.png "Logo secureCodeBox")

The OWASP secureCodeBox Project is a **kubernetes based, modularized toolchain** for _continuous security scans of your software project_. Its goal is to _orchestrate_ and easily _automate_ a bunch of _security-testing tools_ out of the box. With the secureCodeBox we provide a toolchain for continuous scanning of applications to find the low-hanging fruit issues early in the development process and free the resources of the penetration tester to concentrate on the major security issues.

![laptop with dashboard](assets/images/laptop_with_dashboard.png "Example dashboard")

## Description

The purpose of secureCodeBox is not to replace the penetration testers or make them obsolete. We strongly recommend to run extensive tests by experienced penetration testers on all your applications. For more informations about this project please have look at our [GitHub Repo secureCodeBox V1][scb-github] or our new Major Release [GitHub Repo secureCodeBox V2][scbv2-github]

Our main goal is to implement a major security testing platform and framework which enables developers and teams to integrate a bunch of security testing tools in their CI/CD environment or kubernetes environment as easy as possible. The flexibility and scalability of the platform architecture leads to features like _multi tenancy support_, _large scale (multi-) project testing_, support of distributed and private networks, customisable security test flows,... which enables projects to test complex environments without implementing the complete security testing infrastructure on their own.

Secondly we try to foster a broad range of security tools to be easily integrated. Also we will try to integrate existing OWASP Projects as building blocks in our platform.

## Roadmap

### New Major Release V2
Currently we are working heavily on a new major release with an complete new architecture of the secureCodeBox Project which is based on kubernetes. The major release of SCB version 2.0 will be available in the next weeks. The release will contain a major architecture change which will not be backward compatible. More details will follow soon in a series of blog articles.

The new architecture is based on Kubernetes CRDs and follows an function as a service (FaaS) principle. Therefore we impleted an Kubernetes operator which schedules scan jobs as kubernetes jobs. This architecture leeds to a much more ressource efficiency. Instead of long running microservice (SCB v1 Architecture) scans only consume cluster ressource for a short amount of time.  

![SCBv2 Architecture Overview](assets/images/scbv2-architecture.svg "SCBv2 Architecture Overview")

As of **August, 2020, the highest priorities for the next 6 months** are:

- Finalize the Major Release V2 and switch the complete project to a kubernetes based FaaS architecture
- Finalize the integration with the OWASP DefectDojo Project, as a building block for security finding analytics
- Implement a permanend UI to visualize the security scan findings as an alternative to DefectDojo and Kibana (ELK Stack)
- Finalize an kubernetes based *autodiscovery* for all ressource currently running in an kubernetes cluster

## Quickstart secureCodebox V2

### Deployment (based on Helm)
Deploy the secureCodeBox operator first:

```bash
helm repo add securecodebox https://charts.securecodebox.io
kubectl create namespace securecodebox-system
helm -n securecodebox-system upgrade --install securecodebox-operator securecodebox/operator --devel
```

Optionally deploy SCB scanner charts for each security scanner you want to use. They should not be installed into the `securecodebox-system` like the operator so that different teams can use different kinds of scanners.
To get more informations about each scanner and hook please have a look at our [Website][scb-website-integrations] or the corresponding [GitHub Repo secureCodeBox V2][scbv2-github].

```bash
helm upgrade --install amass securecodebox/amass --devel
helm upgrade --install kube-hunter securecodebox/kube-hunter --devel
helm upgrade --install nikto securecodebox/nikto --devel
helm upgrade --install nmap securecodebox/nmap --devel
helm upgrade --install ssh-scan securecodebox/ssh-scan --devel
helm upgrade --install sslyze securecodebox/sslyze --devel
helm upgrade --install trivy securecodebox/trivy --devel
helm upgrade --install zap securecodebox/zap --devel
helm upgrade --install wpscan securecodebox/wpscan --devel
```

Optional deploy some demo apps for scanning:

```bash
helm upgrade --install dummy-ssh securecodebox/dummy-ssh --devel
helm upgrade --install bodgeit securecodebox/bodgeit --devel
helm upgrade --install juice-shop securecodebox/juice-shop --devel
helm upgrade --install old-wordpress securecodebox/old-wordpress --devel
helm upgrade --install swagger-petstore securecodebox/swagger-petstore --devel
```

Deploy secureCodeBox Hooks:

```bash
helm upgrade --install ufh securecodebox/update-field-hook --devel
helm upgrade --install gwh securecodebox/generic-webhook --devel
helm upgrade --install dssh securecodebox/declarative-subsequent-scans --devel
```

Persistence provider Elasticsearch:

```bash
helm upgrade --install elkh securecodebox/persistence-elastic --devel
```

## Community

You are welcome, please join us on... 👋

- [GitHub][scb-github]
- [Slack][scb-slack]
- [Twitter][scb-twitter]

## Licensing

This Project is free software: you can redistribute it and/or modify it under the terms of the [Apache License 2.0](https://github.com/secureCodeBox/secureCodeBox/blob/master/LICENSE). OWASP secureCodeBox Project and any contributions are Copyright © by [iteratec GmbH](https://www.iteratec.com) 2015-2020.

[scb-website]: https://www.securecodebox.io/
[scb-website-integrations]: https://www.securecodebox.io/integrations
[scb-github]: https://github.com/secureCodeBox/secureCodeBox
[scbv2-github]: https://github.com/secureCodeBox/secureCodeBox-v2
[scb-twitter]: https://twitter.com/secureCodeBox
[scb-slack]: https://join.slack.com/t/securecodebox/shared_invite/enQtNDU3MTUyOTM0NTMwLTJiNzg3MmU2ZDY2NDFiMGI0Y2FkM2I5Mzc2ZmEzYTcyN2FlN2Y2NDFiZDE5NjAxMjg1M2IxNDViNzE3OTIxMGU
[scb-license]: https://github.com/secureCodeBox/secureCodeBox/blob/master/LICENSE


