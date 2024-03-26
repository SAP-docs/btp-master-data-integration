<!-- loio6caf1450badb467f8b00fcd203c76925 -->

# Endpoints for SOAP Replication for Business Partners

Basic Authentication and OAuth authentication are supported for the mentioned endpoints here. Refer to your service keys for the **clientid** and the **clientsecret** . In Basic Authentication: **username** is the **clientid** and **password** is the **clientsecret** from your service keys.

> ### Note:  
> If you are using Basic Authentication, the URL query parameter **tenandId** is needed. For example:
> 
> ```
> https://one-mds.cfapps.<region>.hana.ondemand.com:443/businesspartner/v0/soap/BusinessPartnerBulkReplicateRequestIn?tenantId=<identityzone>
> ```

Following are the endpoints for SOAP replication in SAP Master Data Integration - Business Partners. You can call these endpoints through HTTP POST requests:

All values required can be retrieved from **SAP BTP Cockpit \> Subaccount \> Spaces \> Service \> Service Instance \> Service Keys** :

-   TenantHost/Subdomain: Value corresponding to identityzone

-   tenantId: Value corresponding to identityzone

-   BusinessSystemName/SourceSystem: Value for own system



<table>
<tr>
<th valign="top">

Endpoint

</th>
<th valign="top">

Sample Code

</th>
</tr>
<tr>
<td valign="top">

BusinessPartner Inbound

</td>
<td valign="top">

`https://one-mds.cfapps.{region}.hana.ondemand.com/businesspartner/v0/soap/BusinessPartnerBulkReplicateRequestIn` 

</td>
</tr>
<tr>
<td valign="top">

BusinessPartner Confirmation Inbound

</td>
<td valign="top">

`https://one-mds.cfapps.{region}.hana.ondemand.com/businesspartner/v0/soap/sinessPartnerBulkReplicateRequestConfIn` 

</td>
</tr>
<tr>
<td valign="top">

BusinessPartner Relationship Inbound

</td>
<td valign="top">

`https://one-mds.cfapps.{region}.hana.ondemand.com/businesspartner/v0/soap/BusinessPartnerRelationshipBulkReplicateRequestIn` 

</td>
</tr>
<tr>
<td valign="top">

BusinessPartner Relationship Confirmation Inbound

</td>
<td valign="top">

`https://one-mds.cfapps.{region}.hana.ondemand.com/businesspartner/v0/soap/BusinessPartnerRelationshipBulkReplicateRequestConfirmIn` 

</td>
</tr>
<tr>
<td valign="top">

KeyMapping Inbound

</td>
<td valign="top">

`https://one-mds.cfapps.{region}.hana.ondemand.com/businesspartner/v0/soap/KeyMappingBulkReplicateRequestIn` 

</td>
</tr>
<tr>
<td valign="top">

KeyMapping Confirmation Inbound

</td>
<td valign="top">

`https://one-mds.cfapps.{region}.hana.ondemand.com/businesspartner/v0/soap/KeyMappingBulkReplicateRequestConfirmIn` 

</td>
</tr>
</table>

