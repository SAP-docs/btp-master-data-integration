<!-- loiod61330e286714d38a3b893d4643bd1e5 -->

# Distribution Model Maintenance

The distribution model specifies the master data to be replicated from provider to consumer.

To know more about Creation, Activation, Deactivation, and Editing of the Distribution Model, refer [Maintenance of the Distribution Model in SAP Master Data Orchestration](https://help.sap.com/viewer/8ce78b673ef04cc1bcfeb01c93ef7885/CLOUD/en-US/ef9398e6f60a44568d106f71ea4d5cfa.html "The distribution model specifies the configuration according to which master data is replicated from provider to consumer.") :arrow_upper_right:.

> ### Note:  
> In SAP Master Data Integration - Business Partners, destinations with the below naming conventions are created to carry out replications. See [Destination Configuration for SAP Master Data Orchestration](destination-configuration-for-sap-master-data-orchestration-2959a5c.md)
> 
> -   \*\_BPOUTBOUND – Indicates destination for replication of business partner data
> 
> -   \*\_BPRELOUTBOUND – Indicates destination for replication of business partner relationship data
> 
> -   \*\_KMOUTBOUND – Indicates destination for replication of key mapping data



<a name="loiod61330e286714d38a3b893d4643bd1e5__section_xqq_1kl_mnb"/>

## Object Selection Filters

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




<a name="loiod61330e286714d38a3b893d4643bd1e5__section_oz4_mkl_mnb"/>

## Data Scope Filters

Following are the data scope filters supported by SAP Master Data Integration - Business Partners:

-   `BusinessPartner.taxNumbers.taxNumberType.code`

-   `BusinessPartner.identifications.identificationType.code`

-   `BusinessPartner.roles.role.code`

-   `BusinessPartner.customerInformation.salesArrangements.salesAreaRef.salesOrganizationDisplayId`

-   `BusinessPartner.customerInformation.salesArrangements.salesAreaRef.distributionChannel`

-   `BusinessPartner.customerInformation.salesArrangements.salesAreaRef.division`

-   `BusinessPartner.addressData.usages.usage.code`

-   `BusinessPartner.supplierInformation. accountingInformation.companyCodeDisplayId`

-   `BusinessPartner.supplierInformation.purchasingArrangements.purchasingOrganizationDisplayId`


**Related Information**  


[Destination Configuration for SAP Master Data Orchestration](destination-configuration-for-sap-master-data-orchestration-2959a5c.md "")

[Creating MDO Distribution Model for Business Partner Replication](creating-mdo-distribution-model-for-business-partner-replication-659f09e.md "")

