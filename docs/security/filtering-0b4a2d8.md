<!-- loio0b4a2d8862334095ae00fd47574df1f7 -->

# Filtering

SAP Master Data Integration provides a data filtering engine to restrict the events or the data contained within the events that a client receives from the Log API.A filter has to be registered for a specific client \(the service instance in Cloud Foundry\) of a tenant via a separate API.After registering a filter for a client, for all following requests of this client to the Log API, the response of the Log API is based on the conditions of the activated filter.This indicates that the clients will not receive all events, or receive artificial events indicating that certain master data instances are from that point onwards excluded or again included in the returned events.

The filtering behavior can be changed by registering a different filter.Registering a new filter for one client deactivates the previous filter registered for this client.Changing the filter will trigger new include or exclude messages for all existing master data instances whose visibility has changed in the next request of the client to the Log API.

Filters are configured using distribution models that specify which master data can be replicated to consumers.If not all objects or object-specific data are relevant for a consumer, replication filters on object-instance level and data scope ensure the precise distribution of master data.For more information, see [Connecting Clients](https://help.sap.com/viewer/c7713d6177ad479d9ea00958db9f2f81/CLOUD/en-US/69ae614272654411a4c03acea8d488b3.html) and [Maintenance of the Distribution Model in SAP Cloud Platform Master Data Orchestration](https://help.sap.com/viewer/c7713d6177ad479d9ea00958db9f2f81/CLOUD/en-US/ef9398e6f60a44568d106f71ea4d5cfa.html) .

