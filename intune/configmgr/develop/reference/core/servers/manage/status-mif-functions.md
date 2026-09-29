---
title: Status MIF Functions
description: In Configuration Manager, status MIF functions are provided in separate libraries to create a status Management Information Format file.
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
---

# Status MIF Functions

In Configuration Manager, status MIF functions are provided in separate libraries to create a status Management Information Format (MIF) file. For more information about how the install status MIF file is used by Configuration Manager, see [SMS_Package Server WMI Class](../configure/sms_package-server-wmi-class.md).

Success or failure of an advertisement is determined by using either an install status MIF file or the exit code of the advertised program. Relying on the exit code limits the visibility of events during the installation process and requires interpretation of the various exit codes. However, using the install status MIF file provides an enhanced status indicating whether the installation succeeded or failed, and it includes an appropriate description.

## Status MIF Functions

- [Create Function](create-function.md)
- [InstallStatusMIF Function](installstatusmif-function.md)
- [InstallStatusMIFEx Function](installstatusmifex-function.md)
