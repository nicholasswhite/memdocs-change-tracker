---
title: "How to Create a Deployment Template"
description: Create a software updates deployment template in Configuration Manager by creating an instance of the SMS_Template class and populating the properties.
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: how-to
ms.collection: tier3
ms.service: configuration-manager
---

# How to Create a Deployment Template

You create a software updates deployment template, in Configuration Manager, by creating an instance of the `SMS_Template` class and populating the properties.

### To create a deployment template

1. Set up a connection to the SMS Provider.
2. Create the new template object by using the `SMS_Template` class.
3. Populate the new template properties.
4. Save the new template and properties.

## Example

The following example method shows how to create a software updates deployment template by using the `SMS_Template` class and class properties.

For information about calling the sample code, see [Calling Configuration Manager Code Snippets](../core/understand/calling-code-snippets.md).

> [!NOTE]
>
> In the following code examples, the template settings are passed into the method by using a string variable called deploymentTemplateSettings. The template settings are stored in an XML structure.

VB Template Setting Example (one long string):

```xml
deploymentTemplateSettings = "<TemplateDescription xmlns:xsi=""http://www.w3.org/2001/XMLSchema-instance"" xmlns:xsd=""http://www.w3.org/2001/XMLSchema""> <CollectionId>SMS00001</CollectionId> <IncludeSub>true</IncludeSub> <AttendedInstall>true</AttendedInstall> <UTC>true</UTC> <Duration>2</Duration> <DurationUnits>Weeks</DurationUnits> <SuppressServers>Unchecked</SuppressServers> <SuppressWorkstations>Unchecked</SuppressWorkstations> <AllowRestart>false</AllowRestart> <Deploy2003>true</Deploy2003> <CollectImmediately>false</CollectImmediately> <LocalDPOption>DownloadAndInstall</LocalDPOption> <RemoteDPOption>DownloadAndInstall</RemoteDPOption> <DisableMomAlert>false</DisableMomAlert> <GenerateMomAlert>false</GenerateMomAlert> <UseRemoteDP>false</UseRemoteDP> <UseUnprotectedDP>false</UseUnprotectedDP> </TemplateDescription>"
```

C# Template Setting Example (the same template settings and still passed as a string, but the XML structure is more obvious):

```xml
string deploymentTemplateSettings =
  @"<TemplateDescription xmlns:xsi=""http://www.w3.org/2001/XMLSchema-instance"" xmlns:xsd=""http://www.w3.org/2001/XMLSchema"">
  <CollectionId>SMS00001</CollectionId>
  <IncludeSub>true</IncludeSub>
  <AttendedInstall>true</AttendedInstall>
  <UTC>true</UTC>
  <Duration>2</Duration>
  <DurationUnits>Weeks</DurationUnits>
  <SuppressServers>Unchecked</SuppressServers>
  <SuppressWorkstations>Unchecked</SuppressWorkstations>
  <AllowRestart>false</AllowRestart>
  <Deploy2003>true</Deploy2003>
  <CollectImmediately>false</CollectImmediately>
  <LocalDPOption>DownloadAndInstall</LocalDPOption>
  <RemoteDPOption>DownloadAndInstall</RemoteDPOption>
  <DisableMomAlert>false</DisableMomAlert>
  <GenerateMomAlert>false</GenerateMomAlert>
  <UseRemoteDP>false</UseRemoteDP>
  <UseUnprotectedDP>false</UseUnprotectedDP>
  </TemplateDescription>";
```

```vbs

Sub CreateSUMDeploymentTemplate(connection,              _
                                 newTemplateName,         _
                                 newTemplateDescription,  _
                                 newTemplateSettings,     _
                                 newTemplateType)

    ' Create the new Template object.
    Set newSUMTemplate = connection.Get("SMS_Template").SpawnInstance_

    ' Populate the SMS_Template properties.
    ' Note: The template name (newTemplateName) must be unique.
    newSUMTemplate.Name = newTemplateName
    newSUMTemplate.Description = newTemplateDescription
    newSUMTemplate.Data = newTemplateSettings
    newSUMTemplate.Type = newTemplateType

    ' Save the new template and properties.
    newSUMTemplate.Put_

    ' Output the new template name.
    Wscript.Echo "Created new template: " & newTemplateName

 End Sub

```

