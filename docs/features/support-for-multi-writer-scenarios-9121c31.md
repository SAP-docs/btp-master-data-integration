<!-- loio9121c31fd67d40cdb03c0e352833546b -->

# Support for Multi-Writer Scenarios

SAP Master Data Integration service allows applications to write to master data recordsaccording to the configured write permissions. For more information, see [Configuring Clients](../initial-setup-and-administration/configuring-writepermissions-8fe4492.md) .

A scenario where multiple clients have write permissions to the same master datatype and there are records created or updated by multiple clients iscalled a **multiwriter scenario** .

Multiwriter scenarios require coordination between the participating clientsand Master Data Integration to avoid one client overwriting updates made byanother client. Master Data Integration provides optional features that can helpa client to not override updates made by another client.

Consult the documentation of each integration to learn whether an applicationimplements these features and how it can be used in a multiwriter scenario. For more information, see [Integration](../integration/integration-a504461.md) .



<a name="loio9121c31fd67d40cdb03c0e352833546b__patches"/>

## Patches

Master Data Integration allows clients to send patches \(instead of full updates\)to update master data records. If different clients in a multiwriter scenarioupdate different parts of the record, patches can help to avoid overwritingunrelated parts.



<a name="loio9121c31fd67d40cdb03c0e352833546b__optimistic-locking"/>

## Optimistic Locking

Master Data Integration tracks the version ID for each master data record.This version ID can be used for optimistic locking. Optimistic locking allows aclient to detect a concurrent update to the same master data record byanother client as follows:

Master Data Integration assigns new version IDs to a record every time thatrecord is changed. The version ID is replicated to the clients together withthe record. When a client writes to Master Data Integration, it can include theprevious version ID as known to that client. Master Data Integration rejects theupdate if a previous version ID was sent by the client and does notmatch the current version ID. The client can then react to the rejection.

A client that detects a rejection because of a concurrent update can react byinforming the user or by resolving the conflict, and trying to write to MasterData Integration again with an updated previous version ID.

Previous version IDs and optimistic locking are not supportedby the SOAP APIs for Business Partner.

