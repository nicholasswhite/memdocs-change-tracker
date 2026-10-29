---
title: "How to audit remote control usage in Configuration Manager"
description: Audit remote control use in Configuration Manager.
ms.date: "2017-04-23T00:00:00Z"
ms.subservice: core-infra
ms.topic: how-to
ms.collection: tier3
ms.service: configuration-manager
author: sccmavenger
cmProducts:
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/4c50f262-d533-4ba4-9d4a-08899ec3a3d1
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
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/6a8c83be-f1de-4e90-bde0-bd097999a60c
---

# How to audit remote control usage in Configuration Manager

*Applies to: Configuration Manager (current branch)*

You can use Configuration Manager reports to view audit information for remote control.

For more information about how to configure reporting in Configuration Manager, see [Introduction to reporting](../../../servers/manage/introduction-to-reporting.md).

The following two reports are available with the category **Status Messages - Audit**:

- **Remote Control - All computers remote controlled by a specific user** - Displays a summary of remote control activity that a specific user initiated.
- **Remote Control - All remote control information** - Displays a summary of status messages about remote control of client computers.

### To run the report Remote Control - All computers remote controlled by a specific user

1. In the Configuration Manager console, click **Monitoring**.
2. In the **Monitoring** workspace, expand **Reporting**, and then click **Reports**.
3. In the **Reports** node, click the **Category** column to sort the reports so that you can more easily find the reports in the category **Status Messages - Audit**.
4. Select the report **Remote Control - All computers remote controlled by a specific user**, and then, on the **Home** tab, in the **Report Group**, click **Run**.
5. In the **User Name** list of the **Remote Control - All computers remote controlled by a specific user**, specify the user that you want to report audit information for, and then click **View Report**.
6. When you have finished viewing the data in the report, close the report window.

### To run the report Remote Control - All remote control information

1. In the Configuration Manager console, click **Monitoring**.
2. In the **Monitoring** workspace, expand **Reporting**, and then click **Reports**.
3. In the **Reports** node, click the **Category** column to sort the reports so that you can more easily find the reports in the category **Status Messages - Audit**.
4. Select the report **Remote Control - All remote control information**, and then, on the **Home** tab, in the **Report Group**, click **Run** to open the **Remote Control - All remote control information** window.
5. When you have finished viewing data in the report, close the report window.
