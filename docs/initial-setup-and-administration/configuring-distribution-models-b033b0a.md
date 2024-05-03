<!-- loiob033b0a713984a7d85bbb79b426d40d9 -->

# Configuring Distribution Models

Use Business Data Orchestration for configuring distribution models. For more information on Business Data Orchestration, refer to [Subscription Process for Business Data Orchestration](https://help.sap.com/viewer/8ce78b673ef04cc1bcfeb01c93ef7885/CLOUD/en-US/f3fc55879f8342ee9fbafda37db36019.html) 

> ### Note:  
> SAP Master Data Integration offers SOAP APIs for the integration of the Business Partner object in addition to the generic REST APIs. Refer to the documentation of the respective integrating application to identify the underlying APIs used for the integration. The specifics for the Business Partner distribution models are shown below.



<a name="loiob033b0a713984a7d85bbb79b426d40d9__configuring-sap-master-data-integration--business-partners-for-rest-scenario"/>

## Configuring SAP Master Data Integration — Business Partners for REST Scenario



<a name="loiob033b0a713984a7d85bbb79b426d40d9__configuring-business-partner-and-bp-relationship-distribution-model"/>

## Configuring Business Partner and BP Relationship Distribution Model

In order to avoid replication failures, a BP Relationship distribution model must always accompany a business partner distribution model. The failures can occur as referenced business partners because they are not replicated beforehand to the consumers. To avoid replication failures through missing business partners, it is recommended to restrict the use of filter criteria for object selection accordingly.

> ### Note:  
> These are the key activation and deactivation procedures to avoid replication failures: **Activation** : The BP Relationship distribution model can only be activated in case a Business Partner distribution model is already active for the same connection.
> 
> **Deactivation** : The Business Partner distribution model can only be deactivated if there is no active BP Relationship distribution model for the same connection.
> 
> 1.  “Connection” here is mentioned as the combination of provider and consumer in the distribution models.
> 
> 2.  This is relevant for business partner replication via REST in both directions \(from and to SAP Master Data Integration\).



<a name="loiob033b0a713984a7d85bbb79b426d40d9__configuring-sap-master-data-integration--business-partners-for-soap-scenario"/>

## Configuring SAP Master Data Integration — Business Partners for SOAP Scenario

Follow the steps to configure the distribution model, which will be used to replicate the Business Partners from the SAP Master Data Integration service to connected clients.

For more information refer to [Maintenance of the Distribution Model in Business Data Orchestration](https://help.sap.com/docs/SAP_MASTER_DATA_INTEGRATION/8ce78b673ef04cc1bcfeb01c93ef7885/ef9398e6f60a44568d106f71ea4d5cfa.html) .

-   Go to **Instances and Subscriptions** in your Subaccount. Under **Subscriptions** , click on **Master Data Integration \(Orchestration\)** .

-   Select **Go to Application** . This will open the Fiori Launchpad for Business Data Orchestration service application.


Go to **Manage Master Data Orchestration** section and select **Manage Distribution Model** tile.

-   Click **Create** .

-   Provide a name in the **Model** field.

-   In Provider section, click **Create** .

    -   For the provider Business System, click on the value help and select **SAP Master Data Integration** from the **Business System** column.


-   In **Consumer** section, click **Create** .

    -   For the consumer Business System, click on the value help and select the `businessSystemId` for the business system for which the distribution model is being created. The `businessSystemId` , which was used while creating the service instance will appear here. For more information, see [Connecting applications via service instance](connecting-applications-via-service-instances-e01bb46.md) .


-   Select the below value in the **Parameters** section:

    -   Select **Business Partner \(sap.odm.businesspartner.BusinessPartner\)** from **Business Object Type** dropdown field.

    -   Add a relevant number to define the **Package Size** as per your requirement. Recommendation is not to exceed above 50.

    -   For **API** field, select **MDI\_SOAP\_BUSINESS\_PARTNER** 

    -   Select a relevant option for **Recurrence Pattern** under **Scheduling Information** 



> ### Note:  
> The business system you select here is where the data gets distributed. For the consumer system selected above, ensure that below destinations based on the integration scenario are created on SAP BTP Cockpit.
> 
> -   `<businessSystemId>_BPOUTBOUND` 
> 
> -   `<businessSystemId>_BPRELOUTBOUND` 
> 
> -   `<businessSystemId>_KMOUTBOUND` 

-   Optionally, you can set **Data Filters** under **Object Selection** section if applicable.

    **Object Selection Filters** These are the object selection filters supported by SAP Master Data Integration - Business Partners:

    -   `BusinessPartner.authorizationGroup.code` 

    -   `BusinessPartner.addressData.personPostalAddress.country.code` 

    -   `BusinessPartner.addressData.organizationPostalAddress.country.code` 

    -   `BusinessPartner.customerInformation.salesArrangements.salesOfficeDisplayId` 

    -   `BusinessPartner.businessPartnerType` 

    -   `BusinessPartner.roles.role.code` 

    -   `BusinessPartner.customerInformation.customerAccountGroup.code` 

    -   `BusinessPartner.customerInformation.salesArrangements.salesAreaRef.salesOrganizationDisplayId` 

    -   `BusinessPartner.customerInformation.salesArrangements.salesAreaRef.distributionChannel` 

    -   `BusinessPartner.customerInformation.salesArrangements.salesAreaRef.division` 

    -   `BusinessPartner.supplierInformation.accountingInformation.companyCodeDisplayId` 

    -   `BusinessPartner.supplierInformation.purchasingArrangements.purchasingOrganizationDisplayId` 


-   Similarly, set the **Data Filters** under **Data Scope** section, if applicable.

    **Data Scope Filters** These are the object selection filters supported by SAP Master Data Integration - Business Partners:

    -   `BusinessPartner.taxNumbers.taxNumberType.code` 

    -   `BusinessPartner.identifications.identificationType.code` 

    -   `BusinessPartner.roles.role.code` 

    -   `BusinessPartner.customerInformation.salesArrangements.salesAreaRef.salesOrganizationDisplayId` 

    -   `BusinessPartner.customerInformation.salesArrangements.salesAreaRef.distributionChannel` 

    -   `BusinessPartner.customerInformation.salesArrangements.salesAreaRef.division` 

    -   `BusinessPartner.addressData.usages.usage.code` 

    -   `BusinessPartner.supplierInformation. accountingInformation.companyCodeDisplayId` 

    -   `BusinessPartner.supplierInformation.purchasingArrangements.purchasingOrganizationDisplayId` 


-   To enable Distribution of Key Mapping to connected systems, select the **Distribute Key Mapping** checkbox. Similarly, fill the **Key Mapping** section if applicable.

-   Select **Save** . The Business Partner Replication Model is created, with status as **Inactive** . To Activate the replication model, click **Activate** at the top right corner.


> ### Note:  
> 1.  A PUSH based Business Data Orchestration model for Business Partners also includes distribution of Business Partners Relationships and Key Mapping \(if any\). A separate SOAP PUSH distribution model is not required for Business Partners Relationships and Key Mapping. However, a separate destination configuration setup is required for Business Partners Relationships and Key Mapping.For example, `<businessSystemId>_BPRELOUTBOUND` and `<businessSystemId>_KMOUTBOUND` 
> 
> 2.  Refer here for [SOAP distribution related system limitations](../about-this-service/system-limitations-e7ccdfa.md) .

