---
title: How to create a SQL statement by using query designer
description: How to create Configuration Manager report queries using Query Designer.
ms.date: "2019-04-30T00:00:00Z"
ms.subservice: sdk
ms.topic: how-to


ms.collection: tier3
ms.service: configuration-manager
author: sccmavenger
cmProducts:
- https://authoring-docs-microsoft.poolparty.biz/devrel/cbe4ca68-43ac-4375-aba5-5945a6394c20
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
- https://authoring-docs-microsoft.poolparty.biz/devrel/ced846cc-6a3c-4c8f-9dfb-3de0e90e2742
---

# How to create a SQL statement by using query designer

Query Designer in SQL Server can help you to more easily write SQL queries that can be used in your Configuration Manager reports. Use the following procedures to create Configuration Manager report queries using Query Designer.

## To create a new SQL query in query designer

1. Start Microsoft SQL Server Management Studio.
2. Navigate to *&lt;Computer Name&gt;*�**\ Databases \**�*&lt;Configuration Manager database name&gt;*�**\ Views\*\*.
3. Right-click **Views** and then select **New View**.
4. In the **Add Table** dialog box, select the **Views** tab and then select the views that you want to include in the SQL query.

   > [!NOTE]
   >
   > You can select multiple views by holding down the CTRL key.
5. In the design view of query designer, select the columns you want to appear in the report. If you are querying multiple views, you can join these by selecting a column in one view and dragging this over to the same column in another view.
6. Select **Execute SQL** to test the query and see the results.
7. When you are happy with the results returned by the query, copy and paste it from query designer to be used to create your report in Report Builder.

## See also

[SQL statement reference for Configuration Manager reports](sql-statement-reference-configuration-manager-reports.md)
