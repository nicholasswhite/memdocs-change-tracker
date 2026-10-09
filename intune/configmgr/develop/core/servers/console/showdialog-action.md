---
title: Configuration Manager ShowDialog Action
ms.date: "2016-09-20T00:00:00Z"
description: In Configuration Manager, the ShowDialog action opens a property sheet or regular dialog box in the console. With the ShowDialog action, you can display existing dialog boxes or extension dialog boxes that you create.
ms.subservice: sdk
ms.topic: article
ms.collection: tier3
ms.service: configuration-manager
author: sccmavenger
cmProducts:
- https://authoring-docs-microsoft.poolparty.biz/devrel/97159432-14a9-4307-a469-d2f2c75f0e33
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
- https://authoring-docs-microsoft.poolparty.biz/devrel/50565c62-5f6b-4687-be38-323113c72c2e
---

# Configuration Manager ShowDialog Action

The `ShowDialog` action, in Configuration Manager, opens a property sheet or regular dialog box in the Configuration Manager console. With the `ShowDialog` action, you can display existing dialog boxes or extension dialog boxes that you create.

The following attributes and elements are specific to an action that opens a dialog box:

- The `ActionDescription` element `Class` attribute is set to `ShowDialog`.
- The `DialogID` element is the identifier for a property sheet or dialog box displayed in a dialog. It matches the name of the form XML file in the *%ProgramFiles%*\Microsoft Endpoint Manager\AdminConsole\XmlStorage\Extensions\Forms folder.

## Sample ShowDialog Action XML

The following XML shows how to show a dialog box with the identifier **PrototypeForm**:

```
<ActionDescription Class="ShowDialog" DisplayName="Test Action (dialog)" MnemonicDisplayName="Mnemonic" Description="Description"> <ShowOn>              <string>DefaultHomeTab</string>      <string>ContextMenu</string>           </ShowOn>
 <DialogId>PrototypeForm</DialogId>
</ActionDescription>
```

## Sample Properties ShowDialog Action XML

The following attributes and elements are specific to an action that adds a property page to a properties property sheet:

- The `ActionDescription` element `ActionVerb` attribute is set to `Properties`.
- The `DialogID` element identifies a property sheet containing the property page to be displayed in the `Properties` dialog.

  The following XML shows how to integrate a property page (`PrototypeForm`) into a properties context menu option:

```
<ActionDescription ActionVerb="Properties" Class="ShowDialog">  <ShowOn>    <string>DefaultHomeTab</string>    <string>ContextMenu</string>  </ShowOn>  <DialogId>PrototypeForm</DialogId>
</ActionDescription>
```

For more information about creating and showing dialog boxes, see [About console forms](about-configuration-manager-console-forms.md).

## See Also

[About Configuration Manager Dialog Boxes](about-configuration-manager-console-forms.md) [Configuration Manager Actions](configuration-manager-actions.md) [How to Create a Configuration Manager Action](how-to-create-a-configuration-manager-action.md) [How to Create Form XML for a Configuration Manager Property Sheet](how-to-create-form-xml-for-a-configuration-manager-property-sheet.md) [How to Create Form XML for a Configuration Manager Dialog Box](how-to-create-form-xml-for-a-configuration-manager-dialog-box.md) [How to Find a Configuration Manager Node GUID](how-to-find-a-configuration-manager-console-node-guid.md)
