<!-- loio0b5ce707b4b148fba92cd62843d86cc3 -->

# Sharing Local IDs

SAP Master Data Integration service adheres to the Intelligent Enterprise promise. This promise is based on delivery of end-to-end business processes. To ensure this, SAP Master Data Integration manages data objects from clients contributing to the same landscape. For that, every master data object in the SAP Master Data Integration service has a uniquely identifiable ID.

Next to the ID within SAP Master Data Integration, it is also common for objects to have client-specific local IDs. When information flows from one client to another, associated local IDs and the related contexts are carried through with the master data object. By doing so, all destination applications can understand and react to the information they receive.

Master Data Integration provides the capability to store ID maps between **global** and **local IDs** as well as a mechanism to distribute these ID maps and do bidirectional lookups.


<table>
<tr>
<th valign="top">

Request

</th>
<th valign="top">

Function

</th>
</tr>
<tr>
<td valign="top">

1. **RequestsAPI** 

</td>
<td valign="top">

Provides the mechanism to clients to write their local IDs and the associated context to Master Data integration. This information is then added to the metadata of the information which Master Data Integration distributes.

</td>
</tr>
<tr>
<td valign="top">

2. **EventsAPI** 

</td>
<td valign="top">

Allows clients to receive the distributed local IDs and the associated context.

</td>
</tr>
<tr>
<td valign="top">

3. **KeyMappingAPI** 

</td>
<td valign="top">

Allows for applications to bidirectionally look up for local or global IDs, which are connected to each other.

</td>
</tr>
</table>

