<!-- loioac332c2014e0441aa9ffc38e36c4f60a -->

# Glossary


<table>
<tr>
<th valign="top">

Term

</th>
<th valign="top">

Description

</th>
</tr>
<tr>
<td valign="top">

Change event

</td>
<td valign="top">

An event published by SAP Master Data Integration service about changes to the master data database. Clients typically process change events to update their databases.

</td>
</tr>
<tr>
<td valign="top">

Change operation

</td>
<td valign="top">

An identifier for a specific command type to be executed on a master data record. Example values include `create` , `patch` or `delete` .

</td>
</tr>
<tr>
<td valign="top">

Change request

</td>
<td valign="top">

A command sent by a client to Master Data Integration service in order to create, modify, or delete a master data record in the master data database.

</td>
</tr>
<tr>
<td valign="top">

Client

</td>
<td valign="top">

An application or service that integrates with SAP Master Data Integration in order to synchronize its master data database with the master data database of the SAP Master Data Integration tenant.

</td>
</tr>
<tr>
<td valign="top">

Producing client

</td>
<td valign="top">

A client that sends change requests or SOAP messages to SAP Master Data Integration service. *Synonyms:* Upstream client, Sending client, Writing client

</td>
</tr>
<tr>
<td valign="top">

Consuming client

</td>
<td valign="top">

A client that receives change events or SOAP messages from SAP Master Data Integration service. *Synonyms:* Downstream client, Receiving client, Reading client

</td>
</tr>
<tr>
<td valign="top">

Key Mapping

</td>
<td valign="top">

The linking of the identifying keys of object instances that represent identical real-world objects in different clients. You can maintain one or more keys in each client.

</td>
</tr>
<tr>
<td valign="top">

Master Data Record

</td>
<td valign="top">

Data or information about a real-world object. A master data record can, for instance, describe a specific cost center or a specific business partner.

</td>
</tr>
<tr>
<td valign="top">

Master Data Type

</td>
<td valign="top">

The type of master data entities. For example, cost center, bank etc. *Synonyms:* Master Data Object, Business Object, Entity Type

</td>
</tr>
<tr>
<td valign="top">

Tenant

</td>
<td valign="top">

SAP Master Data Integration service is a multi-tenant cloud service. Each tenant of SAP Master Data Integration maintains its own data that is not shared with other tenants. Each tenant in particular has its own master data database, tenant configurations, and client configurations.

</td>
</tr>
</table>

