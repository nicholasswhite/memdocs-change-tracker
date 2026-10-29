---
title: Deployment Type Extension Versioning
description: Configuration Manager supports in-place versioning for minor upgrades and out-of-place versioning for major upgrades.
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: install-set-up-deploy
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

# Deployment Type Extension Versioning

Configuration Manager supports in-place versioning for minor upgrades and out-of-place versioning for major upgrades.

## Versioning

### Minor Revisions

Configuration Manager supports in-place versioning for minor upgrades that are backwards compatible. For in-place versioning, increment the version number.

### Major Revisions

Configuration Manager supports out-of-place versioning for major upgrades that aren't backwards compatible. For out-of-place versioning, it's necessary to create a new extension and technology ID.

## See Also

[Configuration Manager Reference](../reference/configuration-manager-reference.md)
