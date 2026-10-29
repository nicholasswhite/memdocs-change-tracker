---
title: "How to modify Configuration Manager reports"
description: Information about viewing the properties of, and modifying Configuration Manager reports.
ms.date: "2019-04-30T00:00:00Z"
ms.subservice: sdk
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

# How to modify Configuration Manager reports

The procedures in this topic help you to view the properties of, and modify Configuration Manager reports.

## How to view the general properties of a report

You can view general properties for a report in the Configuration Manager console. Use the following procedure to view the properties of a report.

### To view the general properties of a report

1. In the Configuration Manager console, select **Monitoring**.
2. In the **Monitoring** workspace, expand **Reporting**, and then select **Reports**.
3. From the list of reports, select the report that you want to view properties for and then, in the **Home** tab, in the **Properties** group, select **Properties**.
4. In the *report name*�**Properties** dialog box, you can view general information about the report, create and view report subscriptions and view security information about the report.
5. Close the *report name*�**Properties** dialog box.

## How to modify a report

Use SQL Server Report Builder to modify reports. Report Builder can be opened directly from the Configuration Manager console. Use the following procedure to modify a Configuration Manager report.

### To modify a report

1. In the Configuration Manager console, select **Monitoring**.
2. In the **Monitoring** workspace, expand **Reporting**, and then select **Reports**.
3. From the list of reports, select the report that you want to view properties for and then, in the **Home** tab, in the **Report Group** group, select **Edit**.
4. In SQL Server Report builder, make the necessary modifications to the report.
5. Save your report, and then close Report Builder.

## See also

[How to create Configuration Manager reports](how-to-create-configuration-manager-reports.md)
