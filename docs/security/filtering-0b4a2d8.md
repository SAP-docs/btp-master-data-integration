<!-- loio0b4a2d8862334095ae00fd47574df1f7 -->

# Filtering

SAP Master Data Integration service provides a data filtering engine. This engine allows you to restrict the information about events in the LOG API that clients receive. A filter has to be registered for a specific client of a tenant via a separate API. A client is a service instance in Cloud Foundry. Filters are configured using distribution models that specify which master data can be replicated to consuming clients. If not all objects or object-specific data are relevant for a consuming client, replication filters on object-instance level and data scope ensure the precise distribution of master data.

After registering a filter for a client, all following responses of the Log API are based on the conditions of the activated filter. This client does not receive all events. The client receives artificial events, which indicate that certain master data instances are from that point onwards excluded or again included in the returned events.

> ### Note:  
> The filtering behavior can be changed by registering a different filter. Registering a new filter for one client deactivates the previous filter registered for this client.

Changing the filter triggers new include or exclude messages for existing master data instances, if the visibility has changed in the next request of the client to the Log API. s For more information, see [Connecting Clients](https://help.sap.com/viewer/c7713d6177ad479d9ea00958db9f2f81/CLOUD/en-US/69ae614272654411a4c03acea8d488b3.html) and [Maintenance of the Distribution Model in SAP Cloud Platform Master Data Orchestration](https://help.sap.com/viewer/c7713d6177ad479d9ea00958db9f2f81/CLOUD/en-US/ef9398e6f60a44568d106f71ea4d5cfa.html) .

