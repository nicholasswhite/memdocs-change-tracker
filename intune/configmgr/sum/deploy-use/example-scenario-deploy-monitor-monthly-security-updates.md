---
title: "Example scenario to deploy and monitor monthly software updates"
description: How to use software updates in Configuration Manager to deploy and monitor monthly software updates.
ms.date: "2019-10-21T00:00:00Z"
ms.topic: install-set-up-deploy
ms.subservice: software-updates
ms.collection: tier3
---

# Example scenario to deploy and monitor monthly software updates

*Applies to: Configuration Manager (current branch)*

This topic provides an example scenario of how you can use software updates in Configuration Manager to deploy and monitor the security software updates that Microsoft releases monthly.

In this scenario, we follow the actions of the Configuration Manager administrator at Woodgrove Bank. The administrator needs to create a software update deployment strategy with the following conditions and requirements:

- Active software update deployment occurs one week after Microsoft releases the security software updates on the second Tuesday of each month. This event is typically referred to as Patch Tuesday.
- Software updates are downloaded and staged on distribution points. Then a deployment is tested to a subset of clients before the ConfigMgr Admin fully deploys the software updates in his production environment.
- The administrator must be able to monitor the software updates' compliance by month or by year.

  This scenario assumes that the software update point infrastructure has already been implemented. Use the following information to plan for and configure software updates in Configuration Manager.

| Process | Reference |
| --- | --- |
| Review the key concepts for software updates. | [Introduction to software updates](../understand/software-updates-introduction.md) |
| Plan for software updates. This information helps you to plan for capacity considerations, determine the software update point infrastructure, software update point installation, synchronization settings, and client settings for software updates. | [Plan for software updates](../plan-design/plan-for-software-updates.md) |
| Configure software updates. This information helps you to install and configure software update points in your hierarchy and helps to configure and synchronize software updates.   In this scenario, our ConfigMgr Admin configures the software updates synchronization schedule to occur on the second Wednesday of each month to ensure that they retrieve the latest security software updates from Microsoft. | [Synchronize software updates](../get-started/synchronize-software-updates.md) |

The following sections in this topic provide example steps to help you to deploy and monitor Configuration Manager security software updates in your organization.

## Step 1: Create a software update group for yearly compliance

The Configuration Manager administrator creates a software update group that can be used to monitor compliance for all of the security software updates that they release in 2016. The admin performs the steps in the following table.

| Process | Reference |
| --- | --- |
| From the **All Software Updates** node in the Configuration Manager console, the Configuration Manager administrator adds criteria to display only security software updates that are released or revised in year 2015 that meet the following criteria:    - **Criteria**: Date Released or Revised - **Condition**: is greater than or equal to specific date **Value**: 1/1/2015 - **Criteria**: Update Classification **Value**: Security Updates - **Criteria**: Expired  **Value**: No | No additional information |
| ConfigMgr Administrator adds all of the filtered software updates to a new software update group with the following requirements:    - **Name**: Compliance Group - Microsoft Security Updates 2015 - **Description**: Software updates | [Add software updates to an update group](add-software-updates-to-an-update-group.md) |

## Step 2: Create an automatic deployment rule for the current month

The Configuration Manager administrator creates an automatic deployment rule for the security software updates that are released by Microsoft for the current month. The admin performs the steps in the following table.

| Process | Reference |
| --- | --- |
| ConfigMgr Admin creates an automatic deployment rule with the following requirements:    1. On the **General** tab, the ConfigMgr Admin configures the following:     - Specifies **Monthly Security Updates** for the name.    - Selects a test collection with limited clients.    - Selects **Create a new Software Update Group**.    - Verifies that **Enable the deployment after this rule is run** is not selected. 2. On the **Deployment Settings** tab, the ConfigMgr Admin selects the default settings. 3. On the **Software Updates** page, the ConfigMgr Admin configures the following property filters and search criteria:     - Date Released or Revised **Last 1 month**.    - Update Classification **Security Updates**. 4. On the **Evaluation** page, the ConfigMgr Admin enables the rule to run on a schedule for the **second Thursday** of every **month**. The ConfigMgr Admin also verifies that his synchronization schedule is set to run on the **second Wednesday** of every **month**. 5. The ConfigMgr Admin uses the default settings on the Deployment Schedule, User Experience, Alerts, and Download Settings pages. 6. On the **Deployment Package** page, the ConfigMgr Admin specifies a new deployment package. 7. The ConfigMgr Admin uses the default settings on the Download Location and Language Selection pages. | [Automatically deploy software updates](automatically-deploy-software-updates.md) |

## Step 3: Verify that software updates are ready to deploy

On the second Thursday of every month, the ConfigMgr Admin verifies that the software updates are ready to deploy. The admin performs the following step.

| Process | Reference |
| --- | --- |
| The ConfigMgr Admin verifies that software updates synchronization completed successfully. | [Software updates synchronization status](monitor-software-updates.md#BKMK_SUSyncStatus) |

## Step 4: Deploy the software update group

After the ConfigMgr Admin verifies that the software updates are ready to deploy, they deploy the software updates. The admin performs the steps in the following table.

| Process | Reference |
| --- | --- |
| The ConfigMgr Admin creates two test deployments for the new software update group. The admin considers the following environments for each deployment:   **Workstation test deployment**: the ConfigMgr Admin considers the following for the workstation test deployment:    - Specifies a deployment collection that contains a subset of workstation clients to verify the deployment. - Configures the deployment settings that are appropriate for the workstation clients in his environment.   **Server test deployment**: the ConfigMgr Admin considers the following for the server test deployment:    - Specifies a deployment collection that contains a subset of server clients to verify the deployment. - Configures the deployment settings that are appropriate for the server clients in his environment. | [Deploy software updates](deploy-software-updates.md) |
| The ConfigMgr Admin verifies that the test deployments have successfully deployed. | [Software updates deployment status](monitor-software-updates.md#BKMK_SUDeployStatus) |
| The ConfigMgr Admin updates the two deployments with new collections that include his production workstations and servers. | No additional information |

## Step 5: Monitor compliance for deployed software updates

The ConfigMgr Admin monitors compliance of his software update deployments. The admin performs the step in the following table.

| Process | Reference |
| --- | --- |
| The ConfigMgr Admin monitors the software updates deployment status in the Configuration Manager console and checks the software update deployment reports available from the console. | [Monitor software updates](monitor-software-updates.md) |

## Step 6: Add monthly software updates to the yearly update group

The ConfigMgr Admin adds the software updates from the monthly software update group to the yearly software update group. The admin performs the step in the following table.

| Process | Reference |
| --- | --- |
| The ConfigMgr Admin selects the software updates from the monthly software update group and adds the software updates to the software updates group that were created for yearly compliance. The admin tracks the software update compliance and creates various reports for his management. | [Add software updates to a deployed update group](add-software-updates-to-an-update-group.md) |

The ConfigMgr Admin has successfully completed his monthly deployment for security software updates. The admin continues to monitor and report on software update compliance to ensure that the clients in his environment are within acceptable compliance levels.

## Recurring monthly process to deploy software updates

After the first month that our ConfigMgr Admin deploys software updates, the admin performs steps three through six to deploy the monthly security software updates released by Microsoft.
