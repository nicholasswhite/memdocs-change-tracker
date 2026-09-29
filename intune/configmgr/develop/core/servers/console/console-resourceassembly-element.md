---
description: Learn how to define the resources that are used by the node with the ResourceAssembly element in Configuration Manager.
title: "Configuration Manager Console ResourceAssembly Element"
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: article
ms.collection: tier3
ms.service: configuration-manager
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
