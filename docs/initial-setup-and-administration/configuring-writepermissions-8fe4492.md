<!-- loio8fe4492db4114d5dbbf635e6cddfdd37 -->

# Configuring writePermissions



<a name="loio8fe4492db4114d5dbbf635e6cddfdd37__purpose-of-writepermissions"/>

## Purpose of `writePermissions` 

Sets write permissions for master data \(e.g., create, update, delete\).



<a name="loio8fe4492db4114d5dbbf635e6cddfdd37__how-to-configure-writepermissions"/>

## How to configure `writePermissions` 

> ### Note:  
> You should only grant the write permissions that the application needs.

To configure the `writePermissions` , open the SAP BTP cockpit, and navigate to the service instance that is used to connect your application.

View and update attributes as follows:

1.  Navigate to the service instance.

2.  Select **... -\> View Parameters** to view the current attribute configuration of the service instance.

3.  Copy the JSON object with the current state of attributes.

4.  Select **... -\> Update** . Paste the existing JSON object and add, update, or remove the relevant attributes. Note that the update operation does not patch the existing configuration, it replaces the full state of configuration. Therefore, it is important to provide all relevant attributes in the update operation.


Add the following attribute to configure the `writePermissions` .

```
"writePermissions": [
				{ "entityType": "<entityTypeOdmName1>" },
				{ "entityType": "<entityTypeOdmName2>" },
				...
				]
```

The `writePermissions` attribute holds a JSON array of JSON objects that define for which entity types to grant write permissions to the connected application.

The `writePermissions` attribute has to meet the following constraints:

-   A fully qualified entity name according to the SAP One Domain Model specification.

-   Each entity type has to be enclosed in a JSON object with the structure `{"entityType":"<entityTypeOdmName>"}` .


The following structure provides an example for granting write permissions for cost center and purchasing organization to a client:

```
"writePermissions": [
				{ "entityType": "sap.odm.finance.costobject.CostCenter" },
				{ "entityType": "sap.odm.procurement.orgunit.PurchasingOrganization" }
				]
```

Refer to [Integration Models](../about-this-service/integration-models-8882bf9.md) for an overview of the fully qualified entity names according to the SAP One Domain model specification.

