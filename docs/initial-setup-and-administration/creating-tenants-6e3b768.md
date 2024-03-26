<!-- loio6e3b768903744f04a98915c3a3ab2223 -->

# Creating Tenants



<a name="loio6e3b768903744f04a98915c3a3ab2223__prerequisites"/>

## Prerequisites

To create a tenant and use SAP Master Data Integration service, you must have a **global enterprise account** for the SAP Business Technology Platform. For more information on how to obtain a global account, see [Getting a Global Account](https://help.sap.com/docs/btp/sap-business-technology-platform/getting-global-account) . For a comprehensive overview of the account model of SAP BTP, refer to [Account Model](https://help.sap.com/docs/btp/sap-business-technology-platform/account-model) .

> ### Note:  
> SAP Master Data Integration service does not support Trial Accounts or Free Tier.



<a name="loio6e3b768903744f04a98915c3a3ab2223__how-to-create-a-tenant"/>

## How to Create a Tenant

To create a tenant, the first step is to create a subaccount. You must create the subaccount in one of the regions in which SAP Master Data Integration is available. Availability is described in the [data center availability](../about-this-service/data-center-availability-ab183ca.md) . To learn more about creating and managing subaccounts, refer to [Managing Subaccounts Using the Cockpit](https://help.sap.com/docs/btp/sap-business-technology-platform/managing-subaccounts-using-cockpit) .

For each subaccount, there can be at most one tenant of SAP Master Data Integration. This tenant is created for a subaccount when the first service instance or subscription of SAP Master Data Integration is created. Each service instance or subscription within a subaccount is used to connect a different client. To establish technical connectivity, each client requires its own service instance or subscription. Neither data nor configuration is shared between different SAP Master Data Integration tenants.

For more information on how to create an SAP Master Data Integration service instance, see [Connecting Applications](connecting-applications-69ae614.md) .

> ### Note:  
> A subaccount for an SAP Master Data Integration tenant should be exclusively used for managing the SAP Master Data Integration tenant. For security reasons, we recommend creating service instances and subscriptions within a subaccount only for BTP services or clients that have to be used in the context of the SAP Master Data Integration tenant.



<a name="loio6e3b768903744f04a98915c3a3ab2223__how-to-create-multiple-tenants"/>

## How to Create Multiple Tenants

For each subaccount, there can be at most one tenant of SAP Master Data Integration. In case several tenants are needed, a dedicated subaccount must be created for each tenant.



<a name="loio6e3b768903744f04a98915c3a3ab2223__best-practices"/>

## Best Practices

It is recommended to create a single tenant for the production landscape. Connecting multiple applications to the same tenant improves the consistency of the data shared within the landscape.

If you are following the three system landscape setup \(development, test, production\), it is recommended to have three different SAP Master Data Integration tenants — one tenant for each landscape. This avoids unintended data sharing between the landscapes.

