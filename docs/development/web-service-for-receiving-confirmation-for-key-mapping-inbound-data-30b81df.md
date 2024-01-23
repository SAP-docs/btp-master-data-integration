<!-- loio30b81dfa824645cfb90363613acc1f27 -->

# Web Service for Receiving Confirmation for Key Mapping Inbound Data

Technical name: `KeyMappingBulkReplicateConfirmation_In` 

This service enables you to get the status of key mapping in the receiver client from the sender client. It is based on the SOAP protocol.



<a name="loio30b81dfa824645cfb90363613acc1f27__service-structure"/>

## Service Structure



<a name="loio30b81dfa824645cfb90363613acc1f27__service-message-header"/>

## Service Message Header

The service message header contains information on the service, the involved sender and receiver as well as date and time.



<a name="loio30b81dfa824645cfb90363613acc1f27__service-nodes"/>

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

[KeyMappingBulkReplicateConfirmation - Mapping Group](web-service-for-receiving-confirmation-for-key-mapping-inbound-data-30b81df.md#loio30b81dfa824645cfb90363613acc1f27__keymappingbulkreplicateconfirmation---mapping-group) 

</td>
</tr>
</table>



<a name="loio30b81dfa824645cfb90363613acc1f27__restrictions"/>

## Restrictions

This service interface is released with restrictions. For more information, contact your SAP system administrator.



<a name="loio30b81dfa824645cfb90363613acc1f27__keymappingbulkreplicateconfirmation---mapping-group"/>

## KeyMappingBulkReplicateConfirmation - Mapping Group



<a name="loio30b81dfa824645cfb90363613acc1f27__parameters"/>

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

Denotes the business object type. This is also called as Object Type Code \(OTC\). For example, 147 denotes business partner and 197 is material

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

Object Identifier Type Code \(OITC\). OITC denotes the chosen business object type. OITC differs based on business. object

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
</table>

