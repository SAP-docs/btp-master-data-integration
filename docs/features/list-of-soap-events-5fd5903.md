<!-- loio5fd59034f294487d9560e08506b8854a -->

# List of SOAP Events

This section provides an overview on the currently supported SAP Master Data Integration SOAP events that are sent to SAP Cloud ALM. For a generic overview on the monitoring capabilities of SAP Master Data Integration, refer to [Monitoring](monitoring-d187cb0.md) .

**Note:** The event corresponding to the message code `BuPaDuplicateAddressId` is `INBOUND` regarding SAP Master Data Integration, whereas all other events correspond to `OUTBOUND` .


<table>
<tr>
<th valign="top">

MessageCode

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

BuPaDuplicateAddressId

</td>
<td valign="top">

Business Partner with the given Address ID already exists.

</td>
<td valign="top">

`{addressId}` 

</td>
</tr>
<tr>
<td valign="top">

BuPaConfirmationSent

</td>
<td valign="top">

Successfully sent BusinessPartner SOAP confirmation message to destination.

</td>
<td valign="top">

`{destination_name}` 

</td>
</tr>
<tr>
<td valign="top">

KmConfirmationSent

</td>
<td valign="top">

Successfully sent Keymapping SOAP confirmation message to destination.

</td>
<td valign="top">

`{destination_name}` 

</td>
</tr>
<tr>
<td valign="top">

BuPaRelConfirmationSent

</td>
<td valign="top">

Successfully sent BusinessPartnerRelationship SOAP confirmation message to destination.

</td>
<td valign="top">

`{destination_name}` 

</td>
</tr>
<tr>
<td valign="top">

BuPaConfirmationSendFailed

</td>
<td valign="top">

Failed to send BusinessPartner SOAP confirmation message to destination due to error.

</td>
<td valign="top">

`[{destination_name},{error_message}]` 

</td>
</tr>
<tr>
<td valign="top">

BuPaRelConfirmationSendFailed

</td>
<td valign="top">

Failed to send BusinessPartnerRelationship SOAP confirmation message to destination due to error.

</td>
<td valign="top">

`[{destination_name},{error_message}]` 

</td>
</tr>
<tr>
<td valign="top">

KmConfirmationSendFailed

</td>
<td valign="top">

Failed to send KeyMapping SOAP confirmation message to destination due to error.

</td>
<td valign="top">

`[{destination_name},{error_message}]` 

</td>
</tr>
<tr>
<td valign="top">

BuPaConfirmationSendFailedHttpsSchemeExpected

</td>
<td valign="top">

Failed to send BusinessPartner SOAP confirmation message to destination. URL with HTTPS scheme expected for ProxyType Internet.

</td>
<td valign="top">

`{destination_name}` 

</td>
</tr>
<tr>
<td valign="top">

BuPaRelConfirmationFailedHttpsSchemeExpected

</td>
<td valign="top">

Failed to send BusinessPartnerRelationship SOAP confirmation message to destination. URL with HTTPS scheme expected for ProxyType Internet.

</td>
<td valign="top">

`{destination_name}` 

</td>
</tr>
<tr>
<td valign="top">

KmConfirmationFailedHttpsSchemeExpected

</td>
<td valign="top">

Failed to send KeyMapping SOAP confirmation message to destination. URL with HTTPS scheme expected for ProxyType Internet.

</td>
<td valign="top">

`{destination_name}` 

</td>
</tr>
<tr>
<td valign="top">

BuPaConfirmationFailedWrongSchemeConfigured

</td>
<td valign="top">

Failed to send BusinessPartner SOAP confirmation message to destination. URL with HTTP/HTTPS Scheme expected for ProxyType OnPremise.

</td>
<td valign="top">

`{destination_name}` 

</td>
</tr>
<tr>
<td valign="top">

BuPaRelConfirmationFailedWrongSchemeConfigured

</td>
<td valign="top">

Failed to send BusinessPartnerRelationship SOAP confirmation message to destination. URL with HTTP/HTTPS Scheme expected for ProxyType OnPremise.

</td>
<td valign="top">

`{destination_name}` 

</td>
</tr>
<tr>
<td valign="top">

KmConfirmationFailedWrongSchemeConfigured

</td>
<td valign="top">

Failed to send KeyMapping SOAP confirmation message to destination. URL with HTTP/HTTPS Scheme expected for ProxyType OnPremise.

</td>
<td valign="top">

`{destination_name}` 

</td>
</tr>
<tr>
<td valign="top">

BuPaSent

</td>
<td valign="top">

BusinessPartner successfully sent to destination.

</td>
<td valign="top">

