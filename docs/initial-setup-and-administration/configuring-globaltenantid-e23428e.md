<!-- loioe23428eb2c6c43af855f13ea19705b0f -->

# Configuring globalTenantId



<a name="loioe23428eb2c6c43af855f13ea19705b0f__purpose-of-globaltenantid"/>

## `globalTenantId` Purpose of

`globalTenantId` Sets theattribute of the client.

`globalTenantId` It is used when returning the Globally Unique Tenant ID \(GTID\) of the last significant writer on the SAP Master Data Integration Events API. If a client is the last significant writer, the value of itsattribute is the one returned by the Events API.

`globalTenantId` When a client is deleted, the value of itsattribute is no longer accessible on the Events API.



<a name="loioe23428eb2c6c43af855f13ea19705b0f__how-to-configure-globaltenantid"/>

## `globalTenantId` How to configure

> ### Note:  
> `globalTenantId` You should only configureif the documentation of the connected application demands it.

`globalTenantId` To configure the, open the SAP BTP cockpit, and navigate to the service instance that is used to connect your application.

View and update attributes as follows:

`globalTenantId` Add the following attribute to configure the.

`globalTenantId` Theattribute has to meet the following constraints:

1.  Navigate to the service instance.

2.  **... -\> View Parameters** Selectto view the current attribute configuration of the service instance.

3.  Copy the JSON object with the current state of attributes.

4.  **... -\> Update** Select. Paste the existing JSON object and add, update, or remove the relevant attributes. Note that the update operation does not patch the existing configuration, it replaces the full state of configuration. Therefore, it is important to provide all relevant attributes in the update operation.


```
"globalTenantId": "<globallyUniqueTenantId>"
```

-   A length of at least 1 up to 40 characters.

-   `-` `.` `_` `~` Consist of only alphanumeric characters and special characters,,, and.


