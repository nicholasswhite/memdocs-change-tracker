---
title: "Configuration Manager SQL View Security"
description: Facilitate instance (or row) level security on core object classes. Using the Configuration Manager schema views, an application or user is operating outside of this security mechanism.
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: article
ms.collection: tier3
ms.service: configuration-manager
author: sccmavenger
cmProducts:
- https://authoring-docs-microsoft.poolparty.biz/devrel/cbe4ca68-43ac-4375-aba5-5945a6394c20
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
- https://authoring-docs-microsoft.poolparty.biz/devrel/ced846cc-6a3c-4c8f-9dfb-3de0e90e2742
---

# Configuration Manager SQL View Security

The Configuration Manager object security mechanism, implemented in the SMS Provider, facilitates instance (or row) level security on core object classes. By using the Configuration Manager schema views, an application or user is operating outside of this security mechanism. This doesn't mean that the views can't be secured from unauthorized data access; however, security must be configured separately and is less precise than standard Configuration Manager object security. You can give a user read-only permission to access only the views and deny access to any internal Configuration Manager tables. The main security functionality that is lost in the view approach is the ability to secure specific object instances (such as packages and collections) separately for members of groups.

## See Also

[Configuration Manager Schema View Mapping](configuration-manager-schema-view-mapping.md) [Configuration Manager Schema SQL Views](configuration-manager-schema-sql-views.md)
