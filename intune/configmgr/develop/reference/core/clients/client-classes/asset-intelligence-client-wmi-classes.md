---
title: Asset Intelligence Client WMI Classes
description: Learn about the Asset Intelligence client Windows Management Instrumentation classes that query client computers for usage, software, and licensing data.
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
---

# Asset Intelligence Client WMI Classes

In Configuration Manager, the Asset Intelligence client Windows Management Instrumentation (WMI) classes query client computers for usage, software, and licensing data. These classes are in the root/cimv2/sms namespace.

## In This Section

| Term | Definition |
| --- | --- |
| [SMS_AutoStartSoftware Client WMI Class](sms_autostartsoftware-client-wmi-class.md) | Enumerates software that starts automatically with, or immediately after, the operating system. |
| [SMS_BrowserHelperObject Client WMI Class](sms_browserhelperobject-client-wmi-class.md) | Enumerates all browser helper objects on a computer. |
| [SMS_InstalledExecutable Client WMI Class](sms_installedexecutable-client-wmi-class.md) | Identifies executable files associated with a software installation. |
| [SMS_InstalledSoftware Client WMI Class](sms_installedsoftware-client-wmi-class.md) | Merges installed software information from multiple sources to provide categorization and Microsoft Licensing information. |
| [SMS_InstalledSoftwareMS Client WMI Class](sms_installedsoftwarems-client-wmi-class.md) | Merges Microsoft-specific installed software information from multiple sources to provide categorization and Microsoft Licensing information. |
| [SMS_Processor Client WMI Class](sms_processor-client-wmi-class.md) | Represents a device that can interpret a sequence of instructions on a computer that is running a Windows operating system. |
| [SMS_SoftwareShortcut Client WMI Class](sms_softwareshortcut-client-wmi-class.md) | Defines a shortcut to executable files or a shortcut in a common system location. |
| [SMS_SoftwareTag Client WMI Class](sms_softwaretag-client-wmi-class.md) | Indicates the presence of a software application on a computer.   This information applies to System Center 2012 Configuration Manager SP1 or later, and System Center 2012 R2 Configuration Manager or later. |
| [SMS_SystemConsoleUsage Client WMI Class](sms_systemconsoleusage-client-wmi-class.md) | Defines usage data about devices, based on the system security event log. |
| [SMS_SystemConsoleUser Client WMI Class](sms_systemconsoleuser-client-wmi-class.md) | Defines usage data about users, based on the system security event log. |

## Remarks

Classes related to the asset intelligence client WMI classes are:

- `SoftwareLicensingProduct` class. For more information, see [SoftwareLicensingProduct class](https://learn.microsoft.com/en-us/previous-versions/windows/desktop/sppwmi/softwarelicensingproduct).
- `SoftwareLicensingService` class. For more information, see [SoftwareLicensingService class](https://learn.microsoft.com/en-us/previous-versions/windows/desktop/sppwmi/softwarelicensingservice).
- `Win32_USBDevice` class. Tracks devices connected to USB ports.

## See also

[Initiate Asset Intelligence synchronization](../../../../core/clients/asset-intelligence/how-to-initiate-a-synchronization.md)
