<!-- loio870fed9ab8c34d08acd1dc4cbf95708a -->

# Configuring Destinations for SOAP

Consumer destinations are the destinations of the connected systems to which the data will be distributed. Maintaining destinations allows SAP Master Data Integration to securely access the remote connected systems that run on the Internet or on-premise.

> ### Note:  
> A destination for SAP Master Data Integration is only needed for SOAP based integrations for the Business Partner model or if it is part of the respective application integration guide \(for improved SAP Master Data Orchestration compatibility\). For SOAP based integrations, each unique client connection can have maximum of six destinations. Please refer the table at the end of this document for list of destinations.



<a name="loio870fed9ab8c34d08acd1dc4cbf95708a__consumer-destination-for-business-partner"/>

## Consumer Destination for Business Partner



<a name="loio870fed9ab8c34d08acd1dc4cbf95708a__context"/>

## Context

Set up the destination to connect SAP Master Data Integration with the connected client.



<a name="loio870fed9ab8c34d08acd1dc4cbf95708a__procedure"/>

## Procedure

1.  Navigate to the subaccount in SAP BTP cockpit.

2.  Navigate to **Connectivity \> Destinations** .

3.  Choose **New Destination** and enter the mandatory details as follows:

4.  Name: `<businessSystemId>_BPOUTBOUND` . For example, `<C4CSYSTEMID>_BPOUTBOUND` .


> ### Note:  
> The Business System name should be same as the one used while creating that particular SAP Master Data Integration service instance.

1.  Type: HTTP

2.  URL: Service endpoint of connected client


> ### Note:  
> Use the endpoint configured in the connected client to communicate with SAP Master Data Integration.
> 
> Example 1: For S/4HANA Cloud, open a communication arrangement of type SAP\_COM\_0008 and copy the inbound services URL. Example 2: For S/4HANA On-premise, you would need a combination of host name of the system and "Calculated Access URL" configured in SOAManager. \( `https://<Host_name>:<Https_Port>/Calculated_Access_URL` . To retrieve `HostName` execute transaction `smicm` and then Click `Shift + F1` \).

1.  Proxy Type: Internet or OnPremise


> ### Note:  
> -   For more information on proxy type, see **SAP BTP Connectivity \> [HTTP Destinations](https://help.sap.com/docs/connectivity/sap-btp-connectivity-cf/http-destinations?locale=en-US#proxy-types) ** .
> 
> -   Cloud Connector Configuration is required for integration to SAP ERP and SAP S/4HANA destinations. For more information, see **SAP BTP Connectivity \> [Cloud Connector](https://help.sap.com/docs/connectivity/sap-btp-connectivity-cf/cloud-connector) ** .
> 
> -   Choose `OnPremise` for SAP S/4HANA system and `Internet` for SAP S/4HANA cloud system.
> 
> -   For the `Internet` proxy type, always use HTTPS in the service endpoint URL. For the `OnPremise` proxy type, always use HTTPs or HTTP in the service endpoint URL.

1.  Authentication: `<Select Authentication Method>` 

    For example: `OAuth2/ Basic/ Client Certificate Authentication` . For details refer the [Configuring Authentication](https://help.sap.com/docs/connectivity/sap-btp-connectivity-cf/http-destinations?locale=en-US#configuring-authentication) section in this help page.


> ### Note:  
> Repeat above steps and create the following destinations based on the integration scenario :


<table>
<tr>
<th valign="top">

Service Name

</th>
<th valign="top">

Corresponding Destination

</th>
<th valign="top">

Context

</th>
</tr>
<tr>
<td valign="top">

Business Partner Replicate

</td>
<td valign="top">

`<businessSystemId>_BPOUTBOUND` 

</td>
<td valign="top">

Send BP outbound message to the sender client upon successful replication to MDI

</td>
</tr>
<tr>
<td valign="top">

Business Partner Confirmation

</td>
<td valign="top">

`<businessSystemId>_BPCONFIRM` 

</td>
<td valign="top">

Send BP confirmation message to the sender client upon successful replication to MDI

</td>
</tr>
<tr>
<td valign="top">

Business Partner Relationship Replicate

</td>
<td valign="top">

`<businessSystemId>_BPRELOUTBOUND` 

</td>
<td valign="top">

Send BP Relationship outbound message to target client

</td>
</tr>
<tr>
<td valign="top">

Business Partner Relationship Confirmation

</td>
<td valign="top">

`<businessSystemId>_BPRELCONFIRM` 

</td>
<td valign="top">

Send BP Relationship confirmation message to the sender client upon successful replication to MDI

</td>
</tr>
<tr>
<td valign="top">

Key Mapping Replicate

</td>
<td valign="top">

`<businessSystemId>_KMOUTBOUND` 

</td>
<td valign="top">

Send Key Mapping outbound message to target client

</td>
</tr>
<tr>
<td valign="top">

Key Mapping Confirmation

</td>
<td valign="top">

`<businessSystemId>_KEYMAPCONFIRM` 

</td>
<td valign="top">

Send Key Mapping confirmation message to the sender client upon successful replication to MDI

</td>
</tr>
</table>

