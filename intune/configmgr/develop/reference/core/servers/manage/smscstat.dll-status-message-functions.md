---
title: Smscstat.dll Status Message Functions
description: In Configuration Manager, the functions defined by the Smscstat.dll dynamic-link library, report status messages that can be called by using a C interface.
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
author: sccmavenger
cmProducts:
- https://authoring-docs-microsoft.poolparty.biz/devrel/540ac133-a371-4dbb-8f94-28d6cc77a70b
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
- https://authoring-docs-microsoft.poolparty.biz/devrel/60bfc045-f127-4841-9d00-ea35495a5800
---

# Smscstat.dll Status Message Functions

In Configuration Manager, the functions that are defined by the Smscstat.dll dynamic-link library, report status messages that can be called by using a C interface.

## Functions

Smscstat.dll exports the following functions.

| Term | Description |
| --- | --- |
| [AddAttributeToSMSStatusMessage Function](addattributetosmsstatusmessage-function.md) | Adds a single optional status message attribute ID/value pair to a status message object. |
| [CreateSMSStatusMessage Function](createsmsstatusmessage-function.md) | Creates a status message object. |
| [ReportSMSStatusMessage Function](reportsmsstatusmessage-function.md) | Submits a status message object to the Configuration Manager status system. |
