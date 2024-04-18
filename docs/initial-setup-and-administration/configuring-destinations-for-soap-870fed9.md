<!-- loio870fed9ab8c34d08acd1dc4cbf95708a -->

# Configuring Destinations for SOAP

A destination for SAP Master Data Integration service is only necessary in two instances:

-   When Business Partner models use SOAP-based integrations.

-   When stated by the respective application integration guide \(for improved SAP Master Data Orchestration compatibility\).


The connected systems to SAP Master Data Integration can be on-premise or cloud systems. All of those systems send their data to one consumer destination. For SAP Master Data Integration service to securely access remote connected systems, consumer destinations must be maintained.

> ### Note:  
> For SOAP-based integrations, each unique client connection can have a maximum of six destinations. Refer to [the table](configuring-destinations-for-soap-870fed9.md#loio870fed9ab8c34d08acd1dc4cbf95708a__integration-scenarios) at the end of this document for list of destinations.



<a name="loio870fed9ab8c34d08acd1dc4cbf95708a__setting-up-the-consumer-destination"/>

## Setting Up the Consumer Destination

These are the steps to set up the destination to connect SAP Master Data Integration with Business Partner.

-   Navigate to the subaccount in SAP BTP cockpit.

-   Navigate to **Connectivity \> Destinations** .

-   Choose **New Destination** and enter the mandatory details as follows:



<table>
<tr>
<th valign="top">

Parameter

</th>
<th valign="top">

Further Information

</th>
</tr>
<tr>
<td valign="top">

Name: `<businessSystemId>_BPOUTBOUND` . For example, `<C4CSYSTEMID>_BPOUTBOUND` .

</td>
<td valign="top">

The Business System name must be the same as for that particular SAP Master Data Integration service instance.

</td>
</tr>
<tr>
<td valign="top">

Type: HTTP

</td>
<td valign="top">

 

</td>
</tr>
<tr>
<td valign="top">

URL: Service endpoint of connected client

</td>
<td valign="top">

To communicate with SAP Master Data Integration, use the endpoint configured in the connected client. 1. Example: For S/4HANA Cloud, open a communication arrangement of type SAP\_COM\_0008 and copy the inbound services URL. 2. Example: For S/4HANA on premise, you need a combination of the host name of the system and "Calculated Access URL" configured in SOAManager. \( `https://<Host_name>:<Https_Port>/Calculated_Access_URL` . To retrieve the `HostName` , execute transaction `smicm` and then Click `Shift + F1` \).

</td>
</tr>
<tr>
<td valign="top">

Authentication: `<Select Authentication Method>` 

</td>
<td valign="top">

For example: `OAuth2/ Basic/ Client Certificate Authentication` . For details refer the [Configuring Authentication](https://help.sap.com/docs/connectivity/sap-btp-connectivity-cf/http-destinations?locale=en-US#configuring-authentication) section in this help page.

</td>
</tr>
</table>



<a name="loio870fed9ab8c34d08acd1dc4cbf95708a__integration-scenarios"/>

## Integration Scenarios

Repeat the steps in [Setting Up the Consumer Destination](configuring-destinations-for-soap-870fed9.md#loio870fed9ab8c34d08acd1dc4cbf95708a__setting-up-the-consumer-destination) and create the following destinations based on the integration scenario:


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

