<!-- loioe01bb46b7e09427aa37ac2da40198cf2 -->

# Connecting Applications via Service Instances

In the following, you learn how to establish the technical connectivity between an application and an SAP Master Data Integration tenant via a service instance. In this scenario, the applications assume the role of a client of SAP Master Data Integration. For simplicity, we use the term application to refer to both applications and application tenants. We use the term client for an application with an established technical connectivity to an SAP Master Data Integration tenant.

Examples of applications that integrate vie service instances, are the following SAP-branded cloud applications and on-premise applications:

-   [SAP S/4HANA Cloud, public edition](../integration/integrating-with-sap-s-4hana-cloud-b3bb16f.md) 

-   [SAP S/4HANA Cloud, private edition](../integration/integrating-with-sap-s-4hana-cloud-b3bb16f.md) 

-   [SAP S/4HANA \(on-premise\)](../integration/integrating-with-sap-s-4hana-on-premise-adbf8ef.md) 

-   SAP Master Data Governance, cloud edition

-   [SAP SuccessFactors Employee Central, Payroll](../integration/integrating-with-sap-successfactors-3276e31.md) 

-   [SAP Ariba](../integration/integrating-with-sap-ariba-c7062ee.md) 

-   [SAP Customer Experience](../integration/integrating-with-sap-subscription-billing-1304ebb.md) 

-   [SAP Entitlement Management](../integration/integrating-with-sap-entitlement-management-b04dcc1.md) 

-   [SAP Fieldglass](../integration/integrating-with-sap-fieldglass-677569e.md) 

-   [SAP Subscription Billing](../integration/integrating-with-sap-subscription-billing-1304ebb.md) 

-   [SAP Field Service Management](../integration/integrating-with-sap-field-service-management-d294aa5.md) 




<a name="loioe01bb46b7e09427aa37ac2da40198cf2__create-a-service-instance"/>

## Create a Service Instance

For each application you connect, you have to create a dedicated service instance of SAP Master Data Integration from the SAP BTP marketplace. After creating the service instance, you create a service binding to obtain the credentials to establish the technical connectivity to the application. You can create multiple service bindings for a service instance to generate different credentials for the same application. This can be used to renew the credentials of an application.

> ### Note:  
> Every application that connects to an SAP Master Data Integration tenant must use its own dedicated service instance. You must not connect more than one application using the same service instance. Doing so can lead to unexpected behavior and inconsistencies.

