<!-- loio75d55b7c8488424cb9b8a9c14c6eae09 -->

# Configuring Own Business System ID

***before* ** To use the SOAP APIs for business partners, you need to configure the business system ID for the SAP Master Data Integration tenant. If you do not use the SOAP APIs for business partners, you do not need to perform this configuration. The business system ID serves as an identifier for the SAP Master Data Integration tenant in SOAP replication use cases. This step is a one time activity per tenant and must be carried outdata replication via SOAP. SAP Master Data Integration does not support updates of the Business System ID once replication has started.

> ### Note:  
> `BusinessConfigurationAdmin` [Authorization of Business Users](authorization-for-business-users-1e7e229.md) Users performing this operation need to have the role. Refer to.



<a name="loio75d55b7c8488424cb9b8a9c14c6eae09__procedure"/>

## Procedure

Own business system ID of a tenant can be maintained using the SAP Master Data Orchestration UI or Generic Configuration API.

For choosing a business system ID, we recommend the following:

> ### Note:  
> You cannot change the business system ID in SAP Master Data Orchestration once it is set and the replication has started. Changing the business system ID after the replication started can lead to inconsistencies. Therefore, SAP Master Data Integration does not support updating the business system ID after the replication started.

-   The value can have length of up to 60 characters. Only alphanumeric values with underscores and hyphens are permitted.

-   `"identityzone"` [Service Instance in SAP Master Data Integration](connecting-applications-via-service-instances-e01bb46.md#loioe01bb46b7e09427aa37ac2da40198cf2__create-a-service-instance) The value can be set aspresent in service keys of SAP Master Data Integration service instance, referon how to create an instance. However, this is not mandatory.

-   The value maintained in this configuration should match with:

    -   [DRF Configuration](../integration/integrating-with-sap-s-4hana-on-premise-adbf8ef.md#loioadbf8efbda2e4514b7f2776a9eb879c7__data-replication-framework-customizing) Business system name configured in DRF when connecting SAP S/4HANA \(on premise\) with SOAP APIs for business partners of SAP Master Data Integration. For more information, refer to.

    -   [SAP Note 3087667](http://help.sap.com/disclaimer?site=https://launchpad.support.sap.com/#/notes/3087667) Business system name configured in Communication System UI when connecting SAP S/4HANA Cloud with SOAP APIs for business partners of SAP Master Data Integration. For more information, refer to.

    -   `RecipientBusinessSystemID` in the SOAP payload sent from client to SAP Master Data Integration.





<a name="loio75d55b7c8488424cb9b8a9c14c6eae09__using-master-data-orchestration-ui"/>

## Using Master Data Orchestration UI

1.  **Instances and Subscriptions** **Subscriptions** **Master Data Integration \(Orchestration\)** Go toin your Subaccount. Under, click on.

2.  **Go to Application** Select. This will open the Fiori Launchpad for SAP Master Data Orchestration.

3.  **Configure Master Data Integration** [Configure Business System Name](https://help.sap.com/docs/SAP_MASTER_DATA_INTEGRATION/8ce78b673ef04cc1bcfeb01c93ef7885/2efb0f9407eb49a381a0e70e0311ab36.html) Go tosection and selecttile.

4.  `Create` Click onbutton and maintain the desired name of your choice.

5.  **Configure Master Data Integration** [Configure SOAP Replication](https://help.sap.com/docs/SAP_MASTER_DATA_INTEGRATION/8ce78b673ef04cc1bcfeb01c93ef7885/7d72e4afac074ed09533bbe83470dc77.html) Go tosection and selecttile.

6.  Select the business system maintained in the step before and enable SOAP replication.




<a name="loio75d55b7c8488424cb9b8a9c14c6eae09__using-the-api"/>

## Using the API

**POST** Send arequest using the below information.

**URL** :

**Authorization** `Bearer Token` [Authentication of Business Users](authentication-of-business-users-ef53987.md) : Chooseas Type and provide the access token. Refer toto generate access token.

**Payload** `content-type` `application/json` `<Business System Name>` *Sample Payload* : For the request body, setheader as. Use thebelow and replacewith the desired name of your choice :

`201 Created` Ensure thatresponse is received for your POST call.

```
<BASE_URL>/businesspartner/v0/odata/API_GENERIC_CONFIGURATIONS/GenericConfigurations
```

```
{
				"ConfigurationName": "Business System",
				"ConfigurationValue": "<Business System Name>"
				}
```

> ### Note:  
> `<BASE_URL>` `"uri"` [Service Instance in MDI](connecting-applications-via-service-instances-e01bb46.md) can be fetched frompresent in service keys of service instance, created as part of.



<a name="loio75d55b7c8488424cb9b8a9c14c6eae09__updating-the-business-system-id"/>

## Updating the Business System ID

-   Changing the business system ID of a tenant is only possible as long as no business partner data has been replicated to MDI.

-   **using Master Data Orchestration UI** [Configure Business System Name](https://help.sap.com/docs/SAP_MASTER_DATA_INTEGRATION/8ce78b673ef04cc1bcfeb01c93ef7885/2efb0f9407eb49a381a0e70e0311ab36.html) Update of the Business System ID valueis possible using thetile.

-   [Configure SOAP Replication](https://help.sap.com/docs/SAP_MASTER_DATA_INTEGRATION/8ce78b673ef04cc1bcfeb01c93ef7885/7d72e4afac074ed09533bbe83470dc77.html) **Activated** Onceisbusiness system ID value can no longer be edited.