```c#

public void CreateSUMDeploymentTemplate(WqlConnectionManager connection,
                                        string newTemplateName,
                                        string newTemplateDescription,
                                        string newTemplateSettings,
                                        int newTemplateType)
{
    try
    {
        // Create the template object.
        IResultObject newSUMTemplate = connection.CreateInstance("SMS_Template");

        // Populate the new template properties.
        // Note: The template name (newTemplateName) must be unique.
        newSUMTemplate["Name"].StringValue = newTemplateName;
        newSUMTemplate["Description"].StringValue = newTemplateDescription;
        newSUMTemplate["Data"].StringValue = newTemplateSettings;
        newSUMTemplate["Type"].IntegerValue = newTemplateType;

        // Save the new template and the new template properties.
        newSUMTemplate.Put();

        // Output the new template name.
        Console.WriteLine("Created template: " + newTemplateName);
    }

    catch (SmsException ex)
    {
        Console.WriteLine("Failed to create template. Error: " + ex.Message);
        throw;
    }
}

```

This example method has the following parameters:

| Parameter | Type | Description |
| --- | --- | --- |
| `connection` | - Managed: `WqlConnectionManager` - VBScript: [SWbemServices](https://learn.microsoft.com/en-us/windows/win32/wmisdk/swbemservices) | A valid connection to the SMS Provider. |
| `newTemplateName` | - Managed: `String` - VBScript: `String` | The new template name. The template name must be unique. |
| `newTemplateDescription` | - Managed: `String` - VBScript: `String` | The description for the new template. |
| `newTemplateSettings` | - Managed: `String` - VBScript: `String` | The new template settings. The settings are in an XML structure, stored as a string.    - **CollectionId**   The collection for the software update deployment.     - A valid collection ID. - **IncludeSub**   Include members of subcollections.     - `true`   - `false` - **AttendedInstall**   Display software update notifications on clients (false will suppress notifications).     - `true`   - `false` - **UTC**   Use Coordinated Universal Time (UTC) instead of client local time.     - `true`   - `false` - **Duration**   Duration of the deployment.     - 1-24 (hours)   - 1-365 (days)   - 1-4 (weeks)   - 1-12 (months) - **DurationUnits**   Duration units.     - hours   - days   - weeks   - months - **SuppressServers**   Suppress the system restart on servers.     - Checked   - Unchecked - **SuppressWorkstations**   Suppress the system restart on workstations.     - Checked   - Unchecked - **AllowRestart**   Allow system restart outside of maintenance windows (for both servers and workstations).     - `true`   - `false` - **Deploy2003**   Deploy software updates to SMS 2003 clients.     - `true`   - `false` - **CollectImmediately** (SMS 2003 client specific)   Collect hardware inventory immediately after installing software updates.     - `true`   - `false` - **LocalDPOption** (SMS 2003 client specific)   Specify whether to download the update source files before running the installation when a distribution point is available locally.     - DownloadAndInstall   - InstallFromDP - **RemoteDPOption** (SMS 2003 client specific)   Specify whether to download the update source files before running the installation when no distribution point is available locally.     - DownloadAndInstall   - InstallFromDP - **DisableMomAlert**   Disable Operations Manager alerts while software updates run.     - `true`   - `false` - **GenerateMomAlert**   Generate Operations Manager alert when a software update installation fails.     - `true`   - `false` - **UseRemoteDP**   Download software updates from use a remote distribution point (even when a client is connected within a slow or unreliable network boundary).     - `true`   - `false` - **UseUnprotectedDP**   Download software updates from a unprotected distribution point (when updates are not available from any protected distribution point).     - `true`   - `false` |
| `newTemplateType` | - Managed: `Integer` - VBScript: `Integer` | The new template type. Currently the only possible value is:   - `0` (SUM_DEPLOYMENT) |

## Compiling the Code

This C# example requires:

### Namespaces

System

System.Collections.Generic

System.Text

Microsoft.ConfigurationManagement.ManagementProvider

Microsoft.ConfigurationManagement.ManagementProvider.WqlQueryEngine

### Assembly

adminui.wqlqueryengine

microsoft.configurationmanagement.managementprovider

## Robust Programming

For more information about error handling, see [About Configuration Manager Errors](../core/understand/about-configuration-manager-errors.md).

## .NET Framework Security

For more information about securing Configuration Manager applications, see [Configuration Manager role-based administration](../core/servers/configure/role-based-administration.md).

## See Also

[About software update deployments](about-software-updates-deployments.md) [How to Assign a Package to a Distribution Point](../core/servers/configure/how-to-assign-a-package-to-a-distribution-point.md) [SMS_Template](../reference/sum/sms_template-server-wmi-class.md)
