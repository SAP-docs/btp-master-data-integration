<!-- loioc53da2571f5f4be5b76054c8a4b7a0d1 -->

# Deleting Tenants

The tenant of a subaccount will be automatically deleted when either of the following is true:

For more information on how to disconnect an application, please refer to [disconnecting applications](disconnecting-applications-d09d7b9.md).

-   The service instance of SAP Master Data Integration that is getting deleted is the last SAP Master Data Integration service instance in the subaccount, and there are no more active subscriptions to SAP Master Data Integration in the subaccount.

-   The subscription to SAP Master Data Integration that is getting deleted is its last subscription in the subaccount, and there are no service instances of SAP Master Data Integration present in the subaccount.


> ### Caution:  
> Deleting a tenant will irreversibly delete all data associated with the tenant. To avoid deleting a tenant, make sure that it contains at least one service instance or subscription at any point in time. SAP Master Data Integration has a safeguarding mechanism in place to protect against accidental deletion of a tenant for the first case mentioned above, where only one service instance and no other subscriptions are active for the tenant. The deletion of that last instance will only be allowed if the parameter `enableTenantDeletion` is explicitly set to `true` in the configuration of the service instance. For more information on how to update a service instance, see [Updating Service Instances](https://help.sap.com/docs/SERVICEMANAGEMENT/09cc82baadc542a688176dce601398de/002ae850a32244af85c8405fbcd7d9ab.html).

