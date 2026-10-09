---
title: "Use the Setup Wizard to install Configuration Manager sites"
description: Use the Configuration Manager setup wizard to install a new site.
ms.date: "2024-12-16T00:00:00Z"
ms.subservice: core-infra
ms.topic: overview
ms.collection: tier3
ms.service: configuration-manager
author: sccmavenger
cmProducts:
- https://authoring-docs-microsoft.poolparty.biz/devrel/1e69816a-aaaa-474e-a36f-3ec7790fadc3
- https://authoring-docs-microsoft.poolparty.biz/devrel/a3955c7b-f5ee-420d-aff5-d7119738f38b
manager: laurawi
moniker_range_name: ''
ms.author: dannygu
ms.reviewer:
- brianhun
- hugowu
- payur
- qiani
- umaikhan
spProducts:
- https://authoring-docs-microsoft.poolparty.biz/devrel/ae012320-d2b3-47d8-abdc-898a64d069a9
- https://authoring-docs-microsoft.poolparty.biz/devrel/b31948f4-2f38-404b-ac93-c3c8c5b3ae33
---

# Use the Setup Wizard to install Configuration Manager sites

*Applies to: Configuration Manager (current branch)*

To install a new Configuration Manager site by using a guided user interface, use the Configuration Manager Setup Wizard (setup.exe). The wizard supports installing a primary site or central administration site (CAS). You also use the wizard to [upgrade an evaluation installation](upgrade-an-evaluation-install-to-a-full-install.md) of Configuration Manager to a fully licensed installation. When you don't want to use the wizard, you can instead use an [installation script](use-a-command-line-to-install-sites.md) and run an unattended command-line installation.

Install a secondary site from within the Configuration Manager console. Secondary sites don't support a scripted command-line installation.

Before you install a site, be familiar with the details in the following articles:

- [Design a hierarchy of sites](../../../plan-design/hierarchy/design-a-hierarchy-of-sites.md)
- [Site and site system prerequisites](../../../plan-design/configs/site-and-site-system-prerequisites.md)
- [Prepare to install sites](prepare-to-install-sites.md)
- [Prerequisites for installing sites](prerequisites-for-installing-sites.md)
- Assess server readiness with the [Prerequisite Checker](prerequisite-checker.md)
- [Release notes](release-notes.md)

> [!TIP]
>
> If you need assistance with site installation, see the [Support options and community resources](../../../understand/find-help.md#support-options-and-community-resources). For example, the Microsoft Q&amp;A forum for [Configuration Manager site and client deployment](https://learn.microsoft.com/en-us/answers/topics/mem-cm-site-deployment.html).

When you're ready to get started, see the following articles for the specific processes:

[Use the setup wizard to install a central administration or primary site](setup-wizard-central-primary.md)

[Use the setup wizard to install a secondary site](setup-wizard-secondary.md)
