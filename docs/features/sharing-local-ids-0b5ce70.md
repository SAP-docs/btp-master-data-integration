<!-- loio0b5ce707b4b148fba92cd62843d86cc3 -->

# Sharing Local IDs

Intelligent Enterprise promise is based on delivery of end-to-end business processes. For Process Integration, there is a need for semantic consolidation of information across the contributing clients in the landscapes.

Every master data object in SAP Master Data Integration service has a uniquely identifiable ID. But it is also common for the object to be associated with local IDs in the context of the various applications, which need to process that object. These local IDs are fully qualified in that context that they have been defined. However, when information flows from one application to the other, it needs to ensure the associated local IDs and the related contexts are carried through with the master data object. By doing so, all destination applications can understand and react to the information they are receiving.

Master Data Integration provides the capability to store ID maps between Global and Local IDs as well as a mechanism to distribute these ID maps and do bidirectional lookups.

1.  **RequestsAPI** provides the mechanism to applications to write their local IDs and the associated context to Master Data integration. This information is then added to the metadata of the information which Master Data Integration distributes.

2.  **EventsAPI** allows applications to receive the distributed local IDs and the associated context.

3.  **KeyMappingAPI** allows for applications to bidirectionally look up for local or global IDs, which are connected to each other.


