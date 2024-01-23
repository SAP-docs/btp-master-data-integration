<!-- loio422e8f6943764bb5881cf49d4c1e46fa -->

# List of REST Events

This section provides an overview on the currently supported SAP Master Data Integration REST events that are sent to SAP Cloud ALM. For a generic overview on the monitoring capabilities of SAP Master Data Integration, see [Monitoring](monitoring-d187cb0.md) .


<table>
<tr>
<th valign="top">

Message Code

</th>
<th valign="top">

Message

</th>
<th valign="top">

Details

</th>
</tr>
<tr>
<td valign="top">

ExistingInstanceId

</td>
<td valign="top">

Entity with given instance ID already exists.

</td>
<td valign="top">

`[{id: instanceId}]` 

</td>
</tr>
<tr>
<td valign="top">

EntityInstanceDoesNotExist

</td>
<td valign="top">

Entity with given instance ID does not exist.

</td>
<td valign="top">

`[{id: instanceId}]` 

</td>
</tr>
<tr>
<td valign="top">

ValidationError

</td>
<td valign="top">

Validation error.

</td>
<td valign="top">

`[{ValidationError: error message},{...}]` \(list of errors occurred during validation\)

</td>
</tr>
<tr>
<td valign="top">

PatchFailed

</td>
<td valign="top">

Patch failed.

</td>
<td valign="top">

`[{PatchFailed: error message},{...}]` \(list of errors caused the patch to fail\)

</td>
</tr>
<tr>
<td valign="top">

InvalidPreviousVersionI

</td>
<td valign="top">

Invalid previous version ID: `<ID>` 

</td>
<td valign="top">

`[{id: instanceId}]` 

</td>
</tr>
<tr>
<td valign="top">

UpdateOrDeleteOnDeletedInstance

</td>
<td valign="top">

The instance has been deleted and no longer supports any update or delete operations.

</td>
<td valign="top">



</td>
</tr>
<tr>
<td valign="top">

UpdateOrDeleteOnReplacedInstance

</td>
<td valign="top">

The instance has been replaced and no longer supports any update or delete operations.

</td>
<td valign="top">



</td>
</tr>
<tr>
<td valign="top">

MergeOnDeletedInstance

</td>
<td valign="top">

The instance has not been replaced and cannot be merged.

</td>
<td valign="top">

`[{id: instanceId}]` 

</td>
</tr>
<tr>
<td valign="top">

EntityInstanceReplacedByOtherInstance

</td>
<td valign="top">

The instance has been replaced by a different instance and cannot be merged.

</td>
<td valign="top">

`[{id: instanceId},{replacedBy: instanceId}]` 

</td>
</tr>
<tr>
<td valign="top">

DecodeError

</td>
<td valign="top">

The instance could not be decoded properly.

</td>
<td valign="top">



</td>
</tr>
<tr>
<td valign="top">

UnexpectedStateError

</td>
<td valign="top">

Unexpected state error.

</td>
<td valign="top">



</td>
</tr>
<tr>
<td valign="top">

UnknownEntity

</td>
<td valign="top">

Unknown entity.

</td>
<td valign="top">



</td>
</tr>
<tr>
<td valign="top">

ReplacedError

</td>
<td valign="top">

Could not replace an event.

</td>
<td valign="top">

`[{ReplacedFailure: error message}]` 

</td>
</tr>
<tr>
<td valign="top">

ReplacementCycle

</td>
<td valign="top">

Could not identify active replacement because of cyclic references in replacedBy starting from replacement.

</td>
<td valign="top">



</td>
</tr>
<tr>
<td valign="top">

InvalidLogicalKeys

</td>
<td valign="top">

Invalid logical keys.

</td>
<td valign="top">



</td>
</tr>
<tr>
<td valign="top">

LocalIdError

</td>
<td valign="top">

LocalId operations error.

</td>
<td valign="top">

`{context, localId, status}` 

</td>
</tr>
<tr>
<td valign="top">

NormalizationFailed

</td>
<td valign="top">

Could not normalize an event.

</td>
<td valign="top">

`[{NormalizationFailure: error message}]` 

</td>
</tr>
<tr>
<td valign="top">

PrimaryMasterDataEventTooLarge

</td>
<td valign="top">

The size of the SAP Master Data Integration internal record, PrimaryMasterDataEvent, exceeds the limit.

</td>
<td valign="top">



</td>
</tr>
<tr>
<td valign="top">

UnknownTenant

</td>
<td valign="top">

The system for which this request was send was unknown to SAP Master Data Integration at the time of processing.

</td>
<td valign="top">



</td>
</tr>
</table>

