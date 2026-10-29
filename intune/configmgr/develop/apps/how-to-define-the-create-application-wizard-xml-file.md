---
title: How to Define the Create Application Wizard XML File
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: how-to
ms.collection: tier3
description: How to create a custom deployment technology XML File for the Create Application Wizard/.
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
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/a72e95ff-4b4f-4cc1-90c6-7dcba67ff05f
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/e10a756b-c002-4cbb-8cf6-f0fab0633697
spProducts:
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/24dc3ccd-591a-4415-a1fe-8759afafcb12
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/3a741da3-90b9-472d-8fd6-830aafecaac8
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/6a8c83be-f1de-4e90-bde0-bd097999a60c
---

# How to Define the Create Application Wizard XML File

To define the custom deployment technology XML file, create an XML file based on the `https://schemas.microsoft.com/SystemsManagementServer/2005/03/ConsoleFramework` schema. The XML file for the Create Application Wizard should be named, CreateApp_&lt;*TechnologyID*&gt;.xml.

### To define the create application wizard XML file

1. Create a Create Application Wizard XML file.

   The following example from the RDP sample project shows how to define the Create Application Wizard XML file. Wizards aren't extensible for the UI. However, by creating this custom deployment technology XML, the contents of the wizard now include the ability to create an RDP deployment type.

   ```xml
   <?xml version="1.0" encoding="utf-8"?>
   <SmsFormData xmlns="https://schemas.microsoft.com/SystemsManagementServer/2005/03/ConsoleFramework" FormatVersion="1">
     <Form Id="{FD19DEC6-81ED-447B-9D88-3AAD7DE499F1}" CustomData="CreateApp" FormType="PropertySheet" ForceRefresh="true">
       <Pages>
         <Page Assembly="AdminUI.DeploymentType.Rdp.dll" Namespace="RdpTechnology.AdminConsole" VendorId="Partner Company Name" Id="{6802BC91-30EF-49A5-80F6-D4902CD5181C}" Type="RdpDeploymentTechnologyPageControl" />
       </Pages>
     </Form>
   </SmsFormData>
   ```

## See Also

[Configuration Manager Reference](../reference/configuration-manager-reference.md)
