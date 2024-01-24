<!-- loioe23428eb2c6c43af855f13ea19705b0f -->

# Configuring globalTenantId



<a name="loioe23428eb2c6c43af855f13ea19705b0f__purpose-of-globaltenantid"/>

## Purpose of `globalTenantId` 

Sets the `globalTenantId` attribute of the client.

It is used when returning the Globally Unique Tenant ID \(GTID\) of the last significant writer on the SAP Master Data Integration Events API. If a client is the last significant writer, the value of its `globalTenantId` attribute is the one returned by the Events API.

When a client is deleted, the value of its `globalTenantId` attribute is no longer accessible on the Events API.



<a name="loioe23428eb2c6c43af855f13ea19705b0f__how-to-configure-globaltenantid"/>

## How to configure `globalTenantId` 

> ### Note:  
> You should only configure `globalTenantId` if the documentation of the connected application demands it.

To configure the `globalTenantId` , open the SAP BTP cockpit, and navigate to the service instance that is used to connect your application.

View and update attributes as follows:

1.  Navigate to the service instance.

2.  Select **... -\> View Parameters** to view the current attribute configuration of the service instance.

3.  Copy the JSON object with the current state of attributes.

4.  Select **... -\> Update** . Paste the existing JSON object and add, update, or remove the relevant attributes. Note that the update operation does not patch the existing configuration, it replaces the full state of configuration. Therefore, it is important to provide all relevant attributes in the update operation.


Add the following attribute to configure the `globalTenantId` .

```
"globalTenantId": "<globallyUniqueTenantId>"
```

The `globalTenantId` attribute has to meet the following constraints:

-   A length of at least 1 up to 40 characters.

-   Consist of only alphanumeric characters and special characters `-` , `.` , `_` , and `~` .


