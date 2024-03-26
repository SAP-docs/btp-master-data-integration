<!-- loio659f09eb7d4a40bba9974d60bcd291de -->

# Creating MDO Distribution Model for Business Partner Replication

Follow the steps to configure distribution model, which will be used to replicate the Business Partners from the SAP Master Data Integration service to client systems. For more information refer to [Maintenance of the Distribution Model in Business Data Orchestration](https://help.sap.com/viewer/8ce78b673ef04cc1bcfeb01c93ef7885/CLOUD/en-US/ef9398e6f60a44568d106f71ea4d5cfa.html "The distribution model specifies the configuration according to which master data is replicated from provider to consumer.") :arrow_upper_right:.

1.  Go to *Instances and Subscriptions* in your Subaccount. Under *Subscriptions*, click on *Master Data Integration \(Orchestration\)*.
2.  Select *Go to Application*. This will open the Fiori Launchpad for MDO application.
3.  Go to*Configure Master Data Integration* section and select *Manage Distribution Model* tile.
4.  Click *Create*.
5.  Provide a name in the *Model* field. Select *Business Partner \(sap.odm.businesspartner.BusinessPartner\)* from *Business Object Type* dropdown field. Next, choose *Push* from the *Mode* dropdown field.
6.  Add a relevant number to define the *Package Size* as per your requirement. Recommendation is not to exceed above 50.
7.  Select the *Continuous Distribution* checkbox to have the business partners replicated as soon as they are created/updated.
8.  Under *Provider Interface* section, select **MDI\_SOAP\_BUSINESS\_PARTNER** in the *API* placeholder.
9.  In *Provider* section, click *Create*. Under *Cloud Platform Cockpit Destination* field, click to open the input pop-up. In the display table, select *MDI* from the *Provider Value* column.
10. In *Consumer* section, select the **businessSystemId** for the business system for which the distribution model is being created. The `businessSystemId`, which was used while creating the service instance will appear here. For more information, see [Connecting Applications](connecting-applications-69ae614.md).

    > ### Note:  
    > The business system selected here is where the data will be distributed. For the consumer system selected above, ensure that below destinations are created on SAP BTP Cockpit.
    > 
    > -   <businessSystemId\>\_BPOUTBOUND
    > 
    > -   <businessSystemId\>\_BPRELOUTBOUND
    > 
    > -   <businessSystemId\>\_KMOUTBOUND

11. Select the appropriate *Application Category* if applicable.
12. Optionally, you can set *Data Filters*under *Object Selection* section, if applicable. For more information, see the *Object Selection Filters* section in the following document: [Distribution Model Maintenance](distribution-model-maintenance-d61330e.md).
13. Similarly, set the *Data Filters* under*Data Scope* section, if applicable. For more information, see the *Data Scope Filters* section in the following document: [Distribution Model Maintenance](distribution-model-maintenance-d61330e.md).
14. To enable Distribution of Key Mapping to connected systems, select the *Distribute Key Mapping* checkbox. Similarly, fill the *Key Mapping* section if applicable.
15. Select *Save*. The Business Partner Replication Model is created, with status as *Inactive*. To Activate the replication model, click *Activate* at the top right corner.
16. The configuration is now complete.

