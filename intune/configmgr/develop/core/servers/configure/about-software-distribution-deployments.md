---
title: "About Software Distribution Deployments"
description: In Configuration Manager, after a software distribution package has been created, with programs to tell client computers what to do with the package, you need to advertise the program.
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: concept-article
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

# About Software Distribution Deployments

In Configuration Manager, after a software distribution package has been created, with programs to tell client computers what to do with the package, you need to advertise the program that you want the clients to run. Advertising the program makes a program available to a specified collection of clients.

Advertisements are evaluated by Configuration Manager to determine which clients receive a specific program to run on their computers. An advertisement specifies the following information:

- The specific program to run on the client.
- The target collection of computers, users, or user groups that are to receive the program.
- The schedule that specifies when the program is available to clients. If there are assigned (mandatory) advertisements, other options such as Wake On LAN and ignoring maintenance windows can be used with this schedule.

  The site's clients can't receive advertised programs until you enable the software distribution advertised programs client agent on the site's clients. The **Advertised Programs Client Agent** performs the necessary software distribution-related tasks on these clients, primarily allowing the clients to receive and run the programs that you advertise.

## See Also

[About deployments](about-software-distribution-deployments.md) [Software distribution overview](software-distribution-overview.md)
