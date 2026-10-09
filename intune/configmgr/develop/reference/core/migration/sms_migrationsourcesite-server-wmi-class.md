---
title: "SMS_MigrationSourceSite Server WMI Class"
description: Learn how the SMS_MigrationSourceSite class is an SMS Provider server class, in Configuration Manager, that represents a site in the source hierarchy.
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
author: sccmavenger
cmProducts:
- https://authoring-docs-microsoft.poolparty.biz/devrel/aa9d0281-4c35-44bb-8c75-a0920bde2014
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
- https://authoring-docs-microsoft.poolparty.biz/devrel/c7449412-70b0-48ea-831f-3b132eafb97e
---

# SMS_MigrationSourceSite Server WMI Class

The `SMS_MigrationSourceSite` Windows Management Instrumentation (WMI) class is an SMS Provider server class, in Configuration Manager, that represents a site in the source hierarchy.

The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.

## Syntax

```
Class SMS_MigrationSourceSite : SMS_BaseClass
{
    String FQDN;
    Boolean IsCentral;
    Boolean IsConfigured;
    Boolean IsDecommissioned;
    Boolean IsDeleted;
    String ParentSiteCode;
    String ParentSiteServer;
    String SiteCode;
    UInt32 SiteID;
    UInt32 SiteType;
    String SourceSiteFQDN;
    String Version;
};
```

## Methods

The `SMS_MigrationSourceSite` class does not define any methods.

## Properties

`FQDN` Data type: `String`

Access type: Read-only

Qualifiers: none

FQDN of the source Site Server (deprecated).

`IsCentral` Data type: `Boolean`

Access type: Read-only

Qualifiers: none

`true` if the source site is a central site.

`IsConfigured` Data type: `Boolean`

Access type: Read-only

Qualifiers: none

`true` if the source site is configured.

`IsDecommissioned` Data type: `Boolean`

Access type: Read-only

Qualifiers: none

`true` if the site has stopped gathering data.

`IsDeleted` Data type: `Boolean`

Access type: Read-only

Qualifiers: none

`true` if the source site is deleted.

`ParentSiteCode` Data type: `String`

Access type: Read-only

Qualifiers: none

The site code of the parent site of the source site.

`ParentSiteServer` Data type: `String`

Access type: Read-only

Qualifiers: none

The site server name of the parent site of the source site.

`SiteCode` Data type: `String`

Access type: Read-only

Qualifiers: none

The source site code.

`SiteID` Data type: `UInt32`

Access type: Read-only

Qualifiers: [key]

The source site ID.

`SiteType` Data type: `UInt32`

Access type: Read-only

Qualifiers: [enumeration]

See [SMS_SCI_SiteDefinition Server WMI Class](../servers/configure/sms_sci_sitedefinition-server-wmi-class.md).

`SourceSiteFQDN` Data type: `String`

Access type: Read-only

Qualifiers: none

The FQDN of the source site server.

`Version` Data type: `String`

Access type: Read-only

Qualifiers: none

The version of the source site.

This information applies to System Center 2012 Configuration Manager SP1 or later, and System Center 2012 R2 Configuration Manager or later.

## Remarks

All of the instances are gathered from the Configuration Manager database, except for the first one which is created when you specify the source hierarchy. Each instance carries basic information for the source site, such as the parent site code, the site type and the FQDN of the site.

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../../core/reqs/server-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../../core/reqs/server-development-requirements.md).
