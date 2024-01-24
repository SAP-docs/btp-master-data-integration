<!-- loiob033b0a713984a7d85bbb79b426d40d9 -->

# Configuring Distribution Models

Use SAP Master Data Orchestration for configuring distribution models. For more information on SAP Master Data Orchestration, refer to [help.sap.com](https://help.sap.com/viewer/8ce78b673ef04cc1bcfeb01c93ef7885/CLOUD/en-US/f3fc55879f8342ee9fbafda37db36019.html) 

> ### Note:  
> SAP Master Data Integration offers SOAP APIs for the integration of the Business Partner object in addition to the generic REST APIs. Refer to documentation of the respective integrating application to identify the underlying APIs used for the integration. The specifics for the Business Partner distribution models are shown below.



<a name="loiob033b0a713984a7d85bbb79b426d40d9__configuring-sap-master-data-integration--business-partners-for-rest-scenario"/>

## Configuring SAP Master Data Integration — Business Partners for REST Scenario



<a name="loiob033b0a713984a7d85bbb79b426d40d9__configuring-business-partner-and-bp-relationship-distribution-model"/>

## Configuring Business Partner and BP Relationship Distribution Model

A BP Relationship distribution model always has to be accompanied by a business partner distribution model, in order to avoid replication failures. The failures can occur as referenced business partners are not replicated beforehand to the consumers. It is also recommended restricting the use of filter criteria for object selection accordingly, to avoid replication failures through missing business partners.

Note the key activation and deactivation procedures to avoid replication failures.

**Activation** : The BP Relationship distribution model can only be activated in case a Business Partner distribution model is already active for the same connection.

**Deactivation** : The Business Partner distribution model can only be deactivated, if there is no active BP Relationship distribution model for the same connection.

> ### Note:  
> 1.  “Connection” here is mentioned as the combination of provider and consumer in the distribution models.
> 
> 2.  This is relevant for business partner replication via REST in both directions \(from and to SAP Master Data Integration\).



<a name="loiob033b0a713984a7d85bbb79b426d40d9__configuring-sap-master-data-integration--business-partners-for-soap-scenario"/>

## Configuring SAP Master Data Integration — Business Partners for SOAP Scenario

Follow the steps to configure distribution model, which will be used to replicate the Business Partners from the SAP Master Data Integration service to connected clients. For more information refer to [Maintenance of the Distribution Model in SAP Master Data Orchestration](https://help.sap.com/docs/SAP_MASTER_DATA_INTEGRATION/8ce78b673ef04cc1bcfeb01c93ef7885/ef9398e6f60a44568d106f71ea4d5cfa.html) .

1.  Go to **Instances and Subscriptions** in your Subaccount. Under **Subscriptions** , click on **Master Data Integration \(Orchestration\)** .

2.  Select **Go to Application** . This will open the Fiori Launchpad for MDO application.

3.  Go to **Manage Master Data Orchestration** section and select **Manage Distribution Model** tile.

4.  Click **Create** .

5.  Provide a name in the **Model** field. **Select Business Partner \(sap.odm.businesspartner.BusinessPartner\)** from **Business Object Type** dropdown field. Next, choose **Push** from the **Mode** dropdown field.

6.  Select the **Continuous Distribution** checkbox to have the business partners replicated as soon as they are created/updated.

7.  Under **Provider Interface** section, select **SAP Master Data Integration\_SOAP\_BUSINESS\_PARTNER** in the **API** placeholder.

8.  In Provider section, click **Create** . Under **Cloud Platform Cockpit Destination** field, click to open the input pop-up. In the display table, select **SAP Master Data Integration** from the **Provider Value** column.

9.  In **Consumer** section, select the `businessSystemId` for the business system for which the distribution model is being created. The `businessSystemId` , which was used while creating the service instance will appear here. For more information, see [Service Instance in SAP Master Data Integration](connecting-applications-via-service-instances-e01bb46.md) .


> ### Note:  
> The business system selected here is where the data will be distributed. For the consumer system selected above, ensure that below destinations based on the integration scenario are created on SAP BTP Cockpit.
> 
> -   `<businessSystemId>_BPOUTBOUND` 
> 
> -   `<businessSystemId>_BPRELOUTBOUND` 
> 
> -   `<businessSystemId>_KMOUTBOUND` 

1.  Select the appropriate **Application Category** if applicable.

2.  Optionally, you can set **Data Filters** under **Object Selection** section if applicable.

    **Object Selection Filters** 

    Following are the object selection filters supported by SAP Master Data Integration - Business Partners:

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


3.  Similarly, set the **Data Filters** under **Data Scope** section, if applicable.

    **Data Scope Filters** 

    Following are the object selection filters supported by SAP Master Data Integration - Business Partners:

    -   `BusinessPartner.taxNumbers.taxNumberType.code` 

    -   `BusinessPartner.identifications.identificationType.code` 

    -   `BusinessPartner.roles.role.code` 

    -   `BusinessPartner.customerInformation.salesArrangements.salesAreaRef.salesOrganizationDisplayId` 

    -   `BusinessPartner.customerInformation.salesArrangements.salesAreaRef.distributionChannel` 

    -   `BusinessPartner.customerInformation.salesArrangements.salesAreaRef.division` 

    -   `BusinessPartner.addressData.usages.usage.code` 

    -   `BusinessPartner.supplierInformation. accountingInformation.companyCodeDisplayId` 

    -   `BusinessPartner.supplierInformation.purchasingArrangements.purchasingOrganizationDisplayId` 


4.  To enable Distribution of Key Mapping to connected systems, select the **Distribute Key Mapping** checkbox. Similarly, fill the **Key Mapping** section if applicable.

5.  Select **Save** . The Business Partner Replication Model is created, with status as **Inactive** . To Activate the replication model, click **Activate** at the top right corner.


> ### Note:  
> A PUSH based MDO model for Business Partners also includes distribution of Business Partners Relationships and Key Mapping \(if any\). A separate SOAP PUSH distribution model is not required for Business Partners Relationships and Key Mapping. However, a separate destination configuration setup will be required for Business Partners Relationships and Key Mapping. For example `<businessSystemId>_BPRELOUTBOUND` and `<businessSystemId>_KMOUTBOUND` 
