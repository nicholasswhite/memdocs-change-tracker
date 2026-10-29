---
title: "Configuration Manager Role-Based Administration"
description: This section provides topics about programmatically managing role-based administration in Configuration Manager.
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: article
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
spProducts:
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/6a8c83be-f1de-4e90-bde0-bd097999a60c
---

# Configuration Manager Role-Based Administration

This section provides topics about programmatically managing role-based administration in Configuration Manager.

> [!NOTE]
>
> For more information, see [Fundamentals of role-based administration](../../../../core/understand/fundamentals-of-role-based-administration.md).

## About role-based administration

Role-based administration security rights are applied to a domain user or a security group. In Configuration Manager security rights are replicated to all sites in the hierarchy. You can use any single site to change the security rights of a user or security group and it will be automatically replicated to all other sites in that same hierarchy.

Security consists of two basic concepts: security roles and security scopes.

### Security Roles

A security role in Configuration Manager grants permissions to the types of objects a user can interact with, and the actions they can perform with those objects. Configuration Manager provides multiple built-in security roles.

### Security Scopes

A security scope in Configuration Manager establishes security restrictions between the user and object instances. The permissions the user will have with that object instance are determined by their assigned security roles.

### Administrative Users and Security Groups

Domain users and security groups can be granted access to Configuration Manager. The permissions set on an administrator consist of a combination of a security role and scope. A scope is applied to a role that the administrator has. It can never be applied independently of the role.

## See also

[Configuration Manager SDK](../../misc/system-center-configuration-manager-sdk.md)
