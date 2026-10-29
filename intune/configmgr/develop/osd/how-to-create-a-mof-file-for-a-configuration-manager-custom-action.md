---
title: "How to Create a MOF File for a Configuration Manager Custom Action"
description: A custom task sequence action, its properties and its user interface controls are defined by creating a managed object format (MOF) file to describe the class.
ms.date: "2016-09-20T00:00:00Z"
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

# How to Create a MOF File for a Configuration Manager Custom Action

You define a custom task sequence action, its properties and its user interface controls by creating a managed object format (MOF) file to describe the class. The MOF file is then compiled by using Mofcomp.exe.

For more information about custom action MOF files, see [About the Configuration Manager Custom Action MOF File](about-configuration-manager-custom-action-mof-files.md).

The following procedure adds a class declaration for the custom action that you created in [How to Create a Configuration Manager Custom Action Control](how-to-create-a-configuration-manager-custom-action-control.md).

For information about using the custom action, see [About Configuration Manager Custom Action Client Applications](about-configuration-manager-custom-action-client-applications.md).

### To create a MOF file for a custom action

1. In Notepad, create a new file.
2. Add the following MOF code to the file.

   ```

   #pragma autorecover

   #pragma namespace("\\\\.\\root")

   // SMS Root Storage
   instance of __Namespace
   {
       Name = "SMS";
   };

   #pragma namespace("\\\\.\\root\\SMS")

   // Configuration Manager database name for this computer.
   instance of __Namespace
   {
       Name = "site_REPLACESITECODE";
   };

   #pragma namespace("\\\\.\\root\\SMS\\site_REPLACESITECODE")

   #pragma classflags("forceupdate")

   [   CommandLine("smsswd.exe /run:%1 Application.exe /user:%2"),
       VariablePrefix("MyCustomActionPrefix"),
       ActionCategory("My Custom Action Category,7,1"),
       ActionName{"ConfigMgrTSAction.dll", "ConfigMgrTSAction.Properties.Resources", "ConfigMgrTSAction"},
       ActionUI{"ConfigMgrTSAction.dll", "ConfigMgrTSAction","ConfigMgrTSActionControl",
   "ConfigureTSActionOptions"}
       ]
   class ConfigMgrTSActionControl : SMS_TaskSequence_Action
   {
       [TaskSequencePackage, CommandLineArg(1)]
       string          PackageIDForApplicationExe;

       [Not_Null, CommandLineArg(2)]
       string          User;

       [VariableName("CustomLocation")]
       string          Location;

   };
   ```
3. Replace `REPLACESITECODE` with the site code for your Configuration Manager site.
4. Choose a folder, and save the file as type `All Files` with the name CustomAction.mof.
5. Open a Command Prompt window, navigate to the folder that you saved CustomAction.mof in, and enter the following:

   ```
   mofcomp CustomAction.mof
   ```
6. Press ENTER to compile the CustomAction.mof.
7. Confirm that the class has been added in CIM Studio. The class should be listed as a child class of [SMS_TaskSequence_Action](../reference/osd/sms_tasksequence_action-server-wmi-class.md).
8. Complete [How to Use a Configuration Manager Custom Action Control](how-to-use-a-configuration-manager-custom-action-control.md).

## See Also

[About Configuration Manager Custom Actions](about-configuration-manager-custom-actions.md) [About the Configuration Manager Custom Action MOF File](about-configuration-manager-custom-action-mof-files.md) [How to Create a Configuration Manager Custom Action Control](how-to-create-a-configuration-manager-custom-action-control.md) [About Configuration Manager Custom Action Client Applications](about-configuration-manager-custom-action-client-applications.md)
