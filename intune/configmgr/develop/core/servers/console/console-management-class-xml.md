---
title: "Configuration Manager Console Management Class XML"
description: The MyClass node is a subclass of the SMS_SiteControlItem management class, which is defined in ManagementClassDescriptions.xml.
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: how-to
ms.collection: tier3
ms.service: configuration-manager
author: sccmavenger
cmProducts:
- https://authoring-docs-microsoft.poolparty.biz/devrel/c7ddd0ba-08b8-4055-8ab8-0da61f3dfbb3
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/4c50f262-d533-4ba4-9d4a-08899ec3a3d1
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/a72e95ff-4b4f-4cc1-90c6-7dcba67ff05f
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
- https://authoring-docs-microsoft.poolparty.biz/devrel/5cf7e60a-ca26-4c6f-befd-5e90eae977f5
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/24dc3ccd-591a-4415-a1fe-8759afafcb12
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/6a8c83be-f1de-4e90-bde0-bd097999a60c
---

# Configuration Manager Console Management Class XML

The management classes XML for the Configuration Manager console are located %*ProgramFiles*%\Microsoft Endpoint Manager\AdminConsole\XmlStorage\ConsoleRoot\ManagementClassDescriptions.xml file. Your extension management class XML files, however, must be placed in the AdminConsole\XmlStorage\Extensions\ManagementClasses\ folder.

The following XML defines an extension management class called "MyClass". The "MyClass" node is a subclass of the `SMS_SiteControlItem` management class, which is defined in the ConsoleRoot\ManagementClassDescriptions.xml.

```

<ManagementClassDescription Name="MyClass" SuperclassName="SMS_SiteControlItem" SecurityObjectAlias="SMS_Site"> <Properties>          <ManagementClassPropertyDescription Name="RoleName"/>          <ManagementClassPropertyDescription Name="SiteCode" />     </Properties></ManagementClassDescription>
```

You can also expose your own custom management class that is defined within an assembly. For example, the XML below defines a management class called `_SDK`. The `_SDK` class is defined in a custom assembly. Note that the management class must be defined using .NET from within the referenced assembly.

```
<ManagementClassDescription Name="_SDK">       <Properties>          <ManagementClassPropertyDescription Name="MyProperty1"/>         <ManagementClassPropertyDescription Name="MyProperty2"/>           <ManagementClassPropertyDescription Name="MyProperty3"/>      </Properties>       <ResourceAssembly>         <Assembly>UIExtensionsDemo.dll</Assembly>    <Type>UIExtensionsDemo.ConnectionManager._SDK.resources</Type>       </ResourceAssembly>       <ImagesDescription>          <ResourceAssembly>             <Assembly>UIExtensionsDemo.dll</Assembly>        <Type>UIExtensionsDemo.Resources.resources</Type>   </ResourceAssembly>         <ImageResourceName>ViewIcon</ImageResourceName>      </ImagesDescription></ManagementClassDescription>
```

## See also

[About console management classes](about-configuration-manager-console-management-classes.md)
