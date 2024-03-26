<!-- loiofbf9114cc99b472888ca1e499c5408ab -->

# Multiversion Support

SAP Master Data Integration service supports the synchronization of master data objects according to their definition in the [SAP One Domain Model](https://help.sap.com/docs/SAP_ODM/ea7614c1cd0349e58d7f2b04b562d625/2aa15254bfac45a6970d26b6192093cc.html) . The SAP One Domain Model serves as a central data model that creates a common understanding of data across multiple different applications. The integration models used by Master Data Integration adhere to the SAP One Domain Model. To ensure that the SAP One Domain Model can evolve without interrupting existing integrations, Master Data Integration offers **multiversion support** .

The SAP One Domain Model is versioned. Between compatible model versions of master data types, Master Data Integration offers **multiversion support** . This allows applications to synchronize their master data of a specific type with Master Data Integration based on different SAP One Domain Model versions, as long as these versions are compatible.

For example:

-   WorkforcePerson v2.1.1 and WorkforcePerson v3.0.0 are compatible.

-   Application A can send WorkforcePerson objects to Master Data Integration in v3.0.0.

-   Application B can consume WorkforcePerson objects from Master Data Integration in v2.1.1.


The **multiversion support** decouples the development cycles of SAP and non-SAP applications and enables continuous business processes, while evolving the underlying model. The **multiversion support** is restricted to different models of a master data type that have no breaking changes \(such as a removal of a field\) between them.

For an overview of the master data types that are available on Master Data Integration, refer to [Integration Models](../about-this-service/integration-models-8882bf9.md) . This overview includes the compatible versions.

