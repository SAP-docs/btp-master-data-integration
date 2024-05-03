<!-- loio5528c6dc25ef45ec9b9f7fcb0f3b986c -->

# Connecting S/4HANA Cloud or Cloud Applications Based on the SAP BTP ABAP Environment

Configuration steps required for applications based on the SAP BTP ABAP environment to consume SAP Master Data Integration.

Follow the below steps for connecting S/4HANA Cloud, or applications that are based on the SAP Business Technology Platform ABAP environment.



<a name="loio5528c6dc25ef45ec9b9f7fcb0f3b986c__prerequisites"/>

## Prerequisites

In the following it is assumed that you have created a dedicated service instance and a service binding for the application that is to be connected to SAP Master Data Integration. In addition, for the service instance, you have to maintain the `businessSystemId` attribute as well as configure write permissions for the objects your application needs.

For more details, refer to

-   [Connecting Applications via Service Instances](connecting-applications-via-service-instances-e01bb46.md) 

-   [Configuring `businessSystemId` ](configuring-businesssystemids-for-client-applications-b99332f.md) 

-   [Configuring `writePermissions` ](configuring-writepermissions-8fe4492.md) 




<a name="loio5528c6dc25ef45ec9b9f7fcb0f3b986c__establish-connection-to-sap-master-data-integration"/>

## Establish connection to SAP Master Data Integration



<a name="loio5528c6dc25ef45ec9b9f7fcb0f3b986c__create-a-communication-arrangement-sap-com-0659"/>

## Create a Communication Arrangement \(SAP\_COM\_0659\)

Before you create a Communication Arrangement, go to **SAP BTP Cockpit** , select the respective **Service Instance** , and copy the **Service Binding** for *Basic or mTLS Authentication* .

> ### Note:  
> For *mTLS Client Certificate Authentication* , the service Key is generated with **Certificate** and **Key** information.

Using the service binding, create a Communication Arrangement as follows:

1.  Go to the ABAP system’s launchpad and select the **Communication Arrangement** tile.

2.  Choose **New** . Select communication scenario `SAP_COM_0659` .

3.  Paste the **Service Binding** copied from the **SAP BTP Cockpit** .

4.  Select **Create** .

5.  Open the newly created Communication Arrangement and verify the ***auto-filled* ** details like **Arrangement Name** , **Communication System** , **Outbound Communication** , and **Outbound Services** .




<a name="loio5528c6dc25ef45ec9b9f7fcb0f3b986c__enable-integration-with-business-data-orchestration"/>

## Enable integration with Business Data Orchestration



<a name="loio5528c6dc25ef45ec9b9f7fcb0f3b986c__create-a-communication-arrangement-sap-com-0594"/>

## Create a Communication Arrangement \(SAP\_COM\_0594\)

Go to the ABAP system’s launchpad and select the **Communication Arrangement** tile.

Create a Communication Arrangement as follows:

1.  Go to the ABAP system's launchpad and select the **Communication Arrangement** tile.

2.  Choose **New** . Select communication scenario `SAP_COM_0594` , enter any description, and click on **Save** .

3.  Make note of the service URL of service " **MDO: Distribution Administration** " in the **Inbound Services** table, as you will need it later when configuring the SAP BTP destination for Business Data Orchestration.

4.  Create the communication system by clicking on the **New** link.

5.  **Communication System** : Check the **Inbound Only** checkbox.

6.  In the table **Users for Inbound Communication** , click the "+" icon.

7.  Create a new user with any name by clicking on **New User** .

8.  Enter a password \(long enough\) if required, and create the user. **Note:** Ensure that you copy this password since it is required later while configuring the SAP BTP destination for Business Data Orchestration.

9.  Save the communication system.

10. Save and activate the communication arrangement.




<a name="loio5528c6dc25ef45ec9b9f7fcb0f3b986c__create-a-sap-btp-destination-for-business-data-orchestration"/>

## Create a SAP BTP Destination for Business Data Orchestration

Follow guide [SAP Master Data Integration\>Business Data Orchestration\>Initial Setup of Business Data Orchestration\>Connecting Clients](https://help.sap.com/docs/SAP_MASTER_DATA_INTEGRATION/8ce78b673ef04cc1bcfeb01c93ef7885/6b7029a67db0438084485b3b26579b4f.html) to create a destination for your ABAP system using the service URL as well as the inbound user details noted in the previous step.



<a name="loio5528c6dc25ef45ec9b9f7fcb0f3b986c__set-up-distribution-models"/>

## Set up Distribution Models

Follow guide [SAP Master Data Integration\>Business Data Orchestration\>Initial Setup of Business Data Orchestration\>Manage Distribution Models](https://help.sap.com/docs/SAP_MASTER_DATA_INTEGRATION/8ce78b673ef04cc1bcfeb01c93ef7885/f63ec1de09ea4211a8dab5884447c25c.html) to create push or pull distribution models depending on your scenario.

