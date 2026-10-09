---
description: Learn how to use Windows Management Instrumentation (WMI) classes that represent the objects in SMS as templates for managed objects.
title: Configuration Manager Class Schema
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: article
ms.collection: tier3
ms.service: configuration-manager
author: sccmavenger
cmProducts:
- https://authoring-docs-microsoft.poolparty.biz/devrel/bcbcbad5-4208-4783-8035-8481272c98b8
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
- https://authoring-docs-microsoft.poolparty.biz/devrel/43b2e5aa-8a6d-4de2-a252-692232e5edc8
---

# Configuration Manager Class Schema

The Systems Management Server (SMS) class schema is a set of Windows Management Instrumentation (WMI) classes that represent the objects in SMS. Each SMS class is a template for a managed object and all instances of the object use the template. Classes can contain properties and methods: the properties describe the class data and the methods typically perform data management for the class.

## Class categories

The following table describes the categories of classes and how the classes are used.

| Category | Description |
| --- | --- |
| Server | Classes supported on servers running SMS. |
| Advanced Client | Classes supported on SMS Advanced Clients. |

## See also

- [Date and Time Formats](date-and-time-formats.md)
- [Interpreting Bitfield Properties](interpreting-bitfield-properties.md)
- [Lazy Properties](lazy-properties.md)
- [SMS Provider Field Length Restrictions](sms-provider-field-length-restrictions.md)
