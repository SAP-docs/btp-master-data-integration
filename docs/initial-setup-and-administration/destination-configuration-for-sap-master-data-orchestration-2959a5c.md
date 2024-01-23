<!-- loio2959a5c628024e39bcac60e3e7e85ba7 -->

# Destination Configuration for SAP Master Data Orchestration



Consumer destinations are the destinations of the connected systems to which the data will be distributed. Here, users need to maintain the destinations per service instance created in the [Connecting Applications](connecting-applications-69ae614.md) steps, to which SOAP message has to be sent for each of the system, where data will be replicated. The details of interfaces to be configured are provided in the Note section below. Follow the steps below for configuration in SAP Business Technology Platform:

1.  Navigate to the subaccount in SAP BTP cockpit.
2.  Navigate to *Connectivity* \> *Destinations*.
3.  Choose *New Destination* and enter the mandatory details as follows:
    1.  Name: <businessSystemId\>\_BPOUTBOUND. For example, <C4CSYSTEMID\>\_BPOUTBOUND.

        > ### Note:  
        > The Business System name should be same as the one used while creating that particular Service Instance.

    2.  Type: HTTP
    3.  URL: Service endpoint of connected system

        > ### Note:  
        > Use the endpoint configured in the connected system to communicate with SAP Master Data Integration.
        > 
        > Example 1: For S/4HANA Cloud system, open a communication arrangement of type SAP\_COM\_0008 and copy the inbound Services URL.
        > 
        > Example 2: For S/4HANA On-premise system, you would need a combination of host name of the system and "Calculated Access URL" configured in SOAManager.
        > 
        > \(https://<Host\_name\>:<Https\_Port\>/Calculated\_Access\_URL. To retrieve HostName execute transaction `smicm` and then Click **Shift F1**\).

    4.  Proxy Type: Internet or OnPremise

        > ### Note:  
        > OnPremise for S/4HANA on-premise system and Internet for S/4HANA cloud system. Cloud Connector Configuration is required for integration to SAP ERP and SAP S/4HANA On-Premise destinations.

    5.  Authentication: <Select Authentication Method\>

        For example: OAuth2/Basic/Client Certificate Authentication. In case BasicAuthentication method is selected and connecting system is S/4HANA, provide Username and password for S/4HANA system in the relevant fileds in the configuration.



> ### Note:  
> Repeat above steps and create the following destinations::
> 
> 
> <table>
> <tr>
> <th valign="top">
> 
> Service Name
> 
> </th>
> <th valign="top">
> 
> Corresponding Destination
> 
> </th>
> </tr>
> <tr>
> <td valign="top">
> 
> Business Partner Confirmation
> 
> </td>
> <td valign="top">
> 
> <businessSystemId\>\_BPCONFIRM
> 
> </td>
> </tr>
> <tr>
> <td valign="top">
> 
> Business Partner Relationship Confirmation
> 
> </td>
> <td valign="top">
> 
> <businessSystemId\>\_BPRELCONFIRM
> 
> </td>
> </tr>
> <tr>
> <td valign="top">
> 
> Business Partner Relationship Replicate
> 
> </td>
> <td valign="top">
> 
> <businessSystemId\>\_BPRELOUTBOUND
> 
> </td>
> </tr>
> <tr>
> <td valign="top">
> 
> Key Mapping Confirmation
> 
> </td>
> <td valign="top">
> 
> <businessSystemId\>\_KEYMAPCONFIRM
> 
> </td>
> </tr>
> <tr>
> <td valign="top">
> 
> Key Mapping
> 
> </td>
> <td valign="top">
> 
> <businessSystemId\>\_KMOUTBOUND
> 
> </td>
> </tr>
> </table>

> ### Note:  
> Refer to *Cloud Connector* in [https://help.sap.com/viewer/index](https://help.sap.com/viewer/index) *SAP BTP Connectivity* \> *Integration*

**Related Information**  


[Creating MDO Distribution Model for Business Partner Replication](creating-mdo-distribution-model-for-business-partner-replication-659f09e.md "")

