<!-- loio0f2dc7862e994d788fffeaa5f570ac2f -->

# Configuring Clients

Depending on how you intend to use SAP Master Data Integration, you need to provide client configuration for each connected application. You can provide client configuration when you create a service instance to connect an application, or via an update of the service instance. Please refer to [Connecting Applications via Service Instance](connecting-applications-via-service-instances-e01bb46.md) for more details.

This page lists the available configuration attributes.



<a name="loio0f2dc7862e994d788fffeaa5f570ac2f__businesssystemid"/>

## `businessSystemId` 

The `businessSystemId` attribute serves two purposes:

1.  It acts as display name for the client in the distribution model configuration of the Business Data Orchestration UI.

2.  It is mandatory to integrate with the SOAP API for business partners.


Please refer to [Configuring `businessSystemId` ](configuring-businesssystemids-for-client-applications-b99332f.md) for more details.



<a name="loio0f2dc7862e994d788fffeaa5f570ac2f__writepermissions"/>

## `writePermissions` 

Sets write permissions for master data \(e.g., create, update, delete\).

You should only grant the write permissions that the application needs.

Please refer to [Configuring `writePermissions` ](configuring-writepermissions-8fe4492.md) for more details.



<a name="loio0f2dc7862e994d788fffeaa5f570ac2f__globaltenantid"/>

## `globalTenantId` 

Sets the `globalTenantId` attribute of the client.

It is used when returning the Globally Unique Tenant ID \(GTID\) of the last significant writer on the SAP Master Data Integration Events API. If a client is the last significant writer, the value of its `globalTenantId` attribute is the one returned by the Events API.

You should only configure this if the documentation of the connected application demands it.

Please refer to [Configuring `globalTenantId` ](configuring-globaltenantid-e23428e.md) for more details.



<a name="loio0f2dc7862e994d788fffeaa5f570ac2f__logsys"/>

## `logSys` 

Sets the `logSys` attribute of the client.

It is used when returning the logical system of the last significant writer on the SAP Master Data Integration Events API. If a client is the last significant writer, the value of its `logSys` attribute is the one returned by the Events API.

You should only configure this if the documentation of the connected application demands it.

Please refer to [Configuring `logSys` ](configuring-logsys-a59464b.md) for more details.

