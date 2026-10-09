---
title: "About Reporting Status Messages from Configuration Manager Clients"
description: You can raise Configuration Manager client status messages in the Windows event log by using a compiled Managed Object Format (MOF) file on client computers.
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: concept-article
ms.collection: tier3
ms.service: configuration-manager
author: sccmavenger
cmProducts:
- https://authoring-docs-microsoft.poolparty.biz/devrel/2bb407c5-c939-4f7a-9174-27da19279675
- https://authoring-docs-microsoft.poolparty.biz/devrel/bcbcbad5-4208-4783-8035-8481272c98b8
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
- https://authoring-docs-microsoft.poolparty.biz/devrel/43b2e5aa-8a6d-4de2-a252-692232e5edc8
- https://authoring-docs-microsoft.poolparty.biz/devrel/6eda2a8b-e231-4335-b766-c055ea6025a6
---

# About Reporting Status Messages from Configuration Manager Clients

You can raise Configuration Manager client status messages in the Windows event log by using a compiled Managed Object Format (MOF) file on client computers. This can be useful for administrators who are managing servers with System Center Operations Manager. A Configuration Manager status message that is raised by the Configuration Manager client can be caught by the Operations Manager agent on the same computer, which in turn raises an Operations Manager alert for the Configuration Manager status message.

The following example MOF file shows how to raise Configuration Manager program status messages:

```
#pragma namespace("\\\\.\\root\\ccm\\policy\\machine\\requestedconfig")
instance of CCM_EventForwarder_Configuration
{
    InstanceID = "SmsSoftwareDistribution.EventLog";
    Name = "SmsEventLogForwarder";
    PolicyID = "SomePolicyID";
    PolicyInstanceID = "SomePolicyInstance";
    PolicyRuleID = "SomeRuleID";
    PolicySource = "Local";
    PolicyVersion = "1";
        QueryList           = {
                            "SELECT * FROM SoftDistProgramStartedEvent",
                            "SELECT * FROM SoftDistProgramCompletedSuccessfullyEvent",
                            "SELECT * FROM SoftDistProgramCompletedSuccessfulMIFEvent",
                            "SELECT * FROM SoftDistProgramErrorEvent",
                            "SELECT * FROM SoftDistProgramErrorMIFEvent",
                            "SELECT * FROM SoftDistProgramExceededTime",
                            "SELECT * FROM SoftDistProgramPrelimSuccessEvent",
                            "SELECT * FROM SoftDistProgramUnexpectedRebootEvent",
                            "SELECT * FROM SoftDistWarningProgramErrorEvent"
                            };
};
```

## See Also

[About Configuration Manager Status Summarizers](about-configuration-manager-status-summarizers.md)
