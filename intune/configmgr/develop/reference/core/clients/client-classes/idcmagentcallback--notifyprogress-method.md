---
description: "Learn how to notify the caller of progress made on a Desired Configuration Management Agent job using IDCMAgentCallback::NotifyProgress."
title: "IDCMAgentCallback::NotifyProgress Method"
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
---

# IDCMAgentCallback::NotifyProgress Method

The `IDCMAgentCallback::NotifyProgress` method, in Configuration Manager, notifies the caller of progress made on a Desired Configuration Management Agent job.

## Syntax

```
[IDL]
HRESULT NotifyProgress(
     IDCMAgentJob* pJob,
     MessageId msgId
);
```

#### Parameters

`pJob` Data type: `IDCMAgentJob`

Qualifiers: [in]

Pointer to the `IDCMAgentJob` object representing the configuration items and their progress.

`msgId` Data type: `MessageId`

Qualifiers: [in]

Nothing is returned for this parameter.

## Return Values

An `HRESULT` code. Possible values include, but are not limited to, the following:

S_OK The method succeeded. All other return values indicate failure.

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Client Runtime Requirements](../../../../core/reqs/client-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Client Development Requirements](../../../../core/reqs/client-development-requirements.md).

## See Also

[IDCMAgentCallback Interface](idcmagentcallback-interface.md)
