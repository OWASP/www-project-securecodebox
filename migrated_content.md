---
layout: col-sidebar
title: OWASP securecCodebBox
tags: example-tag
level: 0
type: tool
---

![OWASP_Project_Header.jpg](OWASP_Project_Header.jpg "OWASP_Project_Header.jpg")

<img src="Logo_secureCodeBox.png" title="fig:Logo_secureCodeBox.png" alt="Logo_secureCodeBox.png" /> The OWASP secureCodeBox Project is a **docker based, modularized toolchain** for _continuous security scans of your software project_. Its goal is to _orchestrate_ and easily _automate_ a bunch of _security-testing tools_ out of the box. With the secureCodeBox we provide a toolchain for continuous scanning of applications to find the low-hanging fruit issues early in the development process and free the resources of the penetration tester to concentrate on the major security issues.

## Description

The purpose of secureCodeBox is not to replace the penetration testers or make them obsolete. We strongly recommend to run extensive tests by experienced penetration testers on all your applications. For more informations about this project please have look at our <a href="https://github.com/secureCodeBox/secureCodeBox">GitHub Repo</a>
    
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

## Getting Involved

Contributions are welcome and extremely helpful 🙌

You are welcome, please join us on... 👋

- <a href="https://github.com/secureCodeBox/">GitHub</a>
- <a href="https://join.slack.com/t/securecodebox/shared_invite/enQtNDU3MTUyOTM0NTMwLTJiNzg3MmU2ZDY2NDFiMGI0Y2FkM2I5Mzc2ZmEzYTcyN2FlN2Y2NDFiZDE5NjAxMjg1M2IxNDViNzE3OTIxMGU">Slack</a>
- <a href="https://twitter.com/secureCodeBox">Twitter</a>

## Licensing

This Project is free software: you can redistribute it and/or modify it under the terms of the <a href="https://github.com/secureCodeBox/secureCodeBox/blob/master/LICENSE">Apache License 2.0</a>. OWASP secureCodeBox Project and any contributions are Copyright © by {the Project Leader(s) or OWASP} {Year(s)}.

## Project About

<span style="color:#ff0000"> Template:Project_About
    
project_name=OWASP secureCodeBox

<a href="https://github.com/secureCodeBox">GitHub Project</a>

<a href="https://securecodebox.github.io/secureCodeBox/">Documentation</a>

<a href="https://github.com/secureCodeBox/secureCodeBox/issues">Issue Tracker</a>

<a href="https://www.secureCodeBox.io">Website</a>

<a href="https://join.slack.com/t/securecodebox/shared_invite/enQtNDU3MTUyOTM0NTMwLTJiNzg3MmU2ZDY2NDFiMGI0Y2FkM2I5Mzc2ZmEzYTcyN2FlN2Y2NDFiZDE5NjAxMjg1M2IxNDViNzE3OTIxMGU">Slack</a>

<a href="https://twitter.com/secureCodeBox">Twitter</a>

## Project Leader

Leader:

- <a href="User:Rseedorff" title="wikilink">Robert Seedorff</a>

Maintainer:

- <a href="User:J12934" title="wikilink">Jannik Hollenbach</a>

Contributer:

- <a href="User:Timo_Pagel" title="wikilink">Timo Pagel</a>
- <a href="User:Benjamin_Pfänder" title="wikilink">Benjamin Pfänder</a>

## Integrated Projects

- <a href="OWASP_Juice_Shop_Project" title="wikilink">OWASP JuiceShop Project</a>
- <a href="OWASP_Zed_Attack_Proxy_Project" title="wikilink">OWASP Zed Attack Proxy Project</a>
- <a href="OWASP_DefectDojo_Project" title="wikilink">OWASP DefectDojo Project</a>

## Related Projects

- <a href="OWASP_DevSlop_Project" title="wikilink">OWASP DevSlop Project</a>
- <a href="OWASP_Glue_Tool_Project" title="wikilink">OWASP Glue Tool Project</a>

__NOTOC__ <headertabs />

[Category:OWASP Project](Category:OWASP_Project "wikilink")
[Category:OWASP_Builders](Category:OWASP_Builders "wikilink")
[Category:OWASP_Defenders](Category:OWASP_Defenders "wikilink")
[Category:OWASP_Tool](Category:OWASP_Tool "wikilink")
