---
title: "Unattended site recovery for Configuration Manager"
description: Use a script to recover your sites in Configuration Manager.
ms.date: "2022-02-16T00:00:00Z"
ms.subservice: core-infra
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

# Unattended site recovery for Configuration Manager

*Applies to: Configuration Manager (current branch)*

To recover a Configuration Manager central administration site (CAS) or primary site without user interaction, create an unattended installation script to use with the `/script` setup command-line option. The script provides the same type of information that the setup wizard prompts for, except that there are no default settings. Specify all values for the setup keys that apply to the type of recovery.

To use the `/script` setup command-line option, first create an answer file. Then specify this file name on the command line. The name of the file is your decision, but it requires the `.ini` file extension. When you reference this answer file from the command line, provide the full path to the file. For example, if your setup answer file is named `setup.ini`, and it's stored in the `C:\setup` folder, your command line would be:

`setup.exe /script c:\setup\setup.ini`

> [!IMPORTANT]
>
> You need **Administrator** rights to run Configuration Manager setup. When you run setup with the unattended script, open the command prompt with the option to **Run as administrator**.

The script contains section names, key names, and values. Required section key names vary depending on the recovery type that you need. The order of the keys within sections and the order of sections within the file aren't important. The keys aren't case-sensitive. When you provide values for keys, the name of the key is followed by an equal sign (`=`) and the value for the key. For example, `Action=RecoverCCAR`.

For more information, see the following articles:

[Command-line options for setup](../deploy/install/command-line-options-for-setup.md)

[Unattended setup script file keys](../deploy/install/command-line-script-file.md)
