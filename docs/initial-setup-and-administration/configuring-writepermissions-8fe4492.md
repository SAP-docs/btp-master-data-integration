<!-- loio8fe4492db4114d5dbbf635e6cddfdd37 -->

# Configuring writePermissions



<a name="loio8fe4492db4114d5dbbf635e6cddfdd37__purpose-of-writepermissions"/>

## `writePermissions` Purpose of

Sets write permissions for master data \(e.g., create, update, delete\).



<a name="loio8fe4492db4114d5dbbf635e6cddfdd37__how-to-configure-writepermissions"/>

## `writePermissions` How to configure

> ### Note:  
> You should only grant the write permissions that the application needs.

`writePermissions` To configure the, open the SAP BTP cockpit, and navigate to the service instance that is used to connect your application.

View and update attributes as follows:

`writePermissions` Add the following attribute to configure the.

`writePermissions` Theattribute holds a JSON array of JSON objects that define for which entity types to grant write permissions to the connected application.

`writePermissions` Theattribute has to meet the following constraints:

The following structure provides an example for granting write permissions for cost center and purchasing organization to a client:

[Integration Models](../about-this-service/integration-models-8882bf9.md) Refer tofor an overview of the fully qualified entity names according to the SAP One Domain model specification.

1.  Navigate to the service instance.

2.  **... -\> View Parameters** Selectto view the current attribute configuration of the service instance.

3.  Copy the JSON object with the current state of attributes.

4.  **... -\> Update** Select. Paste the existing JSON object and add, update, or remove the relevant attributes. Note that the update operation does not patch the existing configuration, it replaces the full state of configuration. Therefore, it is important to provide all relevant attributes in the update operation.


```
"writePermissions": [
				{ "entityType": "<entityTypeOdmName1>" },
				{ "entityType": "<entityTypeOdmName2>" },
				...
				]
```

```
"writePermissions": [
				{ "entityType": "sap.odm.finance.costobject.CostCenter" },
				{ "entityType": "sap.odm.procurement.orgunit.PurchasingOrganization" }
				]
```

-   A fully qualified entity name according to the SAP One Domain Model specification.

-   `{"entityType":"<entityTypeOdmName>"}` Each entity type has to be enclosed in a JSON object with the structure.


