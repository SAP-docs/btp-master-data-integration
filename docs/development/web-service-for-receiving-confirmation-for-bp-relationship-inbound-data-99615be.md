<!-- loio99615becc4ed4d5899782079fcf5edf1 -->

# Web Service for Receiving Confirmation for BP Relationship Inbound Data

Inbound Interface for Business Partner Relationships Data Replication Confirmation

Inbound Interface for Business Partner Relationships Data Replication Confirmation



<a name="loio99615becc4ed4d5899782079fcf5edf1__description"/>

## Description

Technical name: `BusinessPartnerRelationshipSUITEBulkReplicateConfirmation_In` 

This service enables you to get the status of Business Partner relationship data replication from the client system to the SAP Master Data Integrationn - Business Partners system. It is based on the SOAP protocol.



<a name="loio99615becc4ed4d5899782079fcf5edf1__service-structure"/>

## Service Structure

This inbound interface uses the operation, Inbound Operation for Business Partner Relationship Confirmation Data \( `BusinessPartnerRelationshipSUITEBulkReplicateConfirmation_In` \).



<a name="loio99615becc4ed4d5899782079fcf5edf1__service-message-header"/>

## Service Message Header

The service message header contains information on the service, the involved sender and receiver as well as date and time.



<a name="loio99615becc4ed4d5899782079fcf5edf1__service-nodes"/>

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

BusinessPartnerRelationship

</td>
<td valign="top">

Node that contains details of relationship between two Business Partners

</td>
<td valign="top">

[BusinessPartnerRelationshipSUITEBulkReplicateConfirmation - BusinessPartnerRelationship](web-service-for-receiving-confirmation-for-bp-relationship-inbound-data-99615be.md#loio99615becc4ed4d5899782079fcf5edf1__businesspartnerrelationshipsuitebulkreplicateconfirmation---businesspartnerrelationship) 

</td>
</tr>
<tr>
<td valign="top">

ContactPerson

</td>
<td valign="top">

Line item for contact person

</td>
<td valign="top">

[BusinessPartnerRelationshipSUITEBulkReplicateConfirmation - ContactPerson](web-service-for-receiving-confirmation-for-bp-relationship-inbound-data-99615be.md#loio99615becc4ed4d5899782079fcf5edf1__businesspartnerrelationshipsuitebulkreplicateconfirmation---contactperson) 

</td>
</tr>
</table>



<a name="loio99615becc4ed4d5899782079fcf5edf1__restrictions"/>

## Restrictions

This service interface is released with restrictions. For more information, contact your SAP system administrator.



<a name="loio99615becc4ed4d5899782079fcf5edf1__businesspartnerrelationshipsuitebulkreplicateconfirmation---businesspartnerrelationship"/>

## BusinessPartnerRelationshipSUITEBulkReplicateConfirmation - BusinessPartnerRelationship

This service node contains the following parameters.



<a name="loio99615becc4ed4d5899782079fcf5edf1__parameters"/>

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

BusinessPartnerUUID

</td>
<td valign="top">

Business Partner UUID in the sender business system

</td>
<td valign="top">

Optional

</td>
</tr>
<tr>
<td valign="top">

BusinessPartnerInternalID

</td>
<td valign="top">

Business Partner Number in the sender business system

</td>
<td valign="top">

Optional

</td>
</tr>
<tr>
<td valign="top">

ReceiverBusinessPartnerUUID

</td>
<td valign="top">

Business Partner UUID in the receiver business system

</td>
<td valign="top">

Optional

</td>
</tr>
<tr>
<td valign="top">

ReceiverBusinessPartnerInternalID

</td>
<td valign="top">

Business Partner Number in the receiver business system

</td>
<td valign="top">

Optional

</td>
</tr>
<tr>
<td valign="top">

RelatedBusinessPartnerUUID

</td>
<td valign="top">

UUID of the related Business Partner in the sender business system

</td>
<td valign="top">

Optional

</td>
</tr>
<tr>
<td valign="top">

RelatedBusinessPartnerInternalID

</td>
<td valign="top">

Business Partner number of the Business Partner for which relationship is created \(Sender Business System\)

</td>
<td valign="top">

Optional

</td>
</tr>
<tr>
<td valign="top">

ReceiverRelatedBusinessPartnerUUID

</td>
<td valign="top">

UUID of the related Business Partner in the Receiver Business System

</td>
<td valign="top">

Optional

</td>
</tr>
<tr>
<td valign="top">

ReceiverRelatedBusinessPartnerInternalID

</td>
<td valign="top">

Business Partner Number of the related Business Partner in the Receiver Business System

</td>
<td valign="top">

Optional

</td>
</tr>
<tr>
<td valign="top">

RoleCode

</td>
<td valign="top">

Business Partner Relationship Category; The business partner relationship category characterizes the features of the relationship. For example, Is child of, has contact person etc.

</td>
<td valign="top">

Optional

</td>
</tr>
<tr>
<td valign="top">

BusinessPartnerExternalID

</td>
<td valign="top">

Partner Number for systems where Business Partner number is greater then 10 characters. In sender business system Business Partner No is less than or equal to 10 character. For example, SAP Hybris

</td>
<td valign="top">

Optional

</td>
</tr>
<tr>
<td valign="top">

RelatedBusinessPartnerExternalID

</td>
<td valign="top">

Partner Number of the related Business Partner. Used for systems where Business Partner number is greater then 10 characters. In sender business system Business Partner No is less than or equal to 10 character. For example, SAP Hybris

</td>
<td valign="top">

Optional

</td>
</tr>
<tr>
<td valign="top">

ValidityPeriod

</td>
<td valign="top">

Validity Start Date and End Date

</td>
<td valign="top">

Optional

</td>
</tr>
</table>



<a name="loio99615becc4ed4d5899782079fcf5edf1__businesspartnerrelationshipsuitebulkreplicateconfirmation---contactperson"/>

## BusinessPartnerRelationshipSUITEBulkReplicateConfirmation - ContactPerson

This service node contains the following parameters.



<a name="loio99615becc4ed4d5899782079fcf5edf1__parameters-1"/>

## Parameters


<table>
<tr>
<th valign="top">

Parameter

</th>
<th valign="top">



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

CustomerContactPerson

</td>
<td valign="top">

InternalID

</td>
<td valign="top">

Contact Person number helps to uniquely identify the contact person if it has Customer role \(FLCU00, FLCU01\) in sender system.

</td>
<td valign="top">

Optional

</td>
</tr>
<tr>
<td valign="top">



</td>
<td valign="top">

ReceiverInternalID

</td>
<td valign="top">

Contact Person number helps to uniquely identify the contact person if it has Customer role \(FLCU00, FLCU01\) in receiver system

</td>
<td valign="top">

Optional

</td>
</tr>
<tr>
<td valign="top">

SupplierContactPerson

</td>
<td valign="top">

InternalID

</td>
<td valign="top">

Contact Person number helps to uniquely identify the contact person if it has Supplier role \(FLVN00,FLVN01\) in sender system

</td>
<td valign="top">

Optiona

</td>
</tr>
<tr>
<td valign="top">



</td>
<td valign="top">

ReceiverInternalID

</td>
<td valign="top">

Contact Person number helps to uniquely identify the contact person if it has Supplier role \(FLVN00,FLVN01\) in receiver system

</td>
<td valign="top">

Optional

</td>
</tr>
</table>

