---
description: Learn how to use the group action in configuration manager to create a submenu for related actions.
title: Configuration Manager Group Action
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
spProducts:
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/6a8c83be-f1de-4e90-bde0-bd097999a60c
cmProducts:
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/4c50f262-d533-4ba4-9d4a-08899ec3a3d1
---

# Configuration Manager Group Action

In Configuration Manager, the Group action creates a menu group, also known as a submenu, for related actions.

The following attributes and elements are specific to an action that creates a group of context menu items:

- The &lt;`ActionDescription`&gt; element `Class` attribute is set to **Group**.
- The &lt;`DisplayName`&gt; attribute is the group name displayed in the context menu.
- The &lt;`GroupAsRegion`&gt; Boolean attribute specifies whether or not to display this group as a region on the ribbon bar.
- The &lt;`ActionGroups`&gt; element is a list of actions (&lt;`ActionDescription`&gt; elements) displayed in the context menu group.

## Group Action XML

The following XML demonstrates a group of actions named New Group Name:

```
<ActionDescription Class="Group" GroupAsRegion="true" DisplayName="New Group Name" MnemonicDisplayName="MnemonicNewGroupName" Description="NewGroupNameDescription">  <ShowOn>      <string>DefaultContextualTab</string> <!-- RIBBON -->     <string>ContextMenu</string> <!-- Context Menu -->   </ShowOn>       <ActionGroups>
    <ActionDescription Class="Executable" DisplayName="Test Action (execute)" MnemonicDisplayName="A test item" Description="A test item Description">          <ShowOn>          <string>DefaultContextualTab</string> <!-- RIBBON -->         <string>ContextMenu</string> <!-- Context Menu -->      </ShowOn>         <Executable>
      <FilePath>https://go.microsoft.com/fwlink/?LinkId=67307</FilePath>
    </Executable>
    </ActionDescription>
    <ActionDescription Class="Report" DisplayName="Test Action (report)" MnemonicDisplayName="Mnemonic" Description="Description">
    <ShowOn>         <string>DefaultContextualTab</string> <!-- RIBBON -->        <string>ContextMenu</string> <!-- Context Menu -->      </ShowOn>            <ReportDescription Id="05874720-1D08-4CF7-B182-5F9D065BEAE5">
      </ReportDescription>
    </ActionDescription>
  </ActionGroups>
</ActionDescription>
```

## See Also

[About Configuration Manager console actions](configuration-manager-actions.md) [How to Create a Configuration Manager Action](how-to-create-a-configuration-manager-action.md) [How to Find a Configuration Manager Node GUID](how-to-find-a-configuration-manager-console-node-guid.md)
