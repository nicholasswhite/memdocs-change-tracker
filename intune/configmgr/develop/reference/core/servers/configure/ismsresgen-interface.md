---
description: Learn how to use the ISMSResGen Interface to enable the creation of Data Discovery Records (DDR). This interface inherits from IDispatch.
title: ISMSResGen Interface
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
author: sccmavenger
cmProducts:
- https://authoring-docs-microsoft.poolparty.biz/devrel/540ac133-a371-4dbb-8f94-28d6cc77a70b
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
- https://authoring-docs-microsoft.poolparty.biz/devrel/60bfc045-f127-4841-9d00-ea35495a5800
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/24dc3ccd-591a-4415-a1fe-8759afafcb12
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/6a8c83be-f1de-4e90-bde0-bd097999a60c
---

# ISMSResGen Interface

The `ISMSResGen` automation interface, in Configuration Manager, enables the creation of Data Discovery Records (DDR). This interface inherits from `IDispatch`.

## In This Section

| Term | Definition |
| --- | --- |
| [DDRNew](ddrnew.md) | Creates a new DDR. |
| [DDRAddInteger](ddraddinteger.md) | Adds an integer property to the DDR. |
| [DDRAddString](ddraddstring.md) | Adds a string property to the DDR. |
| [DDRAddIntegerArray](ddraddintegerarray.md) | Adds an integer array property to the DDR. |
| [DDRAddStringArray](ddraddstringarray.md) | Adds a string array property to the DDR. |
| [DDRWrite](ddrwrite.md) | Writes the DDR to a file. |
| [DDRPropertyFlagsEnum Enumeration](ddrpropertyflagsenum-enumeration.md) | Defines flags used by `ISMSResGen`. |

## Remarks

These functions create a single DDR that is sent to the Data Discovery Manager (DDM). The order in which you call the functions is important; you must call `DDRNew` before calling any of the functions that add properties. However, the order in which you add properties to your class is arbitrary. The last function you call must be `DDRWrite` to create the DDR. The DDR must then be manually copied to the **SMS\Inboxes\Auth\Ddm.box** directory.

DDRs that fail to load are moved to the **SMS\Inboxes\Ddm.box\Bad_ddrs** directory. If you have logging turned on, you can view the DDM.log file for an explanation of the failure. After you fix the errors, you can rerun your program to load the DDR.

The IID for `ISMSResGen` is ECB65D0E-B16B-4817-92B0-BF2D9CEFB3AC.

## Requirements

### Runtime Requirements

smsrsgenctl.dll

smsrsgen.dll

For more information, see [Configuration Manager Server Runtime Requirements](../../../../core/reqs/server-runtime-requirements.md).

### Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../../../core/reqs/server-development-requirements.md).

## See Also

[SMSResGen COM Automation Class](smsresgen-com-automation-class.md)
