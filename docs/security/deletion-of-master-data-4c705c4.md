<!-- loio4c705c45b63946708a1d9dc26cfa9695 -->

# Deletion of Master Data

The main responsibility of SAP Master Data Integration is to enable applications to synchronize their master data. As master data potentially contains personal data, SAP Master Data Integration provides features that can be used by integrating applications or administrators to permanently delete data.

Master Data that gets deleted by using corresponding features is deleted permanently after 28 days. This is for both the deletion of a record and the deletion of an attribute of a record.

Consuming clients are informed about the deletion so that they can react accordingly. However, within the 28 days period, it might happen that the service distributes already deleted master data. This can happen if there are multiple changes occurring between two subsequent delta loads of a consuming client.

Delta tokens expire after 28 days. Clients that did not synchronize for 28 days will get an error response indicating that the delta token is outdated. Those clients have to perform an initial load.



<a name="loio4c705c45b63946708a1d9dc26cfa9695__disconnecting-clients-deletion-of-master-data-records"/>

## Disconnecting Clients: Deletion of Master Data Records

Master data is not automatically deleted from SAP Master Data Integration at the time of disconnecting clients, provided there are still active Master Data Integration service instances. For more information on disconnecting clients, see [Disconnecting Applications](../initial-setup-and-administration/disconnecting-applications-d09d7b9.md).

To support data protection and privacy requirements \(in particular w.r.t. data deletion\), we recommend the following activities to be performed by customers before disconnecting a client:

-   Determine all master data in the overall client landscape, which potentially would not be required by other clients connected to the same Master Data Integration tenant. This data would not serve any business purpose after the previously mentioned client is off-boarded.