`{destination_name}` 

</td>
</tr>
<tr>
<td valign="top">

KmSent

</td>
<td valign="top">

KeyMapping successfully sent to destination.

</td>
<td valign="top">

`{destination_name}` 

</td>
</tr>
<tr>
<td valign="top">

BuPaRelSent

</td>
<td valign="top">

BusinessPartner Relationship successfully sent to destination.

</td>
<td valign="top">

`{destination_name}` 

</td>
</tr>
<tr>
<td valign="top">

BuPaSendFailed

</td>
<td valign="top">

Failed to send BusinessPartner SOAP message to destination due to error.

</td>
<td valign="top">

`[{destination_name},{error_message}]` 

</td>
</tr>
<tr>
<td valign="top">

BuPaRelSendFailed

</td>
<td valign="top">

Failed to send BusinessPartnerRelationship SOAP message to destination due to error.

</td>
<td valign="top">

`[{destination_name},{error_message}]` 

</td>
</tr>
<tr>
<td valign="top">

KmSendFailed

</td>
<td valign="top">

Failed to send KeyMapping SOAP message to destination due to error.

</td>
<td valign="top">

`[{destination_name},{error_message}]` 

</td>
</tr>
<tr>
<td valign="top">

BuPaSendFailedDestinationNotFound

</td>
<td valign="top">

Failed to send BusinessPartner SOAP message to destination. Destination not found.

</td>
<td valign="top">

`{destination_name}` 

</td>
</tr>
<tr>
<td valign="top">

BuPaRelSendFailedDestinationNotFound

</td>
<td valign="top">

Failed to send BusinessPartnerRelationship SOAP message to destination. Destination not found.

</td>
<td valign="top">

`{destination_name}` 

</td>
</tr>
<tr>
<td valign="top">

KmSendFailedDestinationNotFound

</td>
<td valign="top">

Failed to send KeyMapping SOAP message to destination. Destination not found.

</td>
<td valign="top">

`{destination_name}` 

</td>
</tr>
<tr>
<td valign="top">

BuPaSendFailedHttpsSchemeExpected

</td>
<td valign="top">

Failed to send BusinessPartner SOAP message to destination. URL with HTTPS scheme expected for ProxyType Internet.

</td>
<td valign="top">

`{destination_name}` 

</td>
</tr>
<tr>
<td valign="top">

BuPaRelSendFailedHttpsSchemeExpected

</td>
<td valign="top">

Failed to send BusinessPartnerRelationship SOAP message to destination. URL with HTTPS scheme expected for ProxyType Internet.

</td>
<td valign="top">

`{destination_name}` 

</td>
</tr>
<tr>
<td valign="top">

KmSendFailedHttpsSchemeExpected

</td>
<td valign="top">

Failed to send KeyMapping SOAP message to destination. URL with HTTPS scheme expected for ProxyType Internet.

</td>
<td valign="top">

`{destination_name}` 

</td>
</tr>
<tr>
<td valign="top">

BuPaSendFailedWrongSchemeConfigured

</td>
<td valign="top">

Failed to send BusinessPartner SOAP message to destination. URL with HTTP/HTTPS Scheme expected for ProxyType OnPremise.

</td>
<td valign="top">

`{destination_name}` 

</td>
</tr>
<tr>
<td valign="top">

BuPaRelSendFailedWrongSchemeConfigured

</td>
<td valign="top">

Failed to send BusinessPartnerRelationship SOAP message to destination. URL with HTTP/HTTPS Scheme expected for ProxyType OnPremise.

</td>
<td valign="top">

`{destination_name}` 

</td>
</tr>
<tr>
<td valign="top">

KmSendFailedWrongSchemeConfigured

</td>
<td valign="top">

Failed to send KeyMapping SOAP message to destination. URL with HTTP/HTTPS Scheme expected for ProxyType OnPremise.

</td>
<td valign="top">

`{destination_name}` 

</td>
</tr>
<tr>
<td valign="top">

BupaConfirmationReceivedSuccessful

</td>
<td valign="top">

BusinessPartner Confirmation SOAP message processed successfully.

</td>
<td valign="top">

 

</td>
</tr>
<tr>
<td valign="top">

BuPaRelConfirmationReceivedSuccessful

</td>
<td valign="top">

BusinessPartnerRelationship Confirmation SOAP message processed successfully.

</td>
<td valign="top">

 

</td>
</tr>
<tr>
<td valign="top">

KmConfirmationReceivedSuccessful

</td>
<td valign="top">

KeyMapping Confirmation SOAP message processed successfully.

</td>
<td valign="top">

 

</td>
</tr>
</table>

