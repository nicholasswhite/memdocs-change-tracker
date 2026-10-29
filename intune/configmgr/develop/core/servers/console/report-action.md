---
description: Learn how to use report action in the configuration manager to display reports in the configuration manager console.
title: Configuration Manager Report Action
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: article
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

# Configuration Manager Report Action

The report action displays a Configuration Manager report in the Configuration Manager console.

The following attributes and elements are specific to an action that opens a report box:

- The `ActionDescription` element `Class` attribute is set to **Report**.
- The `ReportDescription` element `ReportName` attribute is the GUID of the report to be displayed. The GUID maps to the `SMS_Report` class `ReportGUID` property.

> [!NOTE]
>
> An alternative method to load a report is to use the executable action to launch the report's URL. This will display the report in a new window rather than in the Configuration Manager console.

## Sample Report Action XML

The following XML demonstrates how to display a report, identified by its GUID, in the Configuration Manager console:

```
<ActionDescription Class="Report" DisplayName="Test Action (report)" MnemonicDisplayName="Mnemonic" Description="Description"> <ShowOn>      <string>DefaultContextualTab</string> <!-- RIBBON -->     <string>ContextMenu</string> <!-- Context Menu -->   </ShowOn>
 <ReportDescription ReportName="05874720-1D08-4CF7-B182-5F9D065BEAE5">
 </ReportDescription>
</ActionDescription>
```

## See Also

[Configuration Manager Actions](configuration-manager-actions.md) [How to Create a Configuration Manager Action](how-to-create-a-configuration-manager-action.md) [How to Find a Configuration Manager Node GUID](how-to-find-a-configuration-manager-console-node-guid.md) [How to Find a Configuration Manager Node GUID](how-to-find-a-configuration-manager-console-node-guid.md)