-   Customer should ensure deletion of such data when disconnecting the client.

    -   Deletion of master data can be initiated via client leveraging Master Data Integration.

    -   For business partner master data, deletion of records can only be initiated via S/4HANA client. For more information, refer to [Deletion of Business Partner in Master Data Integration](deletion-of-master-data-4c705c4.md#loio4c705c45b63946708a1d9dc26cfa9695__deletion-of-business-partner-in-master-data-integration).





<a name="loio4c705c45b63946708a1d9dc26cfa9695__deletion-of-master-data-records-in-master-data-integration"/>

## Deletion of Master Data Records in Master Data Integration

The main responsibility of SAP Master Data Integration is to maintain a consistent state with regards to master data across connected clients by distributing change events. Change events may contain personal data, therefore Master Data Integration also needs to guarantee that personal data gets deleted. In order to balance between these requirements, the service applies a general deletion strategy.

-   Deletion of master data records can be triggered by a client connected to Master Data Integration.

-   After successfully processing a delete request from a client, Master Data Integration informs all downstream clients that have access to this record about this deletion event.

-   Each downstream client is expected to take care of deletion in local persistence upon receiving the corresponding event from Master Data Integration.

-   Deletion events can only be retrieved by clients within 28 days after the deletion of a master data record.




<a name="loio4c705c45b63946708a1d9dc26cfa9695__deletion-of-business-partner-in-master-data-integration"/>

## Deletion of Business Partner in Master Data Integration

In SAP Master Data Integration, the deletion of a business partner record is a consequence of a request to block the record.

Blocking means restricting access to data under the condition that processing of personal data is no longer required for its primary business purpose. This condition is called "end of purpose".

SAP Master Data Integration leverages SAP Data Retention Manager service to check for end of purpose of business partners. Refer to [SAP Data Retention Manager](https://help.sap.com/docs/DATA_RETENTION_MANAGER/7b96239812444caf9dc36faa15292a2f/08ad7d7ecfc740518d060d57e3f3e7a1.html) for more information on business purposes and related terminology.

SAP Master Data Integration only supports requests to block and check for end of purpose initiated by SAP S/4HANA clients.

> ### Note:  
> SAP Data Retention Manager can check end of purpose only for SAP-branded cloud applications.

> ### Note:  
> Refer to section "2.1. Deletion of Business Partner in Master Data Integration" in SAP Note [2954816](https://launchpad.support.sap.com/#/notes/2954816) to learn more about the restrictions to deletion of business partner records.



<a name="loio4c705c45b63946708a1d9dc26cfa9695__related-information"/>

## Related Information

For more information, see [SAP Data Retention Manager](https://help.sap.com/viewer/product/DATA_RETENTION_MANAGER/SHIP/en-US).



<a name="loio4c705c45b63946708a1d9dc26cfa9695__configuration-for-sap-s4hana"/>

## Configuration for SAP S/4HANA

To maintain ILM configuration for blocking and deletion in the SAP S/4HANA client, refer to [SAP Information Lifecycle Management](https://help.sap.com/viewer/7ce8e5dc89d7407e8baa9de7b775f31f/LATEST/en-US/7fe188e04fdd462e8ec330bb80efc389.html).



<a name="loio4c705c45b63946708a1d9dc26cfa9695__soa-manager-configuration-for-blocking-and-end-of-purpose-check-interfaces"/>

## SOA Manager Configuration for Blocking and End-of-Purpose Check Interfaces

Once you complete the ILM configuration, you need to configure SOA Manager, which is required to send end of purpose check and block request to the SAP Master Data Integration tenant.

*Proxy Information for SOA Manager Configuration* 


<table>
<tr>
<th valign="top">

Internal Name

</th>
<th valign="top">

Name

</th>
<th valign="top">

Namespace

</th>
<th valign="top">

Description

</th>
</tr>
<tr>
<td valign="top">

CO\_ABABUSINESS\_PARTNER\_EOPREMO

</td>
<td valign="top">

ABABusinessPartnerEOPRemoteOut

</td>
<td valign="top">

`http://sap.com/xi/ABA` 

</td>
<td valign="top">

End of purpose check for business partner

</td>
</tr>
<tr>
<td valign="top">

CO\_ABABUSINESS\_PARTNER\_EOPCOMP

</td>
<td valign="top">

ABABusinessPartnerEOPComplout

</td>
<td valign="top">

`http://sap.com/xi/ABA` 

</td>
<td valign="top">

Block business partner

</td>
</tr>
</table>



<a name="loio4c705c45b63946708a1d9dc26cfa9695__configuration-steps"/>

## Configuration Steps

1.  **SOAManager** Open transaction.

2.  **Service Administration** **Web Service Configuration** On thetab, choose.

3.  **Design Time Object Search** **Object Type** **Consumer Proxy** **Object Name** **ABABusinessPartnerEOPRemoteOut** On thetab, selectasfrom the dropdown and giveas.

4.  **Define Logical Ports** **Manual Configuration** **Create** In thescreen, selectfrom thedropdown.

5.  Give logical port name and description.

6.  **Consumer Security** **Authentication Settings** **User ID / Password** In, selectasand give the SAP Master Data Integration ClientID as username and Client Secret as password of your tenant.

7.  `<mdi_url>/businesspartner/v0/soap/BusinessPartnerResponseEOPRemoteIn?tenantId={subdomain_name}` Provide the URL in this format:


1.  In SOAP Protocol tab, select the following values:

    -   Message ID Protocol: SAP Message ID

    -   Data Transfer Scope: Basic Data Transfer

    -   Transfer Protocol: Transfer via SOAP Header


2.  **Finish** Choose.


> ### Note:  
> For the other interface, use the below table to configure the URL in the required format. It can be fetched from “uri” present in service keys of the service instance.

> ### Note:  
> The correctness of the configuration can be checked using “ping web service”. A 403 response indicates correct configuration.


<table>
<tr>
<th valign="top">

> Name

</th>
<th valign="top">

> URL

</th>
</tr>
<tr>
<td valign="top">

> ABABusinessPartnerEOPComplout

</td>
<td valign="top">

> `<mdi_url>/businesspartner/v0/soap/BusinessPartnerEOPComplIn?tenantId={subdomain_name}` 

</td>
</tr>
</table>

