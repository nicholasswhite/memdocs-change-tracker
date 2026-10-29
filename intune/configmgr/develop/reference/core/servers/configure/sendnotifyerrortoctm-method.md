---
description: Learn how to notify Content Transfer Manager of errors using the SendNotifyErrorToCTM method, in Configuration Manager.
title: SendNotifyErrorToCTM Method
ms.date: "2016-09-20T00:00:00Z"
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

# SendNotifyErrorToCTM Method

The **SendNotifyErrorToCTM** method, in Configuration Manager, notifies Content Transfer Manager of errors.

## Syntax

```
HRESULT stdcall SendNotifyErrorToCTM(
    LPCWSTR szEndpoint,
    LPCWSTR szID,
    LPCWSTR szClientData,
    HRESULT hrErrorCode,
    LPCWSTR szErrorMessage
);

```

#### Parameters

`szEndpoint` Data type: LPCWSTR

Qualifiers: [in]

The notification endpoint. This was passed into the call to **ICcmAlternateDownloadProvider::DownloadContent** (szNotifyEndpoint).

`szID` Data type: LPCWSTR

Qualifiers: [in]

The job to which the notification corresponds. This is the GUID originally returned by **ICcmAlternateDownloadProvider::DownloadContent**.

`szClientData` Data type: LPCWSTR

Qualifiers: [in]

The client-specific data that was passed into the call to **ICcmAlternateDownloadProvider::DownloadContent** (szNotifyData.)

`hrErrorCode` Data type: HRESULT

Qualifiers: [in]

The failure code to report.

`szErrorMessage` Data type: LPCWSTR

Qualifiers: [in]

An extended status message. Must not be NULL.

## Return Values

An `HRESULT` code. Possible values include, but aren't limited to, the following one:

S_OK Success implies that discovery was triggered successfully. All other return values indicate failure.

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Client Runtime Requirements](../../../../core/reqs/client-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Client Development Requirements](../../../../core/reqs/client-development-requirements.md).
