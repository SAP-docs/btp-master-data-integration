<!-- loiob99332fc2bd145a58c6200920d9a6e35 -->

# Configuring businessSystemIds for Client Applications



<a name="loiob99332fc2bd145a58c6200920d9a6e35__purpose-of-businesssystemid"/>

## Purpose of `businessSystemId` 

The `businessSystemId` serves the following two purposes.

1.  The `businessSystemId` acts as a display name for the client represented by the service instance in the SAP Master Data Orchestration UI. The display name represents the client's service instance when selecting the consumer destinations for the Master Data Integration service provider when [configuring distribution models](configuring-distribution-models-b033b0a.md) . Distribution models control for instance the read permissions of clients for the data replicated via SAP Master Data Integration.

2.  In addition, the `businessSystemId` configuration attribute is mandatory to connect a client using the SOAP API for Business Partner. When replicating SOAP messages from client to SAP Master Data Integration, the `businessSystemId` must correspond to `SenderBusinessSystemID` in the SOAP message. Therefore, use the **Own Business System** that is configured in SAP S/4HANA On Premise and SAP S/4HANA Cloud systems as `businessSystemId` . You can retrieve this value as follows:

    -   In SAP S/4HANA On-premise, run transaction `SLDCHECK` and check the section **Calling function** `LCR_GET_OWN_BUSINESS_SYSTEM` .

    -   In SAP S/4HANA Cloud, or the SAP Business Technology Platform ABAP environment, go to the Communication Systems and select the system that is marked as **Own System** . Use the name that is maintained in the **Business System** field.


 


<a name="loiob99332fc2bd145a58c6200920d9a6e35__how-to-configure-businesssystemid"/>

## How to configure `businessSystemId` 

> ### Note:  
> You should only configure `businessSystemId` if the documentation of the connected application demands it.

To configure the `businessSystemId` , open the SAP BTP cockpit, and navigate to the service instance that is used to connect your application.

View and update attributes as follows:

1.  Navigate to the service instance.

2.  Select **... -\> View Parameters** to view the current attribute configuration of the service instance.

3.  Copy the JSON object with the current state of attributes.

4.  Select **... -\> Update** . Paste the existing JSON object and add, update, or remove the relevant attributes. Note that the update operation does not patch the existing configuration, it replaces the full state of configuration. Therefore, it is important to provide all relevant attributes in the update operation.


Add the following attribute to configure the `businessSystemId` .

```

				"businessSystemId": "<businessSystemId>"
			
```

The `businessSystemId` attribute has to meet the following constraints:

-   A length of up to 60 characters.

-   It must be unique within a tenant.


