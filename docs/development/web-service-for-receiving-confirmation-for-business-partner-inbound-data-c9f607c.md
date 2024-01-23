<!-- loioc9f607c9f22a496b89e14022de1836fa -->

# Web Service for Receiving Confirmation for Business Partner Inbound Data



<a name="loioc9f607c9f22a496b89e14022de1836fa__description"/>

## Description

Technical name: `BusinessPartnerSUITEBulkReplicateConfirmation_In` 

This service enables you to get the status of Business Partner data replication from the client system to the SAP Master Data Integration - Business Partners system. It is based on the SOAP protocol.



<a name="loioc9f607c9f22a496b89e14022de1836fa__service-structure"/>

## Service Structure

Inbound interface for Business Partner Confirmation Data \( `BusinessPartnerSUITEBulkReplicateConfirmation_In` \).



<a name="loioc9f607c9f22a496b89e14022de1836fa__service-message-header"/>

## Service Message Header

The service message header contains information on the service, the involved sender and receiver as well as date and time.



<a name="loioc9f607c9f22a496b89e14022de1836fa__service-nodes"/>

## Service Nodes

The service nodes contain the business data of the service.


<table>
<tr>
<th valign="top">

Service Node

</th>
<th valign="top">

Description

</th>
<th valign="top">

Link to Details

</th>
</tr>
<tr>
<td valign="top">

BusinessPartner

</td>
<td valign="top">

Node element containing Business Partner details

</td>
<td valign="top">

[BusinessPartnerSUITEBulkReplicateConfirmation - BusinessPartner](web-service-for-receiving-confirmation-for-business-partner-inbound-data-c9f607c.md#loioc9f607c9f22a496b89e14022de1836fa__businesspartnersuitebulkreplicateconfirmation---businesspartner) 

</td>
</tr>
<tr>
<td valign="top">

Customer

</td>
<td valign="top">

Line item Customer

</td>
<td valign="top">

[BusinessPartnerSUITEBulkReplicateConfirmation - Customer](web-service-for-receiving-confirmation-for-business-partner-inbound-data-c9f607c.md#loioc9f607c9f22a496b89e14022de1836fa__businesspartnersuitebulkreplicateconfirmation---customer) 

</td>
</tr>
<tr>
<td valign="top">

Supplier

</td>
<td valign="top">

Line item Supplier

</td>
<td valign="top">

[BusinessPartnerSUITEBulkReplicateConfirmation - Supplier](web-service-for-receiving-confirmation-for-business-partner-inbound-data-c9f607c.md#loioc9f607c9f22a496b89e14022de1836fa__businesspartnersuitebulkreplicateconfirmation---supplier) 

</td>
</tr>
</table>



<a name="loioc9f607c9f22a496b89e14022de1836fa__restrictions"/>

## Restrictions

This service interface is released with restrictions. For more information, contact your SAP system administrator.



<a name="loioc9f607c9f22a496b89e14022de1836fa__businesspartnersuitebulkreplicateconfirmation---businesspartner"/>

## BusinessPartnerSUITEBulkReplicateConfirmation - BusinessPartner

This service node contains the following parameters.



<a name="loioc9f607c9f22a496b89e14022de1836fa__parameters"/>

## Parameters


<table>
<tr>
<th valign="top">

Parameter

</th>
<th valign="top">

Description

</th>
<th valign="top">

Necessity

</th>
</tr>
<tr>
<td valign="top">

UUID

</td>
<td valign="top">

Business Partner UUID in the sender system

</td>
<td valign="top">

Optional

</td>
</tr>
<tr>
<td valign="top">

InternalID

</td>
<td valign="top">

Business Partner Number in sender system

</td>
<td valign="top">

Optional

</td>
</tr>
<tr>
<td valign="top">

ReceiverUUID

</td>
<td valign="top">

Business Partner UUID in receiver system

</td>
<td valign="top">

Optional

</td>
</tr>
<tr>
<td valign="top">

ExternalID

</td>
<td valign="top">

Business Partner number for systems where Business Partner number is greater then 10 characters. In SAP S/4HANA, Business Partner Number is less than or equal to 10 character. For example, SAP Hybris

</td>
<td valign="top">

Optional

</td>
</tr>
<tr>
<td valign="top">

ReceiverInternalID

</td>
<td valign="top">

Business Partner Number in receiver system

</td>
<td valign="top">

Optional

</td>
</tr>
</table>



<a name="loioc9f607c9f22a496b89e14022de1836fa__businesspartnersuitebulkreplicateconfirmation---customer"/>

## BusinessPartnerSUITEBulkReplicateConfirmation - Customer

This service node contains the following parameters.



<a name="loioc9f607c9f22a496b89e14022de1836fa__parameters-1"/>

## Parameters


<table>
<tr>
<th valign="top">

Parameter

</th>
<th valign="top">

Description

</th>
<th valign="top">

Necessity

</th>
</tr>
<tr>
<td valign="top">

InternalID

</td>
<td valign="top">

Customer number of the sender system \(for related Business Partner\)

</td>
<td valign="top">

Optional

</td>
</tr>
<tr>
<td valign="top">

ReceiverInternalID

</td>
<td valign="top">

Customer number of the receiver system \(for related Business Partner\)

</td>
<td valign="top">

Optional

</td>
</tr>
</table>



<a name="loioc9f607c9f22a496b89e14022de1836fa__businesspartnersuitebulkreplicateconfirmation---supplier"/>

## BusinessPartnerSUITEBulkReplicateConfirmation - Supplier

This service node contains the following parameters.



<a name="loioc9f607c9f22a496b89e14022de1836fa__parameters-2"/>

## Parameters


<table>
<tr>
<th valign="top">

Parameter

</th>
<th valign="top">

Description

</th>
<th valign="top">

Necessity

</th>
</tr>
<tr>
<td valign="top">

InternalID

</td>
<td valign="top">

Supplier number in the sender system \(for related Business Partner\)

</td>
<td valign="top">

Optional

</td>
</tr>
<tr>
<td valign="top">

ReceiverInternalID

</td>
<td valign="top">

Supplier number in the receiver system \(for related Business Partner\)

</td>
<td valign="top">

Optional

</td>
</tr>
</table>

