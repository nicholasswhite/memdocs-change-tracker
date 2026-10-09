---
title: "Evaluation of the All collections report in Configuration Manager"
description: Information about all of the collections in the Configuration Manager hierarchy.
ms.date: "2019-04-30T00:00:00Z"
ms.subservice: sdk
ms.topic: article
ms.collection: tier3
ms.service: configuration-manager
author: sccmavenger
cmProducts:
- https://authoring-docs-microsoft.poolparty.biz/devrel/07bb3e10-d135-43ff-bc8b-360497cb39fa
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
- https://authoring-docs-microsoft.poolparty.biz/devrel/12e559b9-eaf6-4aee-9af7-62334e15f863
---

# Evaluation of the All collections report in Configuration Manager

The **All collections** report is one of the built-in reports in Configuration Manager and is a good example of a basic report. This report lists all of the collections in the Configuration Manager hierarchy.

To open the report, use the following procedure:

## To examine the properties of the All collections report

1. In the Configuration Manager console, select **Monitoring**.
2. In the **Monitoring** workspace, expand **Reporting**, and then select **Reports**.
3. From the list of reports, select **All collections** and then, in the **Home** tab, in the **Report Group** group, select **Edit**.
4. In the **Report Data** pane of Report Builder, expand **Datasets** and then double-click **DataSet0**.
5. In the **Dataset Properties** dialog box, you can view the SQL query for the report, the fields that will be returned, and the parameters that the report uses.
6. Close the **Dataset Properties** dialog box.
7. Close Report Builder.

## See also

[Evaluation of the computer information for a specific computer report in Configuration Manager](evaluation-computer-information-report-configuration-manager.md)
