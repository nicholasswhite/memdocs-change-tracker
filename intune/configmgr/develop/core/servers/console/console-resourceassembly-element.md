---
description: Learn how to define the resources that are used by the node with the ResourceAssembly element in Configuration Manager.
title: "Configuration Manager Console ResourceAssembly Element"
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: article
ms.collection: tier3
ms.service: configuration-manager
author: sccmavenger
manager: laurawi
moniker_range_name: ''
ms.author: dannygu
ms.reviewer:
- brianhun
- hugowu
- payur
- qiani
- umaikhan
cmProducts:
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/4c50f262-d533-4ba4-9d4a-08899ec3a3d1
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/a72e95ff-4b4f-4cc1-90c6-7dcba67ff05f
spProducts:
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/24dc3ccd-591a-4415-a1fe-8759afafcb12
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/6a8c83be-f1de-4e90-bde0-bd097999a60c
---

# Configuration Manager Console ResourceAssembly Element

In Configuration Manager, the `ResourceAssembly` element defines the resources that are used by the node. The following XML defines the assembly, `AdminUI.CollectionProperty.dll`, and the type of the resource within the assembly.

```
<ResourceAssembly>
    <Assembly>AdminUI.CollectionProperty.dll</Assembly>
    <Type>Microsoft.ConfigurationManagement.AdminConsole.CollectionProperty.Properties.Resources.resources</Type>
</ResourceAssembly>

```

## See Also

[About Configuration Manager Administrator Console Nodes](about-configuration-manager-console-nodes.md) [How to Find a Configuration Manager Node GUID](how-to-find-a-configuration-manager-console-node-guid.md) [Configuration Manager Console Node XML](console-node-xml.md)
