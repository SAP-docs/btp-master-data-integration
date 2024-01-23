<!-- loio12144699a37b42cf89afb2ec5d447a74 -->

# Web Service for Replicating Key Mapping Inbound Data

`KeyMappingBulkReplicateRequest_In` Technical name:

This service enables you to receive key mapping of supported business object types in the receiver client from the sender client. It is based on the SOAP protocol.



<a name="loio12144699a37b42cf89afb2ec5d447a74__service-structure"/>

## Service Structure



<a name="loio12144699a37b42cf89afb2ec5d447a74__service-message-header"/>

## Service Message Header

The service message header contains information on the service, the involved sender and receiver as well as date and time.



<a name="loio12144699a37b42cf89afb2ec5d447a74__service-nodes"/>

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

Link to details

</th>
</tr>
<tr>
<td valign="top">

MappingGroup

</td>
<td valign="top">

Node that contains key mapping data fields

</td>
<td valign="top">

[KeyMappingBulkReplicateRequest - MappingGroup](web-service-for-replicating-key-mapping-inbound-data-1214469.md#loio12144699a37b42cf89afb2ec5d447a74__keymappingbulkreplicateconfirmation---mapping-group) 

</td>
</tr>
</table>



<a name="loio12144699a37b42cf89afb2ec5d447a74__restrictions"/>

## Restrictions

This service interface is released with restrictions. For more information, contact your SAP system administrator.



<a name="loio12144699a37b42cf89afb2ec5d447a74__keymappingbulkreplicateconfirmation---mapping-group"/>

## KeyMappingBulkReplicateConfirmation - Mapping Group



<a name="loio12144699a37b42cf89afb2ec5d447a74__parameters"/>

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

Key Field

</th>
</tr>
<tr>
<td valign="top">

BusinessSystemID

</td>
<td valign="top">

The system ID in the sender system.

</td>
<td valign="top">

No

</td>
</tr>
<tr>
<td valign="top">

TypeCode

</td>
<td valign="top">

Denotes the business object type. This is also called as Object Type Code \(OTC\). For example, 147 denotes business partner and 197 is material.

</td>
<td valign="top">

No

</td>
</tr>
<tr>
<td valign="top">

ObjectIdentifierSet

</td>
<td valign="top">

A collection of object identifiers.

</td>
<td valign="top">

No

</td>
</tr>
<tr>
<td valign="top">

ObjectIdentifier

</td>
<td valign="top">

An ObjectIdentifier is a combination of object identifier type and key value.

</td>
<td valign="top">

No

</td>
</tr>
<tr>
<td valign="top">

DefiningSchemeCode

</td>
<td valign="top">

Object Identifier Type Code \(OITC\). OITC denotes the chosen business object type. OITC differs based on business object.

</td>
<td valign="top">

No

</td>
</tr>
<tr>
<td valign="top">

KeyValue

</td>
<td valign="top">

The ID value that is defined in the target system.

</td>
<td valign="top">

No

</td>
</tr>
<tr>
<td valign="top">

objectIdentifierListCompleteTransmissionIndicator

</td>
<td valign="top">

Complete transmission defined for object identifier. Indicates whether an object identifier must be transmitted completely.

</td>
<td valign="top">

No

</td>
</tr>
<tr>
<td valign="top">

objectIdentifierSetListCompleteTransmissionIndicator

</td>
<td valign="top">

Complete transmission defined for object identifier set list. Indicates whether an object identifier set must be transmitted completely.

</td>
<td valign="top">

No

</td>
</tr>
<tr>
<td valign="top">

changeOrdinalNumber

</td>
<td valign="top">

Used for In-app sequencing, subsequent changes are sent with incremental number.

</td>
<td valign="top">

No

</td>
</tr>
<tr>
<td valign="top">

reconciliationPeriodCounterValue

</td>
<td valign="top">

Set default value always as 1. Not used for processing.

</td>
<td valign="top">

No

</td>
</tr>
<tr>
<td valign="top">

actionCode

</td>
<td valign="top">

ActionCode attribute controls whether the data is to be created, changed or removed. The key mapping soap Service only supports the value for which data is to be created at the receiver if it does not exist, and to be changed if it exists.

</td>
<td valign="top">

No

</td>
</tr>
<tr>
<td valign="top">

objectListCompleteTransmissionIndicator

</td>
<td valign="top">

Complete transmission defined for an object list. Indicates whether an object must be transmitted completely.

</td>
<td valign="top">

No

</td>
</tr>
</table>

> ### Note:  
> IAMId is now supported in the Key Mapping interface. To exchange IAMId in Key Mapping interface, use the DefiningSchemaCode as CDC\_IAM\_ID.

