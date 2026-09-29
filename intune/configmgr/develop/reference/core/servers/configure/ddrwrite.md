---
title: DDRWrite
description: The`DDRWrite function, in Configuration Manager, writes the data discovery records (DDRs) to a file.
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
---

# DDRWrite

The `DDRWrite` function, in Configuration Manager, writes the data discovery records (DDRs) to a file.

## Syntax

```
[IDL]
HRESULT DDRWrite();
```

#### Parameters

`FileName` Valid Universal Naming Convention (UNC) file name. Use the .ddr file name extension when you specify the file name.

## Return Values

If the function succeeds, the return value is S_OK.

If the [DDRNew](ddrnew.md) function hasn't been called or a file error occurs, the return value is S_FALSE.

## Remarks

Calling `DDRWrite` completes the DDR and writes the record to a binary file. The DDR must be copied to the Data Discovery Manager (DDM) inbox on the site server at a later time (SMS\Inboxes\Auth\Ddm.box).

## Requirements

## Runtime Requirements

smsrsgenctl.dll

smsrsgen.dll

For more information, see [Configuration Manager Server Runtime Requirements](../../../../core/reqs/server-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../../../core/reqs/server-development-requirements.md).

## See Also

[DDRPropertyFlagsEnum Enumeration](ddrpropertyflagsenum-enumeration.md) [SMSResGen COM Automation Class](smsresgen-com-automation-class.md) [ISMSResGen Interface](ismsresgen-interface.md)
