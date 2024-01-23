<!-- loio9254f0e3dd77420b90f573a7fcbc88e2 -->

# Distribution Models

Distribution models contain distribution relevant settings in a central place. They are needed independently if the integrating applications are cloud or on-premise applications. To avoid heterogeneous logic and diverse user interfaces of the specific applications in point-to-point integrations, SAP Master Data Orchestration provides a central control of data distribution in the context of SAP Master Data Integration service.

SAP Master Data Orchestration delivers a user interface for the central maintenance of distribution models. These are later replicated to the clients when the models are activated.

What are now the main ingredients of the distribution model and how are they used in the connected applications? First of all, a model has a name and contains a language-dependent description to be able to easily identify its purpose. Next, the object type and its version have to be specified. Master Data Integration operates based on the master date defined in SAP One Domain Model as a common language. This is important information to identify the contained data scope of the master data. Furthermore, it offers connectivity for one data provider with multiple consumers or the other way around, for multiple providers with one consumer.

In Master Data Integration using scenarios, one partner will always be Master Data Integration depending on the direction. Currently, for distribution only ABAP-based systems like S/4HANA or SAP Cloud Master Data Governance can act as provider in a distribution model because of the ABAP library. Master Data Integration is then the consumer.

More important are the filters, which allow to control the data flow, that is, what data are replicated to what client. The requirements can easily be outlined by two examples. A production unit represented by a corresponding application normally doesn't need customers if the sales application is not available. On the other hand, a locally operating sales organization in the U.S. normally would not need customer sales data from European based sales organizations. These organizational data don't need to be replicated and this will reduce data traffic and volume.

To fulfill these requirements two types of filters are available, instance and data scope filters:

As already indicated in the above two examples, the final filtering occurs by setting up logical conditions based on the payload of the replicated object. The explicit formulation of the specific condition requires knowledge of the business process. Therefore, it can only be set up at the individual SAP customer. This clarifies that the user of the distribution model maintenance in SAP Master Data Orchestration would rather be a user with business background than a technical administrator.

> ### Note:  
> The transition process from the local distribution frameworks to its central representation and maintenance has started. Further information on supported clients will be made available in the scenario descriptions of the Intelligent Enterprise Suite.

> ### Note:  
> For transparency reasons and also flexibility for later changes, it is recommended to always connect only one provider with one consumer.

> ### Note:  
> This implies directly that data providers \("upstream clients" of Master Data Integration\) will normally only have filters if data are strictly only for local use or outdated.

-   **Object Selection Filters** : Object selection filters are used to control which records \(instances\) is to be replicated to a specific consumer \("downstream client"\).

-   **Data Scope Filters** : Data scope filters control the parts of the records that are to be replicated to a specific consumer \("downstream client"\).




<a name="loio9254f0e3dd77420b90f573a7fcbc88e2__related-information"/>

## Related Information

-   [Maintenance of the Distribution Model in SAP Master Data Orchestration](https://help.sap.com/docs/SAP_MASTER_DATA_INTEGRATION/8ce78b673ef04cc1bcfeb01c93ef7885/ef9398e6f60a44568d106f71ea4d5cfa.html) 

-   [Destinations Configuration for SOAP API in Master Data Integration](../initial-setup-and-administration/configuring-destinations-for-soap-870fed9.md) 


