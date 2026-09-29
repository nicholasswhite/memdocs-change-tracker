---
title: ICIINFO Interface
description: ICIINFO can represent a configuration item which has been downloaded and stored by the Desired Configuration Management client or a baseline configuration item in a Desired Configuration Management Agent job in the client data store.
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
---

# ICIINFO Interface

The `ICIINFO` interface, in Configuration Manager, can represent the properties of a configuration item which has been downloaded and stored by the Desired Configuration Management client or the properties of a baseline configuration item in a Desired Configuration Management Agent job in the client data store. In both cases, the configuration item is either a (top level/root) baseline or a Software Updates configuration item.

The interface inherits from `IUnknown`.

## In This Section

The following table lists the methods in the `ICIINFO` interface.

| Term | Definition |
| --- | --- |
| [ICIINFO::GetCategory](iciinfo--getcategory-method.md) | Gets a localized category name by index and the group name of the category. |
| [ICIINFO::GetCategoryCount](iciinfo--getcategorycount-method.md) | Gets the count of categories applied to the configuration item. |
| [ICIINFO::GetCIPresence](iciinfo--getcipresence-method.md) | Gets the current presence for the configuration item. |
| [ICIINFO::GetContextInfo](iciinfo--getcontextinfo-method.md) | Gets the context information by name from the configuration item. |
| [ICIINFO::GetDependantPackages](iciinfo--getdependantpackages-method.md) | Gets dependent package information for the configuration item. |
| [ICIINFO::GetDetailedComplianceInfo](iciinfo--getdetailedcomplianceinfo-method.md) | Gets detailed compliance information from the last compliance evaluation run for the configuration item. |
| [ICIINFO::GetEvalState](iciinfo--getevalstate-method.md) | Gets the current evaluation state of the configuration item. |
| [ICIINFO::GetId](iciinfo--getid-method.md) | Gets the ID of the configuration item. |
| [ICIINFO::GetJobState](iciinfo--getjobstate-method.md) | Gets the current operational job state of the configuration item that is part of a job or task. |
| [ICIINFO::GetLastEvalTime](iciinfo--getlastevaltime-method.md) | Gets the last evaluation time for the configuration item. |
| [ICIINFO::GetProperty](iciinfo--getproperty-method.md) | Gets a named property value from the configuration item. |
| [ICIINFO::GetSdmTypeName](iciinfo--getsdmtypename-method.md) | Gets the fully qualified name of a root configuration item. |
| [ICIINFO::GetVersion](iciinfo--getversion-method.md) | Gets the version of the configuration item. |

## Remarks

To obtain this interface, the application calls the [IDCMSDK Interface](idcmsdk-interface.md). The application calls the [IDCMAgentCallback Interface](idcmagentcallback-interface.md) interface to respond to agent calls.

## UUID

The UUID for `ICIINFO` is ACF43B8E-23A2-4923-B421-CB918FC5CA1F.

## See Also

[Compliance Settings (DCM) Client Interfaces](compliance-settings--dcm--client-interfaces.md) [IDCMSDK Interface](idcmsdk-interface.md) [IDCMAgentCallback Interface](idcmagentcallback-interface.md)
