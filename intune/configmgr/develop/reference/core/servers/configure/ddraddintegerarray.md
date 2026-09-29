---
title: DDRAddIntegerArray
description: The DDRAddIntegerArray function, in Configuration Manager, adds an integer array property to the data discovery record (DDR).
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
---

# DDRAddIntegerArray

The `DDRAddIntegerArray` function, in Configuration Manager, adds an integer array property to the data discovery record (DDR).

## Syntax

```
[IDL]
HRESULT DDRAddIntegerArray();
```

#### Parameters

`Name` Name of the class property.

`Array` Array of integers assigned to the property.

`Flags` Characteristics of the property, such as identifying this property as a key field for comparisons. Enter the following flag or a zero.

| Flag | Description |
| --- | --- |
| ADDPROP_KEY (Hexadecimal 8) | Identifies this property as a key field during a comparison of this DDR with class instances in the database. If an instance in the database matches the data of the DDR key properties, the instance is updated; otherwise, a new instance is created. |

## Return Values

If the function succeeds, the return value is S_OK.

If the [DDRNew](ddrnew.md) function has not been called, the return value is S_FALSE.

## Requirements

## Runtime Requirements

smsrsgenctl.dll

smsrsgen.dll

For more information, see [Configuration Manager Server Runtime Requirements](../../../../core/reqs/server-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../../../core/reqs/server-development-requirements.md).

## See Also

[DDRAddInteger](ddraddinteger.md) [DDRAddStringArray](ddraddstringarray.md) [DDRPropertyFlagsEnum Enumeration](ddrpropertyflagsenum-enumeration.md) [SMSResGen COM Automation Class](smsresgen-com-automation-class.md) [ISMSResGen Interface](ismsresgen-interface.md)
