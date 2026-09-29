---
title: CIPackageInfo Structure
description: In Configuration Manager, the CIPackageInfo structure contains package information for a configuration item.
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
---

# CIPackageInfo Structure

In Configuration Manager, the `CIPackageInfo` structure contains package information for a configuration item.

## Syntax

```
struct CIPackageInfo
{
      LPWSTR szTypeName;
      LPWSTR szPackageName;
      LPWSTR szPackageVersion;
      LPWSTR szNamespace;
};
```

## Members

szTypeName Name of the configuration item.

szPackageName Name of the package.

szPackageVersion Version of the package.

szNamespace Namespace used by the package software.

## See Also

[Compliance Settings (DCM) Client Interfaces](compliance-settings--dcm--client-interfaces.md) [ICIINFO::GetDependantPackages Method](iciinfo--getdependantpackages-method.md)
