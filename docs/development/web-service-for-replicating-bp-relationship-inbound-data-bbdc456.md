<!-- loiobbdc45616c1f4306a4e371ada3f7b6f5 -->

# Web Service for Replicating BP Relationship Inbound Data



<a name="loiobbdc45616c1f4306a4e371ada3f7b6f5__description"/>

## Description

Technical name: `BusinessPartnerRelationshipSUITEBulkReplicateRequest_In` 

This service enables you to replicate Business Partner Relationship data from the client system to the SAP Master Data Integration - Business Partners system. It is based on the SOAP protocol.



<a name="loiobbdc45616c1f4306a4e371ada3f7b6f5__service-structure"/>

## Service Structure

This inbound interface uses the operation, Outbound Operation for Business Partner Relationship Data \(Req\) `BusinessPartnerRelationshipSUITEBulkReplicateRequest_In` \).



<a name="loiobbdc45616c1f4306a4e371ada3f7b6f5__service-message-header"/>

## Service Message Header

The service message header contains information on the service, the involved sender and receiver as well as date and time.



<a name="loiobbdc45616c1f4306a4e371ada3f7b6f5__service-nodes"/>

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

Node that contains details of Business Partner relationships

</td>
<td valign="top">

[BusinessPartnerRelationshipSUITEBulkReplicateRequest - BusinessPartnerRelationship](web-service-for-replicating-bp-relationship-inbound-data-bbdc456.md#loiobbdc45616c1f4306a4e371ada3f7b6f5__businesspartnerrelationshipsuitebulkreplicaterequest---businesspartnerrelationship) 

</td>
</tr>
<tr>
<td valign="top">

ContactPerson

</td>
<td valign="top">

Details of the contact person

</td>
<td valign="top">

[BusinessPartnerRelationshipSUITEBulkReplicateRequest - ContactPerson](web-service-for-replicating-bp-relationship-inbound-data-bbdc456.md#loiobbdc45616c1f4306a4e371ada3f7b6f5__businesspartnerrelationshipsuitebulkreplicaterequest---contactperson) 

</td>
</tr>
</table>



<a name="loiobbdc45616c1f4306a4e371ada3f7b6f5__restrictions"/>

## Restrictions

1.  At present, BP Relationship replication is supported with the following IDs:

    -   businessPartnerUUID

    -   businessPartnerInternalID

    -   relationshipBusinessPartnerUUID

    -   relationshipBusinessPartnerInternalID

    -   receiverBusinessPartnerUUID

    -   receiverBusinessPartnerInternalID

    -   receiverRelationshipBusinessPartnerUUID

    -   receiverRelationshipBusinessPartnerInternalID


2.  BP Relationship replication with IAM ID and External ID is currently not supported.




<a name="loiobbdc45616c1f4306a4e371ada3f7b6f5__businesspartnerrelationshipsuitebulkreplicaterequest---businesspartnerrelationship"/>

## BusinessPartnerRelationshipSUITEBulkReplicateRequest - BusinessPartnerRelationship

This service node contains the following parameters.



<a name="loiobbdc45616c1f4306a4e371ada3f7b6f5__soap-and-odm-mapping-information"/>

## SOAP and ODM Mapping Information


<table>
<tr>
<th valign="top">

SOAP Field

</th>
<th valign="top">

Description

</th>
<th valign="top">

SOAP Path

</th>
<th valign="top">

ODM Field

</th>
<th valign="top">

ODM Path

</th>
<th valign="top">

Necessity

</th>
</tr>
<tr>
<td valign="top">

RoleCode

</td>
<td valign="top">

 

</td>
<td valign="top">

BusinessPartnerRelationship/RoleCode

</td>
<td valign="top">

category

</td>
<td valign="top">

BusinessPartnerRelationship

</td>
<td valign="top">

Optional

</td>
</tr>
<tr>
<td valign="top">

StartDate

</td>
<td valign="top">

Validity Start Date

</td>
<td valign="top">

BusinessPartnerRelationship/ValidityPeriod/StartDate

</td>
<td valign="top">

validFrom

</td>
<td valign="top">

BusinessPartnerRelationship

</td>
<td valign="top">

Optional

</td>
</tr>
<tr>
<td valign="top">

EndDate

</td>
<td valign="top">

Validity End Date

</td>
<td valign="top">

BusinessPartnerRelationship/ValidityPeriod/EndDate

</td>
<td valign="top">

validTo

</td>
<td valign="top">

BusinessPartnerRelationship

</td>
<td valign="top">

Optional

</td>
</tr>
<tr>
<td valign="top">

RelationshipBusinessPartnerUUID

</td>
<td valign="top">

UUID of the related Business Partner in the sender system

</td>
<td valign="top">

BusinessPartnerRelationship/RelationshipBusinessPartnerUUID

</td>
<td valign="top">

relationshipSource

</td>
<td valign="top">

BusinessPartnerRelationship

</td>
<td valign="top">

Optional

</td>
</tr>
<tr>
<td valign="top">

DefaultIndicator

</td>
<td valign="top">

If several relationships of the Business Partner relationship category contact person have been defined for, then one can be can set as default.

</td>
<td valign="top">

BusinessPartnerRelationship/DefaultIndicator

</td>
<td valign="top">

isDefaultTarget

</td>
<td valign="top">

BusinessPartnerRelationship

</td>
<td valign="top">

Optional

</td>
</tr>
</table>



<a name="loiobbdc45616c1f4306a4e371ada3f7b6f5__businesspartnerrelationshipsuitebulkreplicaterequest---contactperson"/>

## BusinessPartnerRelationshipSUITEBulkReplicateRequest - ContactPerson

This service node contains the following parameters.



<a name="loiobbdc45616c1f4306a4e371ada3f7b6f5__soap-and-odm-mapping-information-1"/>

## SOAP and ODM Mapping Information


<table>
<tr>
<th valign="top">

SOAP Field

</th>
<th valign="top">

 

</th>
<th valign="top">

Description

</th>
<th valign="top">

SOAP Path

</th>
<th valign="top">

ODM Field

</th>
<th valign="top">

ODM Path

</th>
</tr>
<tr>
<td valign="top">

**ContactPerson** 

</td>
<td valign="top">

BusinessPartnerFunctionalAreaCode

</td>
<td valign="top">

Department Name of the Conatct Person

</td>
<td valign="top">

BusinessPartnerRelationship/ContactPerson/BusinessPartnerFunctionalAreaCode

</td>
<td valign="top">

departmentName

</td>
<td valign="top">

BusinessPartnerRelationship/ContactPerson

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

ContactPersonNote

</td>
<td valign="top">

Comments, or notes, on a person in a company.

</td>
<td valign="top">

BusinessPartnerRelationship/ContactPerson/ContactPersonNote

</td>
<td valign="top">

note

</td>
<td valign="top">

BusinessPartnerRelationship/ContactPerson

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

BusinessPartnerRelationship/ContactPerson/SupplierContactPerson/ReceiverInternalID

</td>
<td valign="top">

supplierContactPerson

</td>
<td valign="top">

BusinessPartnerRelationship/ContactPerson

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

VIPReasonCode

</td>
<td valign="top">

VIP Partner; Defines whether a person is an important figure \(VIP\) in the company; True/False

</td>
<td valign="top">

BusinessPartnerRelationship/ContactPerson/VIPReasonCode

</td>
<td valign="top">

vipReasonCode

</td>
<td valign="top">

BusinessPartnerRelationship/ContactPerson

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

ReceiverInternalID

</td>
<td valign="top">

Contact Person number helps to uniquely identify the contact person if it has Supplier role \(FLVN00, FLVN01\) in receiver system

</td>
<td valign="top">

BusinessPartnerRelationship/ContactPerson/CustomerContactPerson/ReceiverInternalID

</td>
<td valign="top">

customerContactPerson

</td>
<td valign="top">

BusinessPartnerRelationship/ContactPerson

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

BusinessPartnerFunctionTypeCode

</td>
<td valign="top">

Function of partner \(Identifies the function that a person has within a company\); For example, Secretary, HR Manager

</td>
<td valign="top">

BusinessPartnerRelationship/ContactPerson/BusinessPartnerFunctionTypeCode

</td>
<td valign="top">

functionalTitle

</td>
<td valign="top">

BusinessPartnerRelationship/ContactPerson

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

PowerOfAttorneyTypeCode

</td>
<td valign="top">

Indicates the authority a person has within a company; For example, General commercial powers of attorney, Authority to issue instructions

</td>
<td valign="top">

BusinessPartnerRelationship/ContactPerson/PowerOfAttorneyTypeCode

</td>
<td valign="top">

powerOfAttorneyTypeCode

</td>
<td valign="top">

BusinessPartnerRelationship/ContactPerson

</td>
</tr>
<tr>
<td valign="top">

**WorkplaceAddressInformation** 

</td>
<td valign="top">

AddressUUID

</td>
<td valign="top">

Address number

</td>
<td valign="top">

BusinessPartnerRelationship/ContactPerson/WorkplaceAddressInformation/AddressUUID

</td>
<td valign="top">

id

</td>
<td valign="top">

BusinessPartnerRelationship/ContactPerson/WorkplaceAddressInformation

</td>
</tr>
<tr>
<td valign="top">

**Workplace** 

</td>
<td valign="top">

DepartmentName

</td>
<td valign="top">

Department

</td>
<td valign="top">

BusinessPartnerRelationship/ContactPerson/WorkplaceAddressInformation/Address/Workplace/DepartmentName

</td>
<td valign="top">

departmentName

</td>
<td valign="top">

BusinessPartnerRelationship/ContactPerson/WorkplaceAddressInformation/Address/Workplace

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

FunctionalTitleName

</td>
<td valign="top">

Function of a person, e.g. as contact person in a company.

</td>
<td valign="top">

BusinessPartnerRelationship/ContactPerson/WorkplaceAddressInformation/Address/Workplace/FunctionalTitleName

</td>
<td valign="top">

functionalTitleName

</td>
<td valign="top">

BusinessPartnerRelationship/ContactPerson/WorkplaceAddressInformation/Address/Workplace

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

CorrespondenceShortName

</td>
<td valign="top">

Short name for correspondence

</td>
<td valign="top">

BusinessPartnerRelationship/ContactPerson/WorkplaceAddressInformation/Address/Workplace/CorrespondenceShortName

</td>
<td valign="top">

correspondenceShortName

</td>
<td valign="top">

BusinessPartnerRelationship/ContactPerson/WorkplaceAddressInformation/Address/Workplace

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

FloorID

</td>
<td valign="top">

Floor in building

</td>
<td valign="top">

BusinessPartnerRelationship/ContactPerson/WorkplaceAddressInformation/Address/Workplace/FloorID

</td>
<td valign="top">

floor

</td>
<td valign="top">

BusinessPartnerRelationship/ContactPerson/WorkplaceAddressInformation/Address/Workplace

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

BuildingID

</td>
<td valign="top">

Building \(number or code\)

</td>
<td valign="top">

BusinessPartnerRelationship/ContactPerson/WorkplaceAddressInformation/Address/Workplace/BuildingID

</td>
<td valign="top">

building

</td>
<td valign="top">

BusinessPartnerRelationship/ContactPerson/WorkplaceAddressInformation/Address/Workplace

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

RoomID

</td>
<td valign="top">

Room or Apartment Number

</td>
<td valign="top">

BusinessPartnerRelationship/ContactPerson/WorkplaceAddressInformation/Address/Workplace/RoomID

</td>
<td valign="top">

room

</td>
<td valign="top">

BusinessPartnerRelationship/ContactPerson/WorkplaceAddressInformation/Address/Workplace

</td>
</tr>
<tr>
<td valign="top">

**Email** 

</td>
<td valign="top">

URI

</td>
<td valign="top">

Email address

</td>
<td valign="top">

BusinessPartner/AddressInformation/Address/Email/URI,BusinessPartnerRelationship/ContactPerson/WorkplaceAddressInformation/Address/Email/URI

</td>
<td valign="top">

address

</td>
<td valign="top">

BusinessPartnerRelationship/ContactPerson/WorkplaceAddressInformation/Address/Email

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

StartDate

</td>
<td valign="top">

Email validity start date

</td>
<td valign="top">

BusinessPartner/AddressInformation/Address/Email/ValidityPeriod/StartDate,BusinessPartnerRelationship/ContactPerson/WorkplaceAddressInformation/Address/Email/ValidityPeriod/StartDate

</td>
<td valign="top">

validFrom

</td>
<td valign="top">

BusinessPartnerRelationship/ContactPerson/WorkplaceAddressInformation/Address/Email

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

EndDate

</td>
<td valign="top">

Email validity end date

</td>
<td valign="top">

BusinessPartner/AddressInformation/Address/Email/ValidityPeriod/EndDate,BusinessPartnerRelationship/ContactPerson/WorkplaceAddressInformation/Address/Email/ValidityPeriod/EndDate

</td>
<td valign="top">

validTo

</td>
<td valign="top">

BusinessPartnerRelationship/ContactPerson/WorkplaceAddressInformation/Address/Email

</td>
</tr>
<tr>
<td valign="top">

**Facsimile** 

</td>
<td valign="top">

CountryCode

</td>
<td valign="top">

Countrycode, number and extension

</td>
<td valign="top">

BusinessPartner/AddressInformation/Address/Facsimile/Number/CountryCode,BusinessPartnerRelationship/ContactPerson/WorkplaceAddressInformation/Address/Facsimile/Number/CountryCode

</td>
<td valign="top">

country

</td>
<td valign="top">

BusinessPartnerRelationship/ContactPerson/WorkplaceAddressInformation/Address/Facsimile

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

SubscriberID

</td>
<td valign="top">

 

</td>
<td valign="top">

BusinessPartner/AddressInformation/Address/Facsimile/Number/SubscriberID,BusinessPartnerRelationship/ContactPerson/WorkplaceAddressInformation/Address/Facsimile/Number/SubscriberID

</td>
<td valign="top">

number

</td>
<td valign="top">

BusinessPartnerRelationship/ContactPerson/WorkplaceAddressInformation/Address/Facsimile

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

ExtensionID

</td>
<td valign="top">

 

</td>
<td valign="top">

BusinessPartner/AddressInformation/Address/Facsimile/Number/ExtensionID,BusinessPartnerRelationship/ContactPerson/WorkplaceAddressInformation/Address/Facsimile/Number/ExtensionID

</td>
<td valign="top">

numberExtension

</td>
<td valign="top">

BusinessPartnerRelationship/ContactPerson/WorkplaceAddressInformation/Address/Facsimile

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

StartDate

</td>
<td valign="top">

Fax number validity start date

</td>
<td valign="top">

BusinessPartner/AddressInformation/Address/Facsimile/ValidityPeriod/StartDate,BusinessPartnerRelationship/ContactPerson/WorkplaceAddressInformation/Address/Facsimile/ValidityPeriod/StartDate

</td>
<td valign="top">

validFrom

</td>
<td valign="top">

BusinessPartnerRelationship/ContactPerson/WorkplaceAddressInformation/Address/Facsimile

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

EndDate

</td>
<td valign="top">

Fax number validity end date

</td>
<td valign="top">

BusinessPartner/AddressInformation/Address/Facsimile/ValidityPeriod/EndDate,BusinessPartnerRelationship/ContactPerson/WorkplaceAddressInformation/Address/Facsimile/ValidityPeriod/EndDate

</td>
<td valign="top">

validTo

</td>
<td valign="top">

BusinessPartnerRelationship/ContactPerson/WorkplaceAddressInformation/Address/Facsimile

</td>
</tr>
<tr>
<td valign="top">

**Web** 

</td>
<td valign="top">

URI

</td>
<td valign="top">

Website Address

</td>
<td valign="top">

BusinessPartner/AddressInformation/Address/Web/URI,BusinessPartnerRelationship/ContactPerson/WorkplaceAddressInformation/Address/Web/URI

</td>
<td valign="top">

url

</td>
<td valign="top">

BusinessPartnerRelationship/ContactPerson/WorkplaceAddressInformation/Address/Web

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

URITypeCode

</td>
<td valign="top">

URI type flag

</td>
<td valign="top">

BusinessPartnerRelationship/ContactPerson/WorkplaceAddressInformation/Address/Web/URITypeCode

</td>
<td valign="top">

uriType

</td>
<td valign="top">

contactPersonInformation/address/websites/uriType

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

StartDate

</td>
<td valign="top">

Website validity start date

</td>
<td valign="top">

BusinessPartner/AddressInformation/Address/Web/ValidityPeriod/StartDate,BusinessPartnerRelationship/ContactPerson/WorkplaceAddressInformation/Address/Web/ValidityPeriod/StartDate

</td>
<td valign="top">

validFrom

</td>
<td valign="top">

BusinessPartnerRelationship/ContactPerson/WorkplaceAddressInformation/Address/Web

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

EndDate

</td>
<td valign="top">

Website validity end date

</td>
<td valign="top">

BusinessPartner/AddressInformation/Address/Web/ValidityPeriod/EndDate,BusinessPartnerRelationship/ContactPerson/WorkplaceAddressInformation/Address/Web/ValidityPeriod/EndDate

</td>
<td valign="top">

validTo

</td>
<td valign="top">

BusinessPartnerRelationship/ContactPerson/WorkplaceAddressInformation/Address/Web

</td>
</tr>
<tr>
<td valign="top">

**Telephone** 

</td>
<td valign="top">

CountryCode

</td>
<td valign="top">

Number, Extension and Country Code

</td>
<td valign="top">

BusinessPartner/AddressInformation/Address/Telephone/Number/CountryCode,BusinessPartnerRelationship/ContactPerson/WorkplaceAddressInformation/Address/Telephone/Number/CountryCode

</td>
<td valign="top">

country

</td>
<td valign="top">

BusinessPartnerRelationship/ContactPerson/WorkplaceAddressInformation/Address/Telephone

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

SubscriberID

</td>
<td valign="top">

 

</td>
<td valign="top">

BusinessPartner/AddressInformation/Address/Telephone/Number/SubscriberID,BusinessPartnerRelationship/ContactPerson/WorkplaceAddressInformation/Address/Telephone/Number/SubscriberID

</td>
<td valign="top">

number

</td>
<td valign="top">

BusinessPartnerRelationship/ContactPerson/WorkplaceAddressInformation/Address/Telephone

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

ExtensionID

</td>
<td valign="top">

 

</td>
<td valign="top">

BusinessPartner/AddressInformation/Address/Telephone/Number/ExtensionID,BusinessPartnerRelationship/ContactPerson/WorkplaceAddressInformation/Address/Telephone/Number/ExtensionID

</td>
<td valign="top">

numberExtension

</td>
<td valign="top">

BusinessPartnerRelationship/ContactPerson/WorkplaceAddressInformation/Address/Telephone

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

SMSEnabledIndicator

</td>
<td valign="top">

Indicator: Telephone is SMS-Enabled

</td>
<td valign="top">

BusinessPartnerRelationship/ContactPerson/WorkplaceAddressInformation/Address/Telephone/SMSEnabledIndicator

</td>
<td valign="top">

numberExtension

</td>
<td valign="top">

BusinessPartnerRelationship/ContactPerson/WorkplaceAddressInformation/Address/Telephone

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

StartDate

</td>
<td valign="top">

Telephone validity start date

</td>
<td valign="top">

BusinessPartner/AddressInformation/Address/Telephone/ValidityPeriod/StartDate,BusinessPartnerRelationship/ContactPerson/WorkplaceAddressInformation/Address/Telephone/ValidityPeriod/StartDate

</td>
<td valign="top">

validFrom

</td>
<td valign="top">

BusinessPartnerRelationship/ContactPerson/WorkplaceAddressInformation/Address/Telephone

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

EndDate

</td>
<td valign="top">

Telephone validity end date

</td>
<td valign="top">

BusinessPartner/AddressInformation/Address/Telephone/ValidityPeriod/EndDate,BusinessPartnerRelationship/ContactPerson/WorkplaceAddressInformation/Address/Telephone/ValidityPeriod/EndDate

</td>
<td valign="top">

validTo

</td>
<td valign="top">

BusinessPartnerRelationship/ContactPerson/WorkplaceAddressInformation/Address/Telephone

</td>
</tr>
</table>

