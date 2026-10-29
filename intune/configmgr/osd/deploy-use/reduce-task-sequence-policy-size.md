---
title: "Reduce the size of task sequence policy"
description: When the size of the task sequence policy exceeds 32 MB, the client fails to process the large policy. The client then fails to run the task sequence deployment. Manage the size of task sequence policy to reduce deployment failures.
ms.date: "2022-04-08T00:00:00Z"
ms.subservice: osd
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
spProducts:
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/24dc3ccd-591a-4415-a1fe-8759afafcb12
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/6a8c83be-f1de-4e90-bde0-bd097999a60c
cmProducts:
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/4c50f262-d533-4ba4-9d4a-08899ec3a3d1
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/a72e95ff-4b4f-4cc1-90c6-7dcba67ff05f
---

# Reduce the size of task sequence policy

*Applies to: Configuration Manager (current branch)*

When the size of the task sequence policy exceeds 32 MB, the client fails to process the large policy. The client then fails to run the task sequence deployment. The size of the task sequence as stored in the site database is smaller, but can still cause problems if too large. When the client processes the entire task sequence policy, the expanded size can cause problems over 32 MB.

To check for the 32-MB task sequence policy size on clients, use [management insights](../../core/servers/manage/management-insights.md#operating-system-deployment).

Configuration Manager restricts the following actions for a task sequence in the site database that's greater than 2 MB in size:

- Save changes in the task sequence editor
- Save changes with PowerShell cmdlets
- Import a new task sequence
- Any other change using supported SDK methods

For example, if you try to save changes to a large task sequence, the task sequence editor will display an error.

> [!TIP]
>
> The behavior in version 2010 and later checks for the 2 MB size limit on the task sequence as stored in the site database. When the client processes the entire task sequence policy, the expanded size can cause problems over 32 MB. The management insights check for the 32 MB task sequence policy size.

When you view the list of task sequences in the Configuration Manager console, add the **Size (KB)** column. Use this column to identify large task sequences that can cause problems.

## Actions to reduce task sequence size

To help reduce the size of task sequences and task sequence deployment policies, take the following actions:

- Separate functional segments into child task sequences, and use the [Run Task Sequence](../understand/task-sequence-steps.md#child-task-sequence) step. Keep each task sequence less than 2 MB in the database. Each task sequence has a separate 32-MB limit on its policy size.

  > [!NOTE]
  >
  > Reducing the total number of steps and groups in a task sequence has minimal impact on the policy size. Each step is generally a couple of KB in policy. Moving groups of steps to a child task sequence is more impactful.
- Reduce the number of software updates in deployments to the same collection as the task sequence.
- Instead of entering a script in the [Run PowerShell Script](../understand/task-sequence-steps.md#BKMK_RunPowerShellScript) step, reference it via a package.
- There's an 8-KB limit on the size of the task sequence *environment* when it runs. Review the usage of custom task sequence variables, which can also contribute to the policy size.
- As a last resort, split a complex, dynamic task sequence into separate task sequences with distinct deployments to different collections.

## Next steps

[Export and import task sequences](export-import-task-sequences.md)
