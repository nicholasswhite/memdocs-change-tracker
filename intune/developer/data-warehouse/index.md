---
title: "Microsoft Intune Data Warehouse API"
description: You can use the Intune Data Warehouse API to build reports that provide insight into your enterprise mobile environment.
ms.date: "2024-10-30T00:00:00Z"
ms.topic: reference
author: nicholasswhite
cmProducts:
- https://authoring-docs-microsoft.poolparty.biz/devrel/9bdc1705-9b40-49d6-8377-caa0b71fda66
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/1433a524-c01f-4b87-beab-670c040dea4f
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/a72e95ff-4b4f-4cc1-90c6-7dcba67ff05f
manager: laurawi
moniker_range_name: ''
ms.author: nwhite
ms.collection: M365-identity-device-management
ms.reviewer: jamiesil
ms.service: microsoft-intune
ms.subservice: developer
spProducts:
- https://authoring-docs-microsoft.poolparty.biz/devrel/686ed158-d915-41e9-9760-efa46ba88f6d
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/24dc3ccd-591a-4415-a1fe-8759afafcb12
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/312f1f05-a431-4193-8a4d-e6245d5966de
---

# Microsoft Intune Data Warehouse API

The Intune Data Warehouse API lets you access your Intune data in a machine-readable format for use in your favorite analytics tool. You can use the API to build reports that provide insight into your enterprise mobile environment. The API uses the OData protocol, which follows standard patterns for:

- Request and response headers
- Status codes
- HTTP methods
- URL conventions
- Media types
- Payload formats
- Query options

The OData (Open Data Protocol) is an Organization for the Advancement of Structured Information Standards (OASIS) standard that defines the best practice for building and consuming RESTful APIs. The Intune Data Warehouse uses OData version 4.0.

This reference section provides an overview of endpoints, supported HTTP methods, return payload formats, and documentation of the Intune Data Warehouse data model.

> [!IMPORTANT]
>
> You can try out the latest functionality of the Data Warehouse by using the beta version. To use the beta version, your URL must contain the query parameter `api-version=beta`. The beta version offers features before they are made generally available as a supported service. As Intune adds new features, the beta version may change behavior and data contracts. Any custom code or reporting tools dependent on the beta version may break with ongoing updates.

## OData custom client

You can access the Intune Data Warehouse data model through RESTful endpoints. To gain access to your data, your client must authorize with Microsoft Entra ID using OAuth 2.0. You first set up a web app and a client app in Azure, grant permissions to the client. Your local client gets authorization and can then communicate with the Data Warehouse endpoints.

For more information, see [Get data from the Data Warehouse API with a REST client](setup-rest-client.md).

> [!NOTE]
>
> You can access the [GitHub Intune Data Warehouse repo](https://github.com/Microsoft/Intune-Data-Warehouse) on Github for code samples.

## Interacting with the API

The API requires authorization with Microsoft Entra ID. Microsoft Entra ID uses OAuth 2.0. Once authorized, you can get data from the API using an HTTP GET verb and contacting the exposed entity collections. For details see:

- [Authorization](ref-api-endpoints.md#authorization)
- [API URL Structure](ref-api-endpoints.md#api-url-structure)

## Intune Data Warehouse data model

OData defines an abstract data model and a protocol that let any client access information exposed by any data source. The data model documentation topic contains an explanation of the namespaces, entities, and return objects in the Intune Data Warehouse data model. For more information, see [Data Warehouse Data Model](ref-data-model.md).

## Next steps

Learn more about working with Microsoft Entra ID by reading the [Authentication Scenarios for Microsoft Entra ID](https://learn.microsoft.com/en-us/azure/active-directory/develop/active-directory-authentication-scenarios).

Find OData resources at [odata.org](https://www.odata.org).

Review the OData Version 4.0 standard at [OData Version 4.0](https://docs.oasis-open.org/odata/odata/v4.0/odata-v4.0-part1-protocol.html).
