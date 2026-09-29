---
title: "Capabilities in Configuration Manager technical preview version 1808"
description: Learn about new features available in the Configuration Manager technical preview branch version 1808.
ms.date: "2018-08-17T00:00:00Z"
ms.subservice: core-infra
ms.topic: whats-new
ROBOTS: NOINDEX
ms.collection: tier3
ms.service: configuration-manager
---

# Capabilities in Configuration Manager technical preview version 1808

*Applies to: Configuration Manager (technical preview branch)*

This article introduces the features that are available in the technical preview for Configuration Manager, version 1808. Install this version to update and add new features to your technical preview site.

Review the [technical preview](technical-preview.md) article before installing this update. That article familiarizes you with the general requirements and limitations for using a technical preview, how to update between versions, and how to provide feedback.

  

**The following sections describe the new features to try out in this version:**

## Phased deployment of software updates

Create phased deployments for software updates. Phased deployments allow you to orchestrate a coordinated, sequenced rollout of software based on customizable criteria and groups.

In the Configuration Manager console, go to the **Software Library**, expand **Software Updates**, and select **All Software Updates**. Select one update, and then click **Create Phased Deployment** in the ribbon. This action is also available from the **All Windows 10 Updates** and **Office 365 Updates** nodes.

The behavior of a software update phased deployment is the same as for task sequences and applications. For more information, see [Create phased deployments](../../osd/deploy-use/create-phased-deployment-for-task-sequence.md).

### Known issues

- The Create Phased Deployment wizard only provides the option to **Automatically create a default two phase deployment**.
- The setting to **Gradually make the software available over this period of time (in days)** doesn't work.

## Improvement to repair applications

A new button is now available in Software Center to **Repair** an application. When you configure an application with a repair program, users can start the command from Software Center.

For more information, see [Repair applications](capabilities-in-technical-preview-1807.md#bkmk_app-repair).

## Next steps

For more information about installing or updating the technical preview branch, see [Technical preview](technical-preview.md).

For more information about the different branches of Configuration Manager, see [Which branch of Configuration Manager should I use?](../understand/which-branch-should-i-use.md)
