---
description: Learn how to use the DDRPropertyFlagsEnum enumeration in Configuration Manager which specifies flags that are used by ISMSResGen.
title: DDRPropertyFlagsEnum Enumeration
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
author: sccmavenger
cmProducts:
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
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/24dc3ccd-591a-4415-a1fe-8759afafcb12
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/6a8c83be-f1de-4e90-bde0-bd097999a60c
---

# DDRPropertyFlagsEnum Enumeration

The `DDRPropertyFlagsEnum` enumeration, in Configuration Manager, specifies flags that are used by `ISMSResGen`.

## Syntax

```
enum DDRPropertyFlagsEnum
{
    ADDPROP_NONE = 0x0,
    ADDPROP_GUID = 0x00000002,
    ADDPROP_GROUPING = 0x00000004,
    ADDPROP_KEY = 0x00000008,
    ADDPROP_ARRAY = 0x00000010,
    ADDPROP_AGENT = 0x00000020,
    ADDPROP_NAME = 0x00000044,
    ADDPROP_NAME2 = 0x00000084
};
```

## Elements

ADDPROP_NONE(0x0) No special properties.

ADDPROP_GUID(0x00000002) Defines this property as being a GUID.

ADDPROP_GROUPING(0x00000004) Reserved.

ADDPROP_KEY(0x00000008) Defines this property as being a Key value that must be unique.

ADDPROP_ARRAY(0x00000010) Reserved.

ADDPROP_AGENT(0x00000020) Reserved.

ADDPROP_NAME(0x00000044) Specifies this property as the actual `Name` property in the resource.

ADDPROP_NAME2(0x00000084) Specifies this property as the actual `Comment` property in the resource.

## Requirements

## Runtime Requirements

smsrsgenctl.dll

smsrsgen.dll

For more information, see [Configuration Manager Server Runtime Requirements](../../../../core/reqs/server-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../../../core/reqs/server-development-requirements.md).

## See Also

[SMSResGen COM Automation Class](smsresgen-com-automation-class.md) [DDRAddStringArray](ddraddstringarray.md) [DDRAddIntegerArray](ddraddintegerarray.md) [DDRAddInteger](ddraddinteger.md) [DDRNew](ddrnew.md) [DDRWrite](ddrwrite.md) [DDRAddString](ddraddstring.md) [SMSResGen COM Automation Class](smsresgen-com-automation-class.md) [ISMSResGen Interface](ismsresgen-interface.md)
