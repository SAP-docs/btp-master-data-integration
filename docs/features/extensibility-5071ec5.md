<!-- loio5071ec5461f24c0d998afeb80b3d7a8f -->

# Extensibility

Standard software as delivered by SAP covers a large number of processes, functions and features. However, there are parts to processes in customer landscapes that are specific for individual customers. Therefore, it is common that there is a large need to extend the standard scope with additional features. They are in the end reflected frequently in new attributes of master data, which normally define and control business processes. Besides that, additional attributes and objects are often needed to control distribution or perform analytics. Targets for extensions are often widely used master data objects like Business Partner, Product or Workforce Person \(Employee\).

This demand is increased in a heterogeneous landscape with integration capabilities like SAP Master Data Integration service. Here, the integration is facilitated by the [SAP One Domain Model](https://api.sap.com/sap-one-domain-model) as a common language for all connected applications, which normally possess own data models. The One Domain Model contains related objects that were considered to be relevant for more than one application or even instance in the landscape. Because not all attributes of the connecting applications might be contained in the One Domain Model, an additional need for extensibility is created.

Extensions can be defined in SAP Master Data Orchestration. In this user interface, the One Domain Model structures within Master Data Integration can be extended with additional attributes in case they are annotated as being extensible in the central One Domain Model. It allows the creation of new attributes at every level of the One Domain Model structure.

Concerning compatibility, Master Data Integration propagates extensions to newer versions of the One Domain Model as long as these versions do not contain breaking changes.

In addition, the created attributes can be automatically used as filter criteria in the [Distribution Models of SAP Master Data Orchestration](https://help.sap.com/docs/SAP_MASTER_DATA_INTEGRATION/8ce78b673ef04cc1bcfeb01c93ef7885/ef9398e6f60a44568d106f71ea4d5cfa.html?version=CLOUD).

> ### Note:  
> A draft mode is offered on the user interface in order to make extensions only visible after they are saved to the repository. After that they can't be changed or removed any longer for various reasons. An improvement is in preparation.

> ### Note:  
> These extensions are only valid for Master Data Integration and it needs to be assured that they will be also present in the upstream and downstream applications, which provide and consume the master data.



<a name="loio5071ec5461f24c0d998afeb80b3d7a8f__related-information"/>

## Related Information

Learn how to set up and use extensions- [Manage Business Object Type](https://help.sap.com/docs/SAP_MASTER_DATA_INTEGRATION/8ce78b673ef04cc1bcfeb01c93ef7885/ba60c0c3e1b848a391e26795d3b3aee7.html?version=CLOUD) 

.

