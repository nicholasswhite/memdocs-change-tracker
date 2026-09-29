---
title: AppContentInfo Structure
description: The AppContentInfo structure provides information about the application content.
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
---

# AppContentInfo Structure

In Configuration Manager, the `AppContentInfo` structure contains information about the application content.

## Syntax

```
struct AppContentInfo
{
    LPCWSTR szContentId;
    LPCWSTR szContentVersion;
    LPCWSTR szLocalPath;
};
```

## Members

`szContentId` The content id.

`szContentVersion` The content version.

`szLocalPath` The local path.

## See Also

[Configuration Manager Software Development Kit](../../../../core/misc/system-center-configuration-manager-sdk.md) [Configuration Manager Reference](../../../configuration-manager-reference.md)
