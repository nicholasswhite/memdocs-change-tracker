---
title: How to Define the Create Deployment Type Wizard XML File
description: To define the custom create deployment type wizard XML file, create an XML file based on the schema.
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: how-to
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
cmProducts:
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/4c50f262-d533-4ba4-9d4a-08899ec3a3d1
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/a72e95ff-4b4f-4cc1-90c6-7dcba67ff05f
spProducts:
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/24dc3ccd-591a-4415-a1fe-8759afafcb12
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/6a8c83be-f1de-4e90-bde0-bd097999a60c
---

# How to Define the Create Deployment Type Wizard XML File

To define the custom create deployment type wizard XML file, create an XML file based on the `https://schemas.microsoft.com/SystemsManagementServer/2005/03/ConsoleFramework` schema. The XML file for the Create Application Wizard should be named CreateDeploymentWizard_&lt;*TechnologyID*&gt;.xml.

### To define the create deployment type wizard XML file

1. Create a Create Deployment Type Wizard XML file.

   The following example from the RDP sample project demonstrates how to define the Deployment Type Wizard XML file.

   ```xml
   <?xml version="1.0" encoding="utf-8"?>
   <SmsFormData xmlns="https://schemas.microsoft.com/SystemsManagementServer/2005/03/ConsoleFramework" FormatVersion="1">
     <Form Id="{FD19DEC6-81ED-447B-9D88-3AAD7DE499F1}" CustomData="CreateDT" FormType="PropertySheet" ForceRefresh="true">
       <Pages>
         <Page Assembly="AdminUI.DeploymentType.Rdp.dll" Namespace="RdpTechnology.AdminConsole" VendorId="Partner Company Name" Id="{6802BC91-30EF-49A5-80F6-D4902CD5181C}" Type="RdpDeploymentTechnologyPageControl" />
       </Pages>
     </Form>
   </SmsFormData>
   ```

## See Also

[Configuration Manager Reference](../reference/configuration-manager-reference.md)
