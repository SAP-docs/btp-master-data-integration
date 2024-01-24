<!-- loio20db337061cc4773a1fe1cf04e9d356a -->

# Synchronization of Master Data

SAP Master Data Integration service is a central master data hub. Applications integrate with Master Data Integration to synchronize their local master data databases with the master data database of the central hub. In a typical setup, there is exactly one tenant of Master Data Integration for each landscape. Application tenants of the same landscape integrate against the same tenant. The tenant helps to ensure that all applications within this landscape arrive at a consistent view on master data.

Master Data Integration focuses exclusively on the integration aspect regarding master data. This is achieved via replicating master data records. The service enables applications to do initial loads of master data and afterwards stay in sync with the master data database of Master Data Integration. Administrators can control which data is to be synchronized with which applications via distribution models. For more information, see

[Support for Initial Loads](support-for-initial-loads-923c184.md) and [Distribution Models](distribution-models-9254f0e.md).

For staying in sync with the master data database of Master Data Integration, the service offers a REST API. For business partners and business partner relationships, it additionally offers SOAP APIs. For more information, see [Connecting SOAP Applications](../initial-setup-and-administration/connecting-soap-applications-14fcc48.md).

Applications use the REST Events API to perform initial loads and then delta loads to stay in sync. Delta loads enable the applications to receive events about all changes to the master data database of Master Data Integration that happened since the last call to the events API.

Staying up to date with the changes to the master data database of Master Data Integration in the delta load eventually delivers the same information for every application \(provided identical filter settings\).

