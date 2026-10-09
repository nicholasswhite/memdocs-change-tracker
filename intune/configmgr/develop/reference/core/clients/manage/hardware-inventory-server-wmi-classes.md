---
title: Hardware inventory server WMI classes
description: The Configuration Manager hardware inventory server WMI classes are generated dynamically and the name for a class is transformed from Win32_hardware to SMS_G_System_hardware.
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
author: sccmavenger
cmProducts:
- https://authoring-docs-microsoft.poolparty.biz/devrel/caec7b7f-4941-4578-b79f-c63b1c1f5af4
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
- https://authoring-docs-microsoft.poolparty.biz/devrel/754dea88-f800-4835-b6b5-280cb5d81e88
---

# Hardware inventory server WMI classes

The Configuration Manager hardware inventory server WMI classes are generated dynamically.

During the Configuration Manager hardware inventory process, the name for a class is transformed from "Win32_hardware" to "SMS_G_System_hardware". For example, "Win32_DiskDrive" translates to "SMS_G_System_DISK".

In addition to the class name change, the following differences are found between the Win32 classes and the Configuration Manager hardware inventory server classes:

- Each Configuration Manager class inherits four properties from [SMS_G_System_Current Server WMI Class](sms_g_system_current-server-wmi-class.md).
- The Configuration Manager hardware inventory classes don't support the Win32 class methods.
- Many of the Configuration Manager hardware inventory classes contain a subset of the Win32 class properties.
