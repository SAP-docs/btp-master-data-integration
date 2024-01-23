<!-- loio8a7c50f5961f4df5a1e3f4724bf8b7b3 -->

# Using BTP Booster to Setup SAP Master Data Integration

SAP BTP provides [Boosters](https://help.sap.com/docs/btp/sap-business-technology-platform/boosters) to automate the setup of BTP services. A booster walks you through a set of guided steps in a wizard-like manner and as a result, you get a preconfigured BTP subaccount. You can use the BTP Booster for SAP Master Data Integration to create a basic Master Data Integration setup inside your BTP global account in an automated procedure.



<a name="loio8a7c50f5961f4df5a1e3f4724bf8b7b3__scope-of-the-booster-for-sap-master-data-integration"/>

## Scope of the Booster for SAP Master Data Integration

The Booster for SAP Master Data Integration performs the following setup steps:

-   Creation of a new BTP subaccount or re-use of existing subaccount \(see [Usage Recommendation](using-btp-booster-to-setup-sap-master-data-integration-8a7c50f.md#loio8a7c50f5961f4df5a1e3f4724bf8b7b3__usage-recommendation) \). For more information on manual creation of a new subaccount, see [Creating Tenants](creating-tenants-6e3b768.md) .

-   Creation of a new Cloud Foundry Organization.

-   Creation of a new SAP BTP space.

-   Creation of a new Master Data Integration service instance along with a service key. For more information on manual creation of Master Data Integration service instances, see [Connecting Applications via Service Instances](connecting-applications-via-service-instances-e01bb46.md) .

-   Subscription of the SAP Master Data Orchestration application.

-   Assignment of users of the connected Identity Provider to administrator and developer roles in SAP BTP.

-   Creation and assignment of a BTP role collection for the SAP Master Data Orchestration application.




<a name="loio8a7c50f5961f4df5a1e3f4724bf8b7b3__access-the-booster-for-sap-master-data-integration"/>

## Access the Booster for SAP Master Data Integration

1.  Navigate to your global account in the SAP BTP Cockpit.

2.  Select **Boosters** from menu on the left-hand side.

3.  Select the tile named **Set up SAP Master Data Integration** and click on **Start** in the upcoming screen.

4.  Now, you can see the Booster for Master Data Integration.

5.  Select **Next** to step through the wizard.

6.  Lastly, select **Finish** to execute the setup steps in the background.




<a name="loio8a7c50f5961f4df5a1e3f4724bf8b7b3__usage-recommendation"/>

## Usage Recommendation

SAP Master Data Integration isolates data per tenant and thus by subaccount. That is, several service instances in the same subaccount can share data. Therefore, we recommend to check if the global account wherein your execute the booster already contains a subaccount with a service instance of SAP Master Data Integration. If you want to share data with this service instance, we recommend to choose the existing subaccount in the respective booster step. Otherwise, if you want to separate data, for example to distinguish productive and development landscapes, we recommend to create a new subaccount.



<a name="loio8a7c50f5961f4df5a1e3f4724bf8b7b3__support"/>

## Support

If the booster fails, open a support incident on the component `BC-CP-CF-ONEMDS` .

