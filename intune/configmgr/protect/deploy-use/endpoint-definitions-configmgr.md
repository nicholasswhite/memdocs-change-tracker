---
title: "Use Configuration Manager to deliver definition updates"
description: Learn to configure Configuration Manager software updates to deliver definition updates to client computers.
ms.date: "2020-04-23T00:00:00Z"
ms.subservice: protect
ms.topic: how-to
ms.collection: tier3
ms.service: configuration-manager
author: sccmavenger
cmProducts:
- https://authoring-docs-microsoft.poolparty.biz/devrel/bcbcbad5-4208-4783-8035-8481272c98b8
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/12ed19f9-ebdf-4c8a-8bcd-7a681836774d
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
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/3a764584-4f97-452b-8f1d-36f19b12f6ae
---

# Use Configuration Manager to deliver definition updates

*Applies to: Configuration Manager (current branch)*

You can configure Configuration Manager software updates to automatically deliver definition updates to client computers. Before you begin to create automatic deployment rules, make sure to configure Configuration Manager software updates. For more information, see [Introduction to software updates](../../sum/understand/software-updates-introduction.md).

> [!NOTE]
>
> This procedure is specific to Endpoint Protection. For more general information about automatic deployment rules, see [Automatically deploy software updates](../../sum/deploy-use/automatically-deploy-software-updates.md).

1. In the Configuration Manager console, go to the **Software Library** workspace. Expand **Software Updates**, and then select **Automatic Deployment Rules**.
2. On the **Home** tab of the ribbon, in the **Create** group, select **Create Automatic Deployment Rule**.
3. On the **General** page of the **Create Automatic Deployment Rule Wizard**, specify the following information:

   - **Name**: Enter a unique name for the automatic deployment rule.
   - **Collection**: Select the device collection to which you want to deploy definition updates.

     > [!NOTE]
     >
     > You can't deploy definition updates to a user collection.
4. Select **Add to an existing Software Update Group**.
5. Select **Enable the deployment after this rule is run**.
6. On the **Deployment Settings** page of the wizard, for the **Detail level**, select **Only error messages**.

   > [!NOTE]
   >
   > When you select **Only error messages**, it reduces the number of state messages that the definition deployment sends. This configuration helps reduce the CPU processing on the Configuration Manager servers.
7. On the **Software Updates** page:

   1. Select the **Update Classification** property filter. In the **Search criteria** list, select **&lt;items to find&gt;**.

      In the **Search Criteria** window, select **Definition Updates**, then select **OK**.
   2. Select the **Product** property filter. In the **Search criteria** list, select **&lt;items to find&gt;**.

      In the **Search Criteria** window, select **System Center Endpoint Protection** for Windows 8.1 and earlier or **Windows Defender** for Windows 10 and later, then select **OK**.

   > [!NOTE]
   >
   > Optionally, you can filter out superseded updates. Select the **Superseded** property filter. In the **Search criteria** list, select **&lt;items to find&gt;**. In the **Search Criteria** window, select **No**, then select **OK**.
8. On the **Evaluation Schedule** page of the wizard, select **Run the rule after any software update point synchronization**.
9. On the **Deployment Schedule** page of the wizard, configure the following settings:

   - **Time based on**: If you want all clients to install the latest definitions at the same time, select **UTC**. The actual installation time will vary within two hours.
   - **Software available time**: Specify the available time for the deployment that this rule creates. The specified time must be at least one hour after the automatic deployment rule runs. This configuration makes sure that the content has sufficient time to replicate to the distribution points. Some definition updates might also include antimalware engine updates, which might take longer to reach distribution points.
   - **Installation deadline**: Select **As soon as possible**.

     > [!NOTE]
     >
     > Software update deadlines vary over a two-hour period. This behavior prevents all clients from requesting an update at the same time.
10. On the **User Experience** page of the wizard, for **User notifications**, select **Hide in Software Center and all notifications**. With this configuration, the definition updates install silently.
11. On the **Deployment Package** page of the wizard, select an existing deployment package or create a new one.

    > [!NOTE]
    >
    > Consider placing definition updates in a package that doesn't contain other software updates. This strategy keeps the size of the definition update package smaller, which allows it to replicate to distribution points more quickly.
12. If you create a new deployment package, on the **Distribution Points** page of the wizard, select one or more distribution points. The site copies the content for this package to these distribution points.
13. On the **Download Location** page, select **Download software updates from the Internet**.
14. On the **Language Selection** page, select each language version of the updates to download.
15. On the **Download Settings** page, select the necessary software updates download behavior.
16. Complete the wizard.

Verify that the **Automatic Deployment Rules** node of the Configuration Manager console displays the new rule.

[Create and deploy antimalware policies](endpoint-antimalware-policies.md)
