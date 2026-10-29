---
description: Learn how to set a distribution point in maintenance mode using SetDPMaintenanceMode class method in Configuration Manager.
title: "SetDPMaintenanceMode method in class SMS_DistributionPoint"
ms.date: "2019-05-24T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
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

# SetDPMaintenanceMode method in class SMS_DistributionPoint

The `SetDPMaintenanceMode` WMI class method in Configuration Manager sets a distribution point in maintenance mode. For more information, see [Maintenance mode](../../../../../core/servers/deploy/configure/install-and-configure-distribution-points.md#bkmk_maint).

The following syntax is simplified from Managed Object Format (MOF) code and defines the method.

## Syntax

```MOF
uint32 SetDPMaintenanceMode(
    [in] string NALPath,
    [in] uint32 Mode
);
```

## Parameters

### `NALPath`

Data type: `String`

Qualifiers: `[in]`

Network abstraction layer (NAL) path to the distribution point server.

### `Mode`

Data type: `uint32`

Qualifiers: `[in]`

`1` to enable maintenance mode, `0` to disable

## Return values

An `uint32` data type that's `0` indicates success. A non-zero hresult indicates failure.

For more information about handling returned errors, see [About Configuration Manager errors](../../../../core/understand/about-configuration-manager-errors.md).

## Requirements

### Runtime requirements

For more information, see [Configuration Manager server runtime requirements](../../../../core/reqs/server-runtime-requirements.md).

### Development requirements

For more information, see [Configuration Manager server development requirements](../../../../core/reqs/server-development-requirements.md).

## See also

[SMS_DistributionPointInfo Server WMI Class](sms_distributionpointinfo-server-wmi-class.md)
