<!-- loio5528c6dc25ef45ec9b9f7fcb0f3b986c -->

# Connecting S/4HANA Cloud or Cloud Applications Based on the SAP BTP ABAP Environment

Configuration steps required for applications based on the SAP BTP ABAP environment to consume SAP Master Data Integration.

Follow the below steps for connecting S/4HANA Cloud, or applications that are based on the SAP Business Technology Platform ABAP environment.



<a name="loio5528c6dc25ef45ec9b9f7fcb0f3b986c__prerequisites"/>

## Prerequisites

`businessSystemId` In the following it is assumed that you have created a dedicated service instance and a service binding for the application that is to be connected to SAP Master Data Integration. In addition, for the service instance, you have to maintain theattribute as well as configure write permissions for the objects your application needs.

For more details, refer to

-   [Connecting Applications via Service Instances](connecting-applications-via-service-instances-e01bb46.md) 

-   [`businessSystemId` Configuring](configuring-businesssystemids-for-client-applications-b99332f.md) 

-   [`writePermissions` Configuring](configuring-writepermissions-8fe4492.md) 




<a name="loio5528c6dc25ef45ec9b9f7fcb0f3b986c__establish-connection-to-sap-master-data-integration"/>

## Establish connection to SAP Master Data Integration



<a name="loio5528c6dc25ef45ec9b9f7fcb0f3b986c__create-a-communication-arrangement-sap-com-0659"/>

## Create a Communication Arrangement \(SAP\_COM\_0659\)

**SAP BTP Cockpit** **Service Instance** **Service Binding** *Basic or mTLS Authentication* Before you create a Communication Arrangement, go to, select the respective, and copy thefor.

Using the service binding, create a Communication Arrangement as follows:

> ### Note:  
> *mTLS Client Certificate Authentication* **Certificate** **Key** For, the service Key is generated withandinformation.

1.  **Communication Arrangement** Go to the ABAP system’s launchpad and select thetile.

2.  **New** `SAP_COM_0659` Choose. Select communication scenario.

3.  **Service Binding** **SAP BTP Cockpit** Paste thecopied from the.

4.  **Create** Select.

5.  ***auto-filled* ** **Arrangement Name** **Communication System** **Outbound Communication** **Outbound Services** Open the newly created Communication Arrangement and verify thedetails like,,, and.




<a name="loio5528c6dc25ef45ec9b9f7fcb0f3b986c__enable-integration-with-sap-master-data-orchestration"/>

## Enable integration with SAP Master Data Orchestration



<a name="loio5528c6dc25ef45ec9b9f7fcb0f3b986c__create-a-communication-arrangement-sap-com-0594"/>

## Create a Communication Arrangement \(SAP\_COM\_0594\)

**Communication Arrangement** Go to the ABAP system’s launchpad and select thetile.

Create a Communication Arrangement as follows:

1.  **Communication Arrangement** Go to the ABAP system's launchpad and select thetile.

2.  **New** **Save** `SAP_COM_0594` Choose. Select communication scenario, enter any description, and click on.

3.  **MDO: Distribution Administration** **Inbound Services** Make note of the service URL of service "" in thetable, as you will need it later when configuring the SAP BTP destination for SAP Master Data Orchestration.

4.  **New** Create the communication system by clicking on thelink.

5.  **Communication System** **Inbound Only** : Check thecheckbox.

6.  **Users for Inbound Communication** In the table, click the "+" icon.

7.  **New User** Create a new user with any name by clicking on.

8.  **Note:** Enter a password \(long enough\) if required, and create the user.Ensure that you copy this password since it is required later while configuring the SAP BTP destination for SAP Master Data Orchestration.

9.  Save the communication system.

10. Save and activate the communication arrangement.




<a name="loio5528c6dc25ef45ec9b9f7fcb0f3b986c__create-a-sap-btp-destination-for-sap-master-data-orchestration"/>

## Create a SAP BTP Destination for SAP Master Data Orchestration

[SAP Master Data Integration\>SAP Master Data Orchestration\>Initial Setup of SAP Master Data Orchestration\>Connecting Clients](https://help.sap.com/docs/SAP_MASTER_DATA_INTEGRATION/8ce78b673ef04cc1bcfeb01c93ef7885/6b7029a67db0438084485b3b26579b4f.html) Follow guideto create a destination for your ABAP system using the service URL as well as the inbound user details noted in the previous step.



<a name="loio5528c6dc25ef45ec9b9f7fcb0f3b986c__set-up-distribution-models"/>

## Set up Distribution Models

[SAP Master Data Integration\>SAP Master Data Orchestration\>Initial Setup of SAP Master Data Orchestration\>Manage Distribution Models](https://help.sap.com/docs/SAP_MASTER_DATA_INTEGRATION/8ce78b673ef04cc1bcfeb01c93ef7885/f63ec1de09ea4211a8dab5884447c25c.html) Follow guideto create push or pull distribution models depending on your scenario.

