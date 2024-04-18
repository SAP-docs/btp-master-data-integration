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
<th valign="top">

Synonyms

</th>
</tr>
<tr>
<td valign="top">

Change event

</td>
<td valign="top">

An event about changes to the master data database published by SAP Master Data Integration service. Clients usually process change events to update their databases.

</td>
<td valign="top">

 

</td>
</tr>
<tr>
<td valign="top">

Change operation

</td>
<td valign="top">

An identifier for a specific command type to be executed on a master data record. Example values include `create` , `patch` or `delete` .

</td>
<td valign="top">

 

</td>
</tr>
<tr>
<td valign="top">

Change request

</td>
<td valign="top">

A command sent by a client to Master Data Integration service to create, modify, or delete a master data record in the master data database.

</td>
<td valign="top">

 

</td>
</tr>
<tr>
<td valign="top">

Client

</td>
<td valign="top">

An application or service that integrates with SAP Master Data Integration to synchronize its master data database with the master data database of the SAP Master Data Integration tenant.

</td>
<td valign="top">

 

</td>
</tr>
<tr>
<td valign="top">

Producing client

</td>
<td valign="top">

A client that sends change requests or SOAP messages to the SAP Master Data Integration service.

</td>
<td valign="top">

Upstream client, Sending client, Writing client

</td>
</tr>
<tr>
<td valign="top">

Consuming client

</td>
<td valign="top">

A client that receives change events or SOAP messages from the SAP Master Data Integration service.

</td>
<td valign="top">

Downstream client, Receiving client, Reading client

</td>
</tr>
<tr>
<td valign="top">

Key Mapping

</td>
<td valign="top">

The linking of the identifying keys of object instances that represent identical real-world objects in different clients. You can maintain one or more keys in each client.

</td>
<td valign="top">

 

</td>
</tr>
<tr>
<td valign="top">

Master Data Record

</td>
<td valign="top">

Data or information about a real-world object. A master data record can, for instance, describe a specific cost center or a specific business partner.

</td>
<td valign="top">

 

</td>
</tr>
<tr>
<td valign="top">

Master Data Type

</td>
<td valign="top">

The type of master data entities. For example, cost center, bank etc.

</td>
<td valign="top">

Master Data Object, Business Object, Entity Type

</td>
</tr>
<tr>
<td valign="top">

Tenant

</td>
<td valign="top">

SAP Master Data Integration service is a multitenant cloud service. Each tenant of SAP Master Data Integration maintains its own data that is not shared with other tenants. Each tenant in particular has its own master data database, tenant configurations, and client configurations.

</td>
<td valign="top">

 

</td>
</tr>
</table>

