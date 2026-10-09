---
title: Troubleshoot BitLocker
description: Learn how to troubleshoot problems with BitLocker management in Configuration Manager
ms.date: "2019-11-29T00:00:00Z"
ms.subservice: protect
ms.topic: troubleshooting
ms.collection: tier3
ms.service: configuration-manager
author: sccmavenger
cmProducts:
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/43ab1a66-ffe1-45dd-a4cb-6580218ef802
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
- https://authoring-docs-microsoft.poolparty.biz/devrel/bbc4fbf6-70c4-4d12-b47f-9360080c4977
---

# Troubleshoot BitLocker

*Applies to: Configuration Manager (current branch)*

Use the information in this article to help you troubleshoot issues with BitLocker management in Configuration Manager.

## Server error in self-service

When trying to open the self-service portal (`https://webserver.contoso.com/SelfService`) for the first time, you see the following error message:

```error
Configuration Error - Server Error in '/SelfService' Application

Description: An error occurred during the processing of a configuration file required to service this request. Please review the specific error details below and modify your configuration file appropriately.

Parser Error Message: Could not load file or assembly 'System.Web.Mvc, Version=4.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35' or one of its dependencies. The system cannot find the file specified.
```

To fix this issue, make sure you installed the [prerequisite](../../plan-design/bitlocker-management.md#prerequisites) for **Microsoft ASP.NET MVC 4.0** on the web server.

## See also

For more information about using BitLocker event logs, see [BitLocker event logs](about-event-logs.md).

For a list of known errors and possible causes for event log entries, see the following articles:

- [Client event logs](client-event-logs.md)
- [Server event logs](server-event-logs.md)

To understand why clients are reporting not compliant with the BitLocker management policy, see [Non-compliance codes](non-compliance-codes.md).
