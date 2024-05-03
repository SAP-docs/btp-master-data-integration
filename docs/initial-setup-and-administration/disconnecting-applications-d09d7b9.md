<!-- loiod09d7b9a840147bda023f078e6db9d80 -->

# Disconnecting Applications

To disconnect an application, delete the corresponding service instance or subscription to SAP Master Data Integration.

> ### Note:  
> After deleting a service instance or subscription, it is no longer possible to reconnect an application as the same client and resume the synchronization process. Instead, you will have to repeat the full setup and initial loads for the data that is to be kept in sync.



<a name="loiod09d7b9a840147bda023f078e6db9d80__deleting-a-service-instance"/>

## Deleting a Service Instance

Navigate to the subaccount in the SAP BTP Cockpit and select **Services \> Instances and Subscriptions** . Select the relevant service instance and delete all existing service bindings. Once all service bindings are deleted, you will be able to delete the service instance. For more information, refer to [Deleting Service Instances](https://help.sap.com/docs/service-manager/sap-service-manager/deleting-service-instances) .

If you have connected a SAP BTP application via a service instance and a destination, please review and potentially delete the corresponding destination pointing to the deleted service instance.



<a name="loiod09d7b9a840147bda023f078e6db9d80__remarks"/>

## Remarks

Before deleting a service instance or subscription, make sure to always deactivate its distribution models. Refer to [Deactivating Distribution Models](configuring-distribution-models-b033b0a.md) for more details on how to manage distribution models.

An attempt to delete a service instance with an active distribution model will result in an error, asking you to deactivate it before deleting the instance.

An attempt to delete the last service instance when no other subscriptions exist in the subaccount, will lead to an error, asking you to update the instance to confirm deletion. [Update the service instance](https://help.sap.com/docs/SERVICEMANAGEMENT/09cc82baadc542a688176dce601398de/002ae850a32244af85c8405fbcd7d9ab.html) with the field `enableTenantDeletion` set to `true` .

If the tenant of a subaccount has been deleted and a new client is created in the same subaccount, a new SAP Master Data Integration tenant will be created for that subaccount. For more information, see [Deleting Tenants](deleting-tenants-c53da25.md) .

