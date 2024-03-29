<!-- loiodab76d5506a44c8e85f314fc3be30e13 -->

# What Is Master Data Integration?

Multi-tenant cloud service in the Intelligent Enterprise. 

SAP Master Data Integration service is a central master data hub. Applications integrate with SAP Master Data Integration to synchronize their local master data databases with the master data database of the central hub. In a typical setup, there is exactly one tenant of SAP Master Data Integration for each landscape. The tenant helps to ensure that all applications within this landscape arrive at a consistent view on master data. The following figure illustrates the situation:

![SAP Master Data Integration — Overview](images/MDI_overview_e3c0856.png)

SAP Master Data Integration focuses exclusively on the integration aspect regarding master data. This is achieved via replicating master data records. SAP Master Data Integration enables applications to do initial loads of master data, and afterwards stay in sync with the master data database of SAP Master Data Integration. Administrators can control which data is to be synchronised with which applications, monitor the replication, and comply with data protection and privacy regulations. For more details on the features of SAP Master Data Integration, see [Features](../features/features-832c2df.md) .

Master data processes such as consolidation, data quality control, and central governance are not in the scope of SAP Master Data Integration. These processes can be implemented by leveraging [SAP Master Data Governance, cloud edition](https://www.sapstore.com/solutions/77000/SAP-Master-Data-Governance%2C-cloud-edition) , which integrates with SAP Master Data Integration service.

The Cloud Integration capability of SAP Integration Suite can be used to integrate non-SAP and SAP on-premise applications with SAP Master Data Integration. It comes with special support for SAP Master Data Integration. For more details, see [SAP Cloud Integration](https://help.sap.com/docs/CLOUD_INTEGRATION?locale=en-US) .

SAP Master Data Integration service does not support arbitrary but only specific master data objects. The supported master data objects are adhering to the SAP One Domain Model. For more details on the supported integration models of SAP One Domain Model, see [Integration Models](integration-models-8882bf9.md) . For more information on the SAP One Domain Model, see [SAP One Domain Model](https://help.sap.com/docs/SAP_ODM/ea7614c1cd0349e58d7f2b04b562d625/2aa15254bfac45a6970d26b6192093cc.html) .

To create a tenant of SAP Master Data Integration, an SAP Business Technology Platform global account is required. The service is cross-consumable from any SAP Business Technology Platform data center. For more details on consuming SAP Master Data Integration, see [Data Center Availability](data-center-availability-ab183ca.md) and [Pricing](pricing-741ef3f.md) .

For more information on the available integration from SAP applications into SAP Master Data Integration, see [Integration](../integration/integration-a504461.md) .

> ### Note:  
> This guide is open for contributions and feedback using GitHub. This allows you to get in contact with responsible authors of SAP Help Portal pages and the development team to discuss documentation-related issues. To contribute to this guide, or to provide feedback, choose the corresponding option on SAP Help Portal:
> 
> -   *Feedback* \> *Create issue* : Provide feedback about a documentation page. This option opens an issue on GitHub.
> 
> -   *Feedback* \> *Edit page* : Contribute to a documentation page. This option opens a pull request on GitHub.
> 
> 
> You need a personal GitHub account to use these options.
> 
> -   [Contribution Guidelines](https://help.sap.com/docs/open-documentation-initiative/contribution-guidelines/readme.html) 
> 
> -   [Introduction Video: Open Documentation Initiative](https://www.youtube.com/watch?v=WJ0oarMlVW4) 
> 
> -   [Blog Post: Introducing the Open Documentation Initiative](https://blogs.sap.com/2021/05/20/introducing-the-open-documentation-initiative/) 

