<!-- loio741ef3f1637749eeba8fd0d8fe599803 -->

# Pricing



<a name="loio741ef3f1637749eeba8fd0d8fe599803__consumption-scenarios"/>

## Consumption Scenarios

Consumption of Master Data Integration that is induced by running integration of SAP-branded cloud applications is free of charge. This includes integration that are implemented via the Cloud Integration capability of [SAP Integration Suite](https://help.sap.com/docs/SAP_INTEGRATION_SUITE) , for instance for integrating SAP ECC or non-SAP applications and services. The list of SAP-branded cloud applications includes:

-   [SAP Ariba](https://help.sap.com/docs/ariba) 

-   [SAP Cloud for Customer](https://help.sap.com/docs/SAP_CLOUD_FOR_CUSTOMER) 

-   [SAP Commerce Cloud](https://help.sap.com/docs/SAP_COMMERCE_CLOUD) 

-   [SAP Concur](https://www.concur.com/en-us/support) 

-   [SAP Configure Price Quote](https://help.sap.com/docs/SAP_CPQ) 

-   [SAP Customer Data Cloud](https://help.sap.com/docs/SAP_CUSTOMER_DATA_CLOUD) 

-   [SAP Emarsys Account Engagement](https://help.sap.com/docs/SAP_EMARSYS_ACCOUNT_ENGAGEMENT) 

-   [SAP Field Service Management](https://help.sap.com/docs/SAP_FIELD_SERVICE_MANAGEMENT) 

-   [SAP Fieldglass](https://help.sap.com/docs/SAP_Fieldglass) 

-   [SAP Integration Suite](https://help.sap.com/docs/SAP_INTEGRATION_SUITE) 

-   [SAP Marketing Cloud](https://help.sap.com/docs/SAP_MARKETING_CLOUD) 

-   [SAP Master Data Governance, cloud edition](https://help.sap.com/docs/MDG_CE) 

-   [SAP S/4HANA Cloud, private edition](https://help.sap.com/docs/SAP_S4HANA_CLOUD_PE) 

-   [SAP S/4HANA Cloud, public edition](https://help.sap.com/docs/SAP_S4HANA_CLOUD) 

-   [SAP S/4HANA Cloud for Projects, Resource Management](https://help.sap.com/docs/PPRM_OD) 

-   [SAP Subscription Billing](https://help.sap.com/docs/CLOUD_TO_CASH_OD) 

-   [SAP SuccessFactors Employee Central](https://help.sap.com/docs/SAP_SUCCESSFACTORS_EMPLOYEE_CENTRAL) 

-   [SAP SuccessFactors Employee Central Payroll](https://help.sap.com/docs/SAP_SUCCESSFACTORS_EMPLOYEE_CENTRAL_PAYROLL) 


Consumption that is induced by integration of [SAP S/4HANA](https://help.sap.com/docs/SAP_S4HANA_ON-PREMISE) \(On-Premise\) is charged based on the following metrics:

-   Storage: data stored in GB

-   Bandwidth: data transferred in GB


In case of hybrid scenarios, that is, scenarios that include SAP-branded cloud applications and [SAP S/4HANA](https://help.sap.com/docs/SAP_S4HANA_ON-PREMISE) \(On-Premise\), the usage for storage is charged only for those master data records that are not consumed by any SAP-branded cloud application.



<a name="loio741ef3f1637749eeba8fd0d8fe599803__service-plans"/>

## Service Plans

The pricing schema is implemented via the two service plans: *SAP Integration* and *S/4HANA On-Premise* . These service plans have to be configured in the setup phase for each client \(see [Connecting Clients](../initial-setup-and-administration/connecting-applications-69ae614.md) \) according to the following rules:

-   Service plan: *SAP Integration* 

    -   This service plan is to be chosen only for connecting SAP-branded cloud applications. It must not be used for connecting other applications.

    -   Choose this service plan also for integration implemented via [SAP Integration Suite](https://help.sap.com/docs/SAP_INTEGRATION_SUITE) . More information on how to implement integration to SAP Master Data Integration via the Cloud Integration capability of Integration Suite can be found in the blog post [SAP Integration Suite — Integration with SAP Master Data Integration service](https://blogs.sap.com/2022/05/20/sap-integration-suite-integration-with-sap-master-data-integration-mdi-service/) .

    -   This service plan is available as a default entitlement on every SAP Business Technology Platform global account.

    -   This service plan is free for usage with SAP-branded cloud applications \(including SAP Integration Suite\).


-   Service plan: *SAP S/4HANA On-Premise* 

    -   This service plan is to be chosen only for the integration of [SAP S/4HANA](https://help.sap.com/docs/SAP_S4HANA_ON-PREMISE) \(On-Premise\) systems. It must not be used for connecting other applications or services.

    -   This service plan is only available for CPEA-enabled Business Technology Platform global accounts.

    -   Charging happens based on 2 metrics: storage and bandwidth.





<a name="loio741ef3f1637749eeba8fd0d8fe599803__additional-information"/>

## Additional Information

-   SAP Master Data Integration is available as a default entitlement on every SAP Business Technology Platform global account. No additional subscription is needed.

-   SAP ECC can be connected via SAP Cloud Integration \(see [SAP Integration Suite — Integration with SAP Master Data Integration service](https://blogs.sap.com/2022/05/20/sap-integration-suite-integration-with-sap-master-data-integration-mdi-service/) \)


Learn more about pricing and usage of SAP Master Data Integration in our service catalog on [SAP Discovery Center](https://discovery-center.cloud.sap/serviceCatalog/master-data-integration) .

