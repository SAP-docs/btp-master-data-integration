<!-- loio9121c31fd67d40cdb03c0e352833546b -->

# Support for Multiwriter Scenarios

SAP Master Data Integration service allows applications to write to master data records according to the configured write permissions. For more information, see [Configuring Clients](../initial-setup-and-administration/configuring-writepermissions-8fe4492.md) .

A scenario where multiple clients have write permissions to the same master data type and there are records created or updated by multiple clients is called a **multiwriter scenario** .

Multiwriter scenarios require coordination between the participating clients and Master Data Integration to avoid one client overwriting updates made by another client. Master Data Integration provides optional features that can help a client to not override updates made by another client.

Consult the documentation of each integration to learn whether an application implements these features and how it can be used in a multiwriter scenario. For more information, see [Integration](../integration/integration-a504461.md) .



<a name="loio9121c31fd67d40cdb03c0e352833546b__patches"/>

## Patches

Master Data Integration allows clients to send patches \(instead of full updates\) to update master data records. If different clients in a multiwriter scenario update different parts of the record, patches can help to avoid overwriting unrelated parts.



<a name="loio9121c31fd67d40cdb03c0e352833546b__optimistic-locking"/>

## Optimistic Locking

Master Data Integration tracks the version ID for each master data record. This version ID can be used for optimistic locking. Optimistic locking allows a client to detect a concurrent update to the same master data record by another client as follows:

Master Data Integration assigns new version IDs to a record every time that record is changed. The version ID is replicated to the clients together with the record. When a client writes to Master Data Integration, it can include the previous version ID as known to that client. Master Data Integration rejects the update if a previous version ID was sent by the client and does not match the current version ID. The client can then react to the rejection.

A client that detects a rejection because of a concurrent update can react by informing the user or by resolving the conflict, and trying to write to Master Data Integration again with an updated previous version ID.

Previous version IDs and optimistic locking are not supported by the SOAP APIs for Business Partner.

