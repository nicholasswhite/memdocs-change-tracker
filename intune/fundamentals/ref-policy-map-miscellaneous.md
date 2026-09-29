---
title: Miscellaneous policy mapping from Basic Mobility and Security to Intune
description: A detailed miscellaneous policy map between Basic Mobility and Security access requirements and Intune.
ms.date: "2025-12-03T00:00:00Z"
ms.topic: reference
ms.reviewer: dagerrit
---

# Miscellaneous policy mapping from Basic Mobility and Security to Intune

This article provides mapping details between Basic Mobility and Security to Intune. Specifically, this page maps the following Microsoft Purview compliance portal policies and device properties to the equivalent policies and properties in the Microsoft Intune admin center:

- Device properties and actions
- Organization-wide device access settings
- Device security policies Name and Description

Intune offers more policy flexibility. So, each Office policy translates into multiple Intune and Microsoft Entra policies to achieve the same result.

## Device properties and actions

To see these settings, sign in to the [Microsoft 365 admin center](https://portal.office.com/adminportal/home#/MifoDevices) and then select a device.

### User

- **Devices** &gt; **All devices** &gt; device name &gt; **Overview** &gt; **Enrolled by**

### Device type

- **Devices** &gt; **All devices** &gt; device name &gt; **Overview** &gt; **Operating system**

### State

This setting isn't a default column in the admin center device list. You can show it by using the **Columns** picker.

- **Devices** &gt; **All devices** &gt; **Device state** column

### OS version

- **Devices** &gt; **All devices** &gt; device name &gt; **Hardware** &gt; **Operating system version**

### Factory reset

- **Devices** &gt; **All devices** &gt; device name &gt; **Overview** &gt; **Wipe**

### Remove company data

- **Devices** &gt; **All devices** &gt; device name &gt; **Overview** &gt; **Retire**

## Organization-wide device access settings

To see these settings in the Microsoft Purview compliance portal, sign in to the [Purview compliance portal](https://protection.office.com/devicev2). Then, select **Device security policies** &gt; **Manage organization-wide device access settings**.

These settings are backed by the Conditional Access policy [GraphAggregatorService] Device policy. It includes:

- Device platforms: iOS, Android
- Target client apps: Mobile app desktop clients
- Access controls: require compliant device

### If a device isn't supported by MDM for Office 365, do you want to allow or block it from using an Exchange account to access your organization's email?

This setting modifies one classic Conditional Access policy:

- **Endpoint security** &gt; **Conditional Access** &gt; **Classic policies** &gt; **[GraphAggregatorService] Device policy** &gt; **Conditions** &gt; **Client apps (Preview)** &gt; **Mobile apps and desktop clients** &gt; **Exchange ActiveSync clients** &gt; **Apply policy only to supported platform**

### Are there any security groups you want to exclude from access control?

This setting modifies five classic Conditional Access policies:

- [GraphAggregatorService] Device policy
- [Office 365 Exchange Online] Device policy
- [Outlook Service for Exchange] Device policy
- [Office 365 SharePoint Online] Device policy
- [Outlook Service for OneDrive] Device policy
- **Endpoint security** &gt; **Conditional Access** &gt; policy name &gt; **Users and groups** &gt; **Exclude**

## Device security policy Name and Description

To see these settings in the Microsoft Purview compliance portal, sign in to the [Purview compliance portal](https://protection.office.com/devicev2). Then, select **Device security policies** &gt; policy name &gt; **Edit policy** &gt; **Name**.

### Name

Up to three compliance policies and up to six configuration profiles (three for restrictions and three for email):

- **Devices** &gt; **By platform** &gt; **Windows** &gt; **Manage devices** &gt; **Compliance** &gt; policy name_O365_W &gt; **Properties** &gt; **Basics Edit** &gt; **Name**
- **Devices** &gt; **By platform** &gt; **iOS/iPadOS** &gt; **Manage devices** &gt; **Compliance** &gt; policy name_O365_i &gt; **Properties** &gt; **Basics Edit** &gt; **Name**
- **Devices** &gt; **By platform** &gt; **Android** &gt; **Manage devices** &gt; **Compliance** &gt; policy name_O365_A &gt; **Properties** &gt; **Basics Edit** &gt; **Name**
- **Devices** &gt; **By platform** &gt; **Windows** &gt; **Manage devices** &gt; **Configuration** &gt; policy name_O365_W &gt; **Properties** &gt; **Basics Edit** &gt; **Name**
- **Devices** &gt; **By platform** &gt; **iOS/iPadOS** &gt; **Manage devices** &gt; **Configuration**&gt; policy name_O365_i &gt; **Properties** &gt; **Basics Edit** &gt; **Name**
- **Devices** &gt; **By platform** &gt; **Android** &gt; **Manage devices** &gt; **Configuration** &gt; policy name_O365_A &gt; **Properties** &gt; **Basics Edit** &gt; **Name**
- **Devices** &gt; **By platform** &gt; **Windows** &gt; **Manage devices** &gt; **Configuration** &gt; policy name_O365_W_Email &gt; **Properties** &gt; **Basics Edit** &gt; **Name**
- **Devices** &gt; **By platform** &gt; **iOS/iPadOS** &gt; **Manage devices** &gt; **Configuration**&gt; policy name_O365_i_Email &gt; **Properties** &gt; **Basics Edit** &gt; **Name**
- **Devices** &gt; **By platform** &gt; **Android** &gt; **Manage devices** &gt; **Configuration** &gt; policy name_O365_A_Email &gt; **Properties** &gt; **Basics Edit** &gt; **Name**

### Description

Up to three compliance policies and up to six configuration profiles (three for restrictions and three for email):

- **Devices** &gt; **By platform** &gt; **Windows** &gt; **Manage devices** &gt; **Compliance** &gt; policy name_O365_W &gt; **Properties** &gt; **Basics Edit** &gt; **Description**
- **Devices** &gt; **By platform** &gt; **iOS/iPadOS** &gt; **Manage devices** &gt; **Compliance** &gt; policy name_O365_i &gt; **Properties** &gt; **Basics Edit** &gt; **Description**
- **Devices** &gt; **By platform** &gt; **Android** &gt; **Manage devices** &gt; **Compliance** &gt; policy name_O365_A &gt; **Properties** &gt; **Basics Edit** &gt; **Description**
- **Devices** &gt; **By platform** &gt; **Windows** &gt; **Manage devices** &gt; **Configuration** &gt; policy name_O365_W &gt; **Properties** &gt; **Basics Edit** &gt; **Description**
- **Devices** &gt; **By platform** &gt; **iOS/iPadOS** &gt; **Manage devices** &gt; **Configuration**&gt; policy name_O365_i &gt; **Properties** &gt; **Basics Edit** &gt; **Description**
- **Devices** &gt; **By platform** &gt; **Android** &gt; **Manage devices** &gt; **Configuration** &gt; policy name_O365_A &gt; **Properties** &gt; **Basics Edit** &gt; **Description**
- **Devices** &gt; **By platform** &gt; **Windows** &gt; **Manage devices** &gt; **Configuration** &gt; policy name_O365_W_Email &gt; **Properties** &gt; **Basics Edit** &gt; **Description**
- **Devices** &gt; **By platform** &gt; **iOS/iPadOS** &gt; **Manage devices** &gt; **Configuration**&gt; policy name_O365_i_Email &gt; **Properties** &gt; **Basics Edit** &gt; **Description**
- **Devices** &gt; **By platform** &gt; **Android** &gt; **Manage devices** &gt; **Configuration** &gt; policy name_O365_A_Email &gt; **Properties** &gt; **Basics Edit** &gt; **Description**

## Related article

- [Move from Basic Mobility and Security to Intune](migrate-from-other-mdm.md)