To create a service instance of SAP Master Data Integration, perform the following steps in the context of a subaccount. If the SAP Master Data Integration tenant belonging to a subaccount does not yet exist, it will be created automatically when creating the first service instance. Refer to [Creating Service Instances](https://help.sap.com/docs/service-manager/sap-service-manager/creating-service-instances) for further details on how to create service instances using the SAP Business Technology Platform cockpit.

1.  Navigate to **Services** \> **Service Marketplace** and select **Master Data Integration** .

2.  Select **Create** in the top-right corner.

    A wizard opens, offering you to configure your new service instance:

    1.  Enter basic information for your service instance.

        For **Service** , ensure that `Master Data Integration` is selected from the dropdown list.

        Select the correct service plan from the dropdown field. The following service plans are available:

        -   `sap-integration` — This service plan must be chosen for connecting SAP-branded cloud applications \(e.g., SAP S/4HANA Cloud\). It must not be used for connecting other applications.

        -   `s4hana-onpremise` — This service plan must be chosen for the integration of SAP S/4HANA systems. It must not be used for connecting other applications.


        *Remark* : The `s4hana-onpremise` service plan is visible as a service plan option, if and only if you create the service instance in an CPEA-enabled BTP account. For more information, see [Entitlements and Quotas](https://help.sap.com/viewer/65de2977205c403bbc107264b8eccf4b/latest/en-US/00aa2c23479d42568b18882b1ca90d79.html) .

        For **Runtime Environment** , select `Other` from the dropdown list.

        Choose an **Instance Name** for your service instance. It is recommended to choose a name that uniquely identifies the application. For instance, you could choose the name `S4_FS10` for a service instance representing an SAP S/4HANA Cloud tenant `FS10` .

    2.  Choose **Next** .

    3.  Configure service instance parameters.

        Provide a value for the mandatory `application` attribute based on the application that you intend to connect:


        <table>
        <tr>
        <th valign="top">

        Application
        
        </th>
        <th valign="top">

        Attribute value
        
        </th>
        </tr>
        <tr>
        <td valign="top">
        
        SAP Ariba
        
        </td>
        <td valign="top">
        
        ariba
        
        </td>
        </tr>
        <tr>
        <td valign="top">
        
        SAP Cloud for Customer
        
        </td>
        <td valign="top">
        
        c4c
        
        </td>
        </tr>
        <tr>
        <td valign="top">
        
        SAP Customer Data Cloud
        
        </td>
        <td valign="top">
        
        cdc
        
        </td>
        </tr>
        <tr>
        <td valign="top">
        
        SAP Commerce Cloud
        
        </td>
        <td valign="top">
        
        commerceCloud
        
        </td>
        </tr>
        <tr>
        <td valign="top">
        
        SAP Concur
        
        </td>
        <td valign="top">
        
        concur
        
        </td>
        </tr>
        <tr>
        <td valign="top">
        
        SAP Fieldglass
        
        </td>
        <td valign="top">
        
        fieldglass
        
        </td>
        </tr>
        <tr>
        <td valign="top">
        
        SAP CPQ
        
        </td>
        <td valign="top">
        
        cpq
        
        </td>
        </tr>
        <tr>
        <td valign="top">
        
        SAP Subscription Billing
        
        </td>
        <td valign="top">
        
        hrc
        
        </td>
        </tr>
        <tr>
        <td valign="top">
        
        SAP Master Data Governance
        
        </td>
        <td valign="top">
        
        mdg
        
        </td>
        </tr>
        <tr>
        <td valign="top">
        
        SAP S/4HANA Cloud
        
        </td>
        <td valign="top">
        
        s4
        
        </td>
        </tr>
        <tr>
        <td valign="top">
        
        SAP S/4HANA Cloud for Projects, Resource Management
        
        </td>
        <td valign="top">
        
        resource management
        
        </td>
        </tr>
        <tr>
        <td valign="top">
        
        SAP SuccessFactors
        
        </td>
        <td valign="top">
        
        sfsf
        
        </td>
        </tr>
        </table>
        
        For example, if you connect an SAP S/4HANA Cloud tenant, you provide the following configuration:

        ```
        {
          "application": "s4"
        }
        ```

        Be aware that the service parameter dialog will show you all available attributes in the form of a JSON template. If you are unsure if these parameters are relevant for your scenario, you should only keep the `application` attribute and remove all other attributes.

        If needed, you can add and update attributes later.

        For an overview of attributes and their purpose, please refer to [Configuring Clients](configuring-clients-0f2dc78.md) .

        To view and update attributes as follows:

        1.  Navigate to the service instance.

        2.  Select **... -\> View Parameters** to view the current attribute configuration of the service instance.

        3.  Select **... -\> Update** to update the attribute configuration. Note that you need to provide all attributes, including existing ones, when performing an update.


    4.  Choose **Next** and review the instance details.

    5.  Choose **Create** to create the service instance. Note that you may have to refresh your browser if the instance does not immediately show up.


3.  Navigate to the newly created service instance. It should be visible in the subaccount **Services \> Instances** .

4.  **Creating a Service Binding** 

    Create a service binding in the newly created service instance to obtain credentials as follows. Refer to [Service Bindings](https://help.sap.com/docs/service-manager/sap-service-manager/service-bindings) for further details.

    1.  In the **Service Bindings** section, click on **Create** .

    2.  A wizard opens, offering you to configure your new service binding:

        **Choosing a Binding Name** 

        The service binding contains credentials. These credentials are used to authenticate an application. Multiple service bindings can be created. You must not use the service bindings of one service instance to connect multiple applications. All connections that are established via one service instance appear as the same client for SAP Master Data Integration.

        It is recommended to indicate the date of creation in the service binding name. By encoding the date in the binding name, it is easily possible to judge whether specific credentials might have been compromised in case of security incidents in a given time frame.

        For example, the recommended service binding name for a service binding created on May 1st, 2024 would be `ValidFrom_20240501` , encoding the creation date as part of the binding name.

        **Choosing Binding Parameters** 

        When providing no binding parameters, SAP Master Data Integration defaults to generating credentials for an OAuth2 client credentials flow for authentication. This flow authenticates via client ID and client secret.

        SAP Master Data Integration also supports OAuth2-based authentication methods that utilize certificate-based mutual TLS. By providing specific binding parameters, you can configure which type of credentials to use or generate for a service binding. For details on available options and which parameters to use, refer to [OAuth2-based Authentication](oauth2-based-authentication-7701dff.md) .

    3.  **Click on Create** .





<a name="loioe01bb46b7e09427aa37ac2da40198cf2__configuring-the-applications"/>

## Configuring the Applications

The service bindings of a service instance can be utilized by applications to authenticate at the APIs of SAP Master Data Integration. This information needs to be copied into the application so that the application can authenticate.

Steps on how to maintain this information in the application can be found in the documentation of the respective application. If you are connecting an SAP S/4HANA Cloud tenant, for instance, the documentation of SAP S/4HANA Cloud contains a section on how to [establish connectivity with SAP Master Data Integration](https://help.sap.com/docs/SAP_S4HANA_CLOUD/0f69f8fb28ac4bf48d2b57b9637e81fa/32afd67be8dc4e66890171e9924098f6.html) . Refer to [Integration](../integration/integration-a504461.md) for more information on the integrations applications provide.

To obtain the relevant information for establishing the connection, open the service binding by clicking on its name. Proceed as follows:

If you are using certificate-based authentication with an auto-generated certificate, the relevant fields are the following:

-   `uri` — the URL for the SAP Master Data Integration API.

-   `certurl` in the `uaa` section — the URL for authenticating the client and obtaining an access token for the SAP Master Data Integration API.

-   `clientid` in the `uaa` section — the OAuth2 client ID.

-   `key` in the `uaa` section — the private key for authentication.

-   `certificate` in the `uaa` section — the certificate \(with public key\) for authentication.


If you are using client ID and client secret for authentication, the relevant fields are the following:

-   `uri` — the URL for the SAP Master Data Integration API.

-   `url` in the `uaa` section — the URL for authenticating the client and obtaining an access token for the SAP Master Data Integration API.

-   `clientid` in the `uaa` section — the OAuth2 client ID.

-   `clientsecret` in the `uaa` section — the OAuth2 client secret.


For further details on available authentication methods, refer to [OAuth2-based Authentication](oauth2-based-authentication-7701dff.md) .

> ### Caution:  
> The newly connected client does not yet have permissions to access data. Refer to [Maintenance of the Distribution Model in SAP Master Data Orchestration](configuring-distribution-models-b033b0a.md) for more details on how to provide the desired permissions.

