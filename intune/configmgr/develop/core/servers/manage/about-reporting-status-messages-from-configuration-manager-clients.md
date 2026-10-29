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
- https://authoring-docs-microsoft.poolparty.biz/devrel/bcbcbad5-4208-4783-8035-8481272c98b8
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
- https://authoring-docs-microsoft.poolparty.biz/devrel/43b2e5aa-8a6d-4de2-a252-692232e5edc8
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/6a8c83be-f1de-4e90-bde0-bd097999a60c
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
