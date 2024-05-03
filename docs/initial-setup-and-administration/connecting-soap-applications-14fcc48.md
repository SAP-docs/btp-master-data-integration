<!-- loio14fcc481e55542fc887c6a7cc25db333 -->

# Connecting SOAP Applications

Integrating an application via the SOAP APIs of Master Data Integration for business partners \(respectively business partner relationships\) requires additional configuration steps.



<a name="loio14fcc481e55542fc887c6a7cc25db333__prerequisites"/>

## Prerequisites

1.  A service instance of SAP Master Data Integration for client is required. Follow [Connecting Applications via Service Instance](connecting-applications-via-service-instances-e01bb46.md) to create a service instance.

2.  Subscription to SAP Master Data Integration \(Orchestration\) on the SAP BTP Cockpit. See [Subscription Process for Business Data Orchestration](https://help.sap.com/viewer/c7713d6177ad479d9ea00958db9f2f81/CLOUD/en-US/f3fc55879f8342ee9fbafda37db36019.html) for further details.

3.  Business system ID configuration for tenants. See [Configuring Business System ID for Tenants](configuring-own-business-system-id-75d55b7.md) for further details.




<a name="loio14fcc481e55542fc887c6a7cc25db333__procedure"/>

## Procedure

This section describes the configuration that is needed to enable the SOAP APIs for business partners:



<a name="loio14fcc481e55542fc887c6a7cc25db333__configuration-activities"/>

## Configuration Activities:

-   Set up the destination to connect SAP Master Data Integration with the connected client. See [Destinations Configuration for SOAP API in Master Data Integration](configuring-destinations-for-soap-870fed9.md) for further details.

-   Maintenance of distribution model. See [Distribution Model Maintenance](configuring-distribution-models-b033b0a.md) for further details.


To complete the integration with SAP Master Data Integration, perform the configurations on the connected application. For more information, refer to the links provided under the section [Integration](../integration/integration-a504461.md) .

