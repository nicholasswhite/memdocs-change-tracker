---
description: Learn how to use the OS Deployment Driver Supported Platforms Schema to check which operating systems are compatible.
title: "Operating System Deployment Driver Supported Platforms Schema"
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
---

# Operating System Deployment Driver Supported Platforms Schema

The following reference section documents the XML schema that is used to specify the platforms that are supported by an operating system deployment driver in Microsoft Configuration Manager.

The schema is used in the `SMS_Driver` class `SDMPackageXML` property.

> [!CAUTION]
>
> The supported platforms portion of `SDMPackageXML` is the only part of the Driver XML schema that can be edited. You should not make changes to other parts of the XML.

## Supported Platform XML

&lt;[PlatformApplicabilityConditions](platformapplicabilityconditions.md)&gt;

&lt;[PlatformApplicabilityCondition](platformapplicabilitycondition.md)&gt;

&lt;[Query1](query1.md)&gt;&lt;/Query1&gt;

&lt;[Query2](query2.md)&gt;&lt;/Query2&gt;

&lt;/PlatformApplicabilityCondition&gt;

&lt;/PlatformApplicabilityConditions&gt;

## See Also

[Operating System Deployment Driver Supported Platforms Schema](operating-system-deployment-driver-supported-platforms-schema.md) [PlatformApplicabilityCondition](platformapplicabilitycondition.md) [Query1](query1.md) [Query2](query2.md)
