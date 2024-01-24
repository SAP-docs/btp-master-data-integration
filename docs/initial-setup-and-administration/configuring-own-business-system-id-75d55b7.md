<!-- loio75d55b7c8488424cb9b8a9c14c6eae09 -->

# Configuring Own Business System ID

To use the SOAP APIs for business partners, you need to configure the business system ID for the SAP Master Data Integration tenant. If you do not use the SOAP APIs for business partners, you do not need to perform this configuration. The business system ID serves as an identifier for the SAP Master Data Integration tenant in SOAP replication use cases. This step is a one time activity per tenant and must be carried out ***before* ** data replication via SOAP. SAP Master Data Integration does not support updates of the Business System ID once replication has started.

> ### Note:  
> Users performing this operation need to have the role `BusinessConfigurationAdmin` . Refer to [Authorization of Business Users](authorization-for-business-users-1e7e229.md) .



<a name="loio75d55b7c8488424cb9b8a9c14c6eae09__procedure"/>

## Procedure

Own business system ID of a tenant can be maintained using the SAP Master Data Orchestration UI or Generic Configuration API.

> ### Note:  
> You cannot change the business system ID in SAP Master Data Orchestration once it is set and the replication has started. Changing the business system ID after the replication started can lead to inconsistencies. Therefore, SAP Master Data Integration does not support updating the business system ID after the replication started.

For choosing a business system ID, we recommend the following:

-   The value can have length of up to 60 characters. Only alphanumeric values with underscores and hyphens are permitted.

-   The value can be set as `"identityzone"` present in service keys of SAP Master Data Integration service instance, refer [Service Instance in SAP Master Data Integration](connecting-applications-via-service-instances-e01bb46.md#loioe01bb46b7e09427aa37ac2da40198cf2__create-a-service-instance) on how to create an instance. However, this is not mandatory.

-   The value maintained in this configuration should match with:

    -   Business system name configured in DRF when connecting SAP S/4HANA \(on premise\) with SOAP APIs for business partners of SAP Master Data Integration. For more information, refer to [DRF Configuration](../integration/integrating-with-sap-s-4hana-on-premise-adbf8ef.md#loioadbf8efbda2e4514b7f2776a9eb879c7__data-replication-framework-customizing) .

    -   Business system name configured in Communication System UI when connecting SAP S/4HANA Cloud with SOAP APIs for business partners of SAP Master Data Integration. For more information, refer to [SAP Note 3087667](http://help.sap.com/disclaimer?site=https://launchpad.support.sap.com/#/notes/3087667) .

    -   `RecipientBusinessSystemID` in the SOAP payload sent from client to SAP Master Data Integration.





<a name="loio75d55b7c8488424cb9b8a9c14c6eae09__using-master-data-orchestration-ui"/>

## Using Master Data Orchestration UI

1.  Go to **Instances and Subscriptions** in your Subaccount. Under **Subscriptions** , click on **Master Data Integration \(Orchestration\)** .

2.  Select **Go to Application** . This will open the Fiori Launchpad for SAP Master Data Orchestration.

3.  Go to **Configure Master Data Integration** section and select [Configure Business System Name](https://help.sap.com/docs/SAP_MASTER_DATA_INTEGRATION/8ce78b673ef04cc1bcfeb01c93ef7885/2efb0f9407eb49a381a0e70e0311ab36.html) tile.

4.  Click on `Create` button and maintain the desired name of your choice.

5.  Go to **Configure Master Data Integration** section and select [Configure SOAP Replication](https://help.sap.com/docs/SAP_MASTER_DATA_INTEGRATION/8ce78b673ef04cc1bcfeb01c93ef7885/7d72e4afac074ed09533bbe83470dc77.html) tile.

6.  Select the business system maintained in the step before and enable SOAP replication.




<a name="loio75d55b7c8488424cb9b8a9c14c6eae09__using-the-api"/>

## Using the API

Send a **POST** request using the below information.

**URL** :

```
<BASE_URL>/businesspartner/v0/odata/API_GENERIC_CONFIGURATIONS/GenericConfigurations
```

> ### Note:  
> `<BASE_URL>` can be fetched from `"uri"` present in service keys of service instance, created as part of [Service Instance in MDI](connecting-applications-via-service-instances-e01bb46.md) .

**Authorization** : Choose `Bearer Token` as Type and provide the access token. Refer to [Authentication of Business Users](authentication-of-business-users-ef53987.md) to generate access token.

**Payload** : For the request body, set `content-type` header as `application/json` . Use the *Sample Payload* below and replace `<Business System Name>` with the desired name of your choice :

```
{
				"ConfigurationName": "Business System",
				"ConfigurationValue": "<Business System Name>"
				}
```

Ensure that `201 Created` response is received for your POST call.



<a name="loio75d55b7c8488424cb9b8a9c14c6eae09__updating-the-business-system-id"/>

## Updating the Business System ID

-   Changing the business system ID of a tenant is only possible as long as no business partner data has been replicated to MDI.

-   Update of the Business System ID value **using Master Data Orchestration UI** is possible using the [Configure Business System Name](https://help.sap.com/docs/SAP_MASTER_DATA_INTEGRATION/8ce78b673ef04cc1bcfeb01c93ef7885/2efb0f9407eb49a381a0e70e0311ab36.html) tile.

-   Once [Configure SOAP Replication](https://help.sap.com/docs/SAP_MASTER_DATA_INTEGRATION/8ce78b673ef04cc1bcfeb01c93ef7885/7d72e4afac074ed09533bbe83470dc77.html) is **Activated** business system ID value can no longer be edited.


