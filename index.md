---
layout: col-sidebar
title: OWASP secureCodeBox
tags: scanner
level: 0
type: tool
---

![logo](/assets/images/logo.png "Logo secureCodeBox") 

The OWASP secureCodeBox Project is a **docker based, modularized toolchain** for _continuous security scans of your software project_. Its goal is to _orchestrate_ and easily _automate_ a bunch of _security-testing tools_ out of the box. With the secureCodeBox we provide a toolchain for continuous scanning of applications to find the low-hanging fruit issues early in the development process and free the resources of the penetration tester to concentrate on the major security issues.

![laptop with dashboard](/assets/images/laptop_with_dashboard.png "Example dashboard") 

## Description

The purpose of secureCodeBox is not to replace the penetration testers or make them obsolete. We strongly recommend to run extensive tests by experienced penetration testers on all your applications. For more informations about this project please have look at our [GitHub Repo](https://github.com/secureCodeBox/secureCodeBox)
    
Our main goal is to implement a major security testing platform and framework which enables developers and teams to integrate a bunch of security testing tools in their CI/CD environment as easy as possible. The flexibility and scalability of the platform architecture leads to features like _multi tenancy support_, _large scale (multi-) project testing_, support of distributed and private networks, customisable security test flows,... which enables projects to test complex environments without implementing the complete security testing infrastructure on their own.

Secondly we try to foster a broad range of security tools to be easily integrated. Also we will try to integrate existing OWASP Projects as building blocks in our platform.

## Roadmap 

As of **Mai, 2019, the highest priorities for the next 6 months** are:

- Finalize the integration with the OWASP DefectDojo Project, as a building block for security finding analytics
- Enhance the multi tenant support
- Migrate the deployment setup to Kubernetes, based on terraform for provisioning
- Implement a UI for the Project based on the existing secureCodeBox API
- Integrate a new REST API security scanner

**Future milestones in general are**:

- Adapt a serverless infrastructure architecture for the security scanner microservices
- Migrate the process engine (Camunda) to a more lightweight technology (Zeebe.io maybe)

## Licensing

This Project is free software: you can redistribute it and/or modify it under the terms of the [Apache License 2.0](https://github.com/secureCodeBox/secureCodeBox/blob/master/LICENSE). OWASP secureCodeBox Project and any contributions are Copyright © by {the Project Leader(s) or OWASP} {Year(s)}.
