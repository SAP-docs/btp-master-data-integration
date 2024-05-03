<!-- loioc53da2571f5f4be5b76054c8a4b7a0d1 -->

# Deleting Tenants

The tenant of a subaccount will be deleted when the respective criteria's contained within the following condition are true:

> ### Note:  
> The tenant deletion process differs based on the fact if there was ever the SAP Master Data Integration Tenant Application subscribed in the subaccount. If the tenant application is/was subscribed follow the steps in section 1. if there was never a subscription of the SAP Master Data Integration Tenant Application follow the steps in section 2.

**1. The SAP Master Data Integration Tenant Application was ever subscribed in the subaccount** 

-   The SAP Master Data Integration Tenant application is unsubscribed from the subaccount


SAP Master Data Integration Tenant application has a safeguarding mechanism in place to protect against deletion of a tenant because of accidental unsubscription. Tenant data will not be immediately deleted, but retained for a period of 28 days after the unsubscription of the SAP Master Data Integration Tenant application.

During the retention period, when the SAP Master Data Integration Tenant application is unsubscribed, clients connected with the tenant will not be able to access the SAP Master Data Integration APIs. Hence, no data replication via the tenant can take place.

To continue to use the same tenant and associated data, resubscribe to SAP Master Data Integration Tenant application within the data retention period of 28 days. On re-subscription of the application, clients connected with the tenant will again be able to access the SAP Master Data Integration APIs.

Unsubscribed tenants will be deleted after the expiry of the data retention period. This will irreversibly delete all data associated with the tenant and service instances of SAP Master Data Integration in that tenant will become permanently unusable.

> ### Caution:  
> Resubscribing to SAP Master Data Integration Tenant application in a subaccount within the retention period does not create a fresh tenant, but allows clients to access the already existing data of the tenant in the same subaccount. It is not possible to create a new tenant in the same subaccount during the retention period.
> 
> **2. The SAP Master Data Integration Tenant Application was never subscribed in the subaccount:** 

-   The tenant is deleted when the last service instance of SAP Master Data Integration in the subaccount is getting deleted.


For more information on how to disconnect an application, please refer to [disconnecting applications](disconnecting-applications-d09d7b9.md) .

> ### Caution:  
> Deleting a tenant will irreversibly delete all data associated with the tenant. To avoid deleting a tenant, make sure that it contains at least one service instance or subscription at any point in time. Deleting the last service instance will also delete all associated data for the tenant in SAP Master Data Integration service. There is no retention period and the data is permanently deleted in SAP Master Data Integration. SAP Master Data Integration has a safeguarding mechanism in place to protect against accidental deletion of a tenant for the first case mentioned above, where only one service instance and no other subscriptions are active for the tenant. The deletion of that last instance will only be allowed if the parameter `enableTenantDeletion` is explicitly set to `true` in the configuration of the service instance. For more information on how to update a service instance, see [Updating Service Instances](https://help.sap.com/docs/SERVICEMANAGEMENT/09cc82baadc542a688176dce601398de/002ae850a32244af85c8405fbcd7d9ab.html) .

