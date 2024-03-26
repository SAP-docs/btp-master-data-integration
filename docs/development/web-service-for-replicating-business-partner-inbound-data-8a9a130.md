<!-- loio8a9a1305ac764111b648e3303f24c784 -->

# Web Service for Replicating Business Partner Inbound Data



<a name="loio8a9a1305ac764111b648e3303f24c784__description"/>

## Description

Technical name: `BusinessPartnerSUITEBulkReplicateRequest_In` .

This service enables you to replicate Business Partner data from the client system to SAP Master Data Integration - Business Partners system.



<a name="loio8a9a1305ac764111b648e3303f24c784__service-structure"/>

## Service Structure

This inbound interface uses the operation Inbound interface for Business Partner Data \( `BusinessPartnerSUITEBulkReplicateRequest_In` \).



<a name="loio8a9a1305ac764111b648e3303f24c784__service-message-header"/>

## Service Message Header

The service message header contains information on the service, the involved sender and receiver as well as date and time.



<a name="loio8a9a1305ac764111b648e3303f24c784__service-nodes"/>

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

Node that contains details of BusinessPartner.

</td>
<td valign="top">

[BusinessPartnerSUITEBulkReplicateRequest - BusinessPartner](web-service-for-replicating-business-partner-inbound-data-8a9a130.md#loio8a9a1305ac764111b648e3303f24c784__businesspartnersuitebulkreplicaterequest---businesspartner) 

</td>
</tr>
<tr>
<td valign="top">

Person

</td>
<td valign="top">

Business Partner person data.

</td>
<td valign="top">

[BusinessPartnerSUITEBulkReplicateRequest - Person](web-service-for-replicating-business-partner-inbound-data-8a9a130.md#loio8a9a1305ac764111b648e3303f24c784__businesspartnersuitebulkreplicaterequest---person) 

</td>
</tr>
<tr>
<td valign="top">

Organization

</td>
<td valign="top">

Entity details organization.

</td>
<td valign="top">

[BusinessPartnerSUITEBulkReplicateRequest - Organization](web-service-for-replicating-business-partner-inbound-data-8a9a130.md#loio8a9a1305ac764111b648e3303f24c784__businesspartnersuitebulkreplicaterequest---organization) 

</td>
</tr>
<tr>
<td valign="top">

Identification

</td>
<td valign="top">

Entity details identification.

</td>
<td valign="top">

[BusinessPartnerSUITEBulkReplicateRequest - Identification](web-service-for-replicating-business-partner-inbound-data-8a9a130.md#loio8a9a1305ac764111b648e3303f24c784__businesspartnersuitebulkreplicaterequest---identification) 

</td>
</tr>
<tr>
<td valign="top">

BankDetails

</td>
<td valign="top">

Entity details of bank.

</td>
<td valign="top">

[BusinessPartnerSUITEBulkReplicateRequest - BankDetails](web-service-for-replicating-business-partner-inbound-data-8a9a130.md#loio8a9a1305ac764111b648e3303f24c784__businesspartnersuitebulkreplicaterequest---bankdetails) 

</td>
</tr>
<tr>
<td valign="top">

TaxNumber

</td>
<td valign="top">

Entity details of tax.

</td>
<td valign="top">

[BusinessPartnerSUITEBulkReplicateRequest - TaxNumber](web-service-for-replicating-business-partner-inbound-data-8a9a130.md#loio8a9a1305ac764111b648e3303f24c784__businesspartnersuitebulkreplicaterequest---taxnumber) 

</td>
</tr>
<tr>
<td valign="top">

Role

</td>
<td valign="top">

Entity details of Business Partner role.

</td>
<td valign="top">

[BusinessPartnerSUITEBulkReplicateRequest - Role](web-service-for-replicating-business-partner-inbound-data-8a9a130.md#loio8a9a1305ac764111b648e3303f24c784__businesspartnersuitebulkreplicaterequest---role) 

</td>
</tr>
<tr>
<td valign="top">

Business Partner Group

</td>
<td valign="top">

Entity details of Business Partner group.

</td>
<td valign="top">

[BusinessPartnerSUITEBulkReplicateRequest - Business Partner Group](web-service-for-replicating-business-partner-inbound-data-8a9a130.md#loio8a9a1305ac764111b648e3303f24c784__businesspartnersuitebulkreplicaterequest---business-partner-group) 

</td>
</tr>
<tr>
<td valign="top">

Address Data

</td>
<td valign="top">

Entity details of address.

</td>
<td valign="top">

[BusinessPartnerSUITEBulkReplicateRequest - Address Data](web-service-for-replicating-business-partner-inbound-data-8a9a130.md#loio8a9a1305ac764111b648e3303f24c784__businesspartnersuitebulkreplicaterequest---address-data) 

</td>
</tr>
<tr>
<td valign="top">

Customer

</td>
<td valign="top">

Entity details of customer.

</td>
<td valign="top">

[BusinessPartnerSUITEBulkReplicateRequest - Customer](web-service-for-replicating-business-partner-inbound-data-8a9a130.md#loio8a9a1305ac764111b648e3303f24c784__businesspartnersuitebulkreplicaterequest---customer) 

</td>
</tr>
<tr>
<td valign="top">

Supplier

</td>
<td valign="top">

Entity details of supplier.

</td>
<td valign="top">

[BusinessPartnerSUITEBulkReplicateRequest - Supplier](web-service-for-replicating-business-partner-inbound-data-8a9a130.md#loio8a9a1305ac764111b648e3303f24c784__businesspartnersuitebulkreplicaterequest---supplier) 

</td>
</tr>
</table>



<a name="loio8a9a1305ac764111b648e3303f24c784__restrictions"/>

## Restrictions

This service interface is released with restrictions. For more information, contact your SAP system administrator.



<a name="loio8a9a1305ac764111b648e3303f24c784__businesspartnersuitebulkreplicaterequest---businesspartner"/>

## BusinessPartnerSUITEBulkReplicateRequest - BusinessPartner

This service node contains the following parameters:



<a name="loio8a9a1305ac764111b648e3303f24c784__soap-and-odm-mapping-information"/>

## SOAP and ODM Mapping Information


<table>
<tr>
<th valign="top">

SOAP Field Name

</th>
<th valign="top">

Description

</th>
<th valign="top">

SOAP Path

</th>
<th valign="top">

ODM Field Name

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

UUID

</td>
<td valign="top">

This is the Business Partner UUID in the Receiver system. This will be empty during the first replication.

</td>
<td valign="top">

BusinessPartner/UUID

</td>
<td valign="top">

Id

</td>
<td valign="top">

BusinessPartner

</td>
<td valign="top">

Optional

</td>
</tr>
<tr>
<td valign="top">

CategoryCode

</td>
<td valign="top">

Category under which a business partner is classified \(Organization/Natural person/Group of natural persons or organizations\).

</td>
<td valign="top">

BusinessPartner/CategoryCode

</td>
<td valign="top">

businessPartnerType

</td>
<td valign="top">

BusinessPartner

</td>
<td valign="top">

Optional

</td>
</tr>
<tr>
<td valign="top">

BlockedIndicator

</td>
<td valign="top">

If the business partner is blocked centrally, certain activities cannot be executed.

</td>
<td valign="top">

BusinessPartner/Common/BlockedIndicator

</td>
<td valign="top">

isBlocked

</td>
<td valign="top">

BusinessPartner

</td>
<td valign="top">

 

</td>
</tr>
<tr>
<td valign="top">

Status

</td>
<td valign="top">

 

</td>
<td valign="top">

BusinessPartner/Common/Status

</td>
<td valign="top">

lifecycleStatus

</td>
<td valign="top">

BusinessPartner

</td>
<td valign="top">

 

</td>
</tr>
<tr>
<td valign="top">

BusinessPartnerAuthorisationGroupCode

</td>
<td valign="top">

You can use authorization groups to stipulate which business partners a user is allowed to process.

</td>
<td valign="top">

BusinessPartner/Common/BusinessPartnerAuthorisationGroupCode

</td>
<td valign="top">

authorizationGroup

</td>
<td valign="top">

BusinessPartner

</td>
<td valign="top">

 

</td>
</tr>
<tr>
<td valign="top">

NumberRangeIntervalBusinessPartnerGroupCode

</td>
<td valign="top">

Classification assigned when creating a business partner.

</td>
<td valign="top">

BusinessPartner/NumberRangeIntervalBusinessPartnerGroupCode

</td>
<td valign="top">

grouping

</td>
<td valign="top">

BusinessPartner

</td>
<td valign="top">

 

</td>
</tr>
<tr>
<td valign="top">

NaturalPersonIndicator

</td>
<td valign="top">

Indicator through which a distinction between natural and legal persons can be made during tax reporting.

</td>
<td valign="top">

BusinessPartner/Common/NaturalPersonIndicator

</td>
<td valign="top">

isNaturalPersonUnderTaxLaw

</td>
<td valign="top">

BusinessPartner

</td>
<td valign="top">

 

</td>
</tr>
<tr>
<td valign="top">

ContactAllowedCode

</td>
<td valign="top">

Business Partner: Contact Permission.

</td>
<td valign="top">

BusinessPartner/Common/ContactAllowedCode

</td>
<td valign="top">

contactPermission

</td>
<td valign="top">

BusinessPartner

</td>
<td valign="top">

 

</td>
</tr>
<tr>
<td valign="top">

DeletedIndicator

</td>
<td valign="top">

Indicates if the business partner is meant to be archived.

</td>
<td valign="top">

BusinessPartner/Common/DeletedIndicator

</td>
<td valign="top">

meantToBeArchived

</td>
<td valign="top">

BusinessPartner

</td>
<td valign="top">

 

</td>
</tr>
<tr>
<td valign="top">

CorrespondenceBrailleRequiredIndicator

</td>
<td valign="top">

Business Partner Print Format.

</td>
<td valign="top">

BusinessPartner/Common/CorrespondenceBrailleRequiredIndicator

</td>
<td valign="top">

businessPartnerPrintFormat

</td>
<td valign="top">

BusinessPartner

</td>
<td valign="top">

 

</td>
</tr>
<tr>
<td valign="top">

CorrespondenceLargePrintRequiredIndicator

</td>
<td valign="top">

Business Partner Print Large Format.

</td>
<td valign="top">

BusinessPartner/Common/CorrespondenceLargePrintRequiredIndicator

</td>
<td valign="top">

businessPartnerPrintLargeFormat

</td>
<td valign="top">

BusinessPartner

</td>
<td valign="top">

 

</td>
</tr>
<tr>
<td valign="top">

KeyWordsText

</td>
<td valign="top">

Denotes the term that you define for a business partner, and via which you can restrict the search for a business partner in the business partner search or in the locator.

</td>
<td valign="top">

BusinessPartner/Common/KeyWordsText

</td>
<td valign="top">

searchTerm1

</td>
<td valign="top">

BusinessPartner/SearchTerms

</td>
<td valign="top">

 

</td>
</tr>
<tr>
<td valign="top">

AdditionalKeyWordsText

</td>
<td valign="top">

Denotes the term that you define for a business partner, and via which you can restrict the search for a business partner in the business partner search or in the locator.

</td>
<td valign="top">

BusinessPartner/Common/AdditionalKeyWordsText

</td>
<td valign="top">

searchTerm2

</td>
<td valign="top">

BusinessPartner/SearchTerms

</td>
<td valign="top">

 

</td>
</tr>
<tr>
<td valign="top">

ReleasedIndicator

</td>
<td valign="top">

Indicates if the business partner has been released for business processes.

</td>
<td valign="top">

BusinessPartner/Common/ReleasedIndicator

</td>
<td valign="top">

isReleased

</td>
<td valign="top">

BusinessPartner

</td>
<td valign="top">

 

</td>
</tr>
</table>



<a name="loio8a9a1305ac764111b648e3303f24c784__businesspartnersuitebulkreplicaterequest---person"/>

## BusinessPartnerSUITEBulkReplicateRequest - Person

This service node contains the following parameters:



<a name="loio8a9a1305ac764111b648e3303f24c784__soap-and-odm-mapping-information-1"/>

## SOAP and ODM Mapping Information


<table>
<tr>
<th valign="top">

Category

</th>
<th valign="top">

SOAP Field Name

</th>
<th valign="top">

Description

</th>
<th valign="top">

SOAP Path

</th>
<th valign="top">

ODM Field Name

</th>
<th valign="top">

ODM Path

</th>
</tr>
<tr>
<td valign="top">

**Person** 

</td>
<td valign="top">

GenderCode

</td>
<td valign="top">

Selection: Business partner is male / Selection: Business partner is female.

</td>
<td valign="top">

BusinessPartner/Common/Person/GenderCode

</td>
<td valign="top">

gender

</td>
<td valign="top">

BusinessPartner/person

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

NationalityCountryCode

</td>
<td valign="top">

Nationality of Business Partner \(Person\).

</td>
<td valign="top">

BusinessPartner/Common/Person/NationalityCountryCode

</td>
<td valign="top">

nationality

</td>
<td valign="top">

BusinessPartner/person

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

BirthDate

</td>
<td valign="top">

Date of Birth of Business Partner.

</td>
<td valign="top">

BusinessPartner/Common/Person/BirthDate

</td>
<td valign="top">

birthDate

</td>
<td valign="top">

BusinessPartner/person

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

VerbalCommunicationLanguageCode

</td>
<td valign="top">

Language for verbal communication with a business partner.

</td>
<td valign="top">

BusinessPartner/Common/VerbalCommunicationLanguageCode

</td>
<td valign="top">

language

</td>
<td valign="top">

BusinessPartner/person

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

NonVerbalCommunicationLanguageCode

</td>
<td valign="top">

Correspondence language \(written\) for business partners in the Person category.

</td>
<td valign="top">

BusinessPartner/Common/Person/NonVerbalCommunicationLanguageCode

</td>
<td valign="top">

correspondenceLanguage

</td>
<td valign="top">

BusinessPartner/person

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

MaritalStatusCode

</td>
<td valign="top">

Marital Status of Business Partner.

</td>
<td valign="top">

BusinessPartner/Common/Person/MaritalStatusCode

</td>
<td valign="top">

maritalStatus

</td>
<td valign="top">

BusinessPartner/person

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

Employer

</td>
<td valign="top">

Name of Employer of a natural Person.

</td>
<td valign="top">

BusinessPartner/Common/Person/Employer

</td>
<td valign="top">

employerName

</td>
<td valign="top">

BusinessPartner/person

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

BusinessPartnerOccupationGroup

</td>
<td valign="top">

You can assign an occupation to business partners in the category "Person". This is for information purposes only.

</td>
<td valign="top">

BusinessPartner/Common/Person/OccupationCode

</td>
<td valign="top">

occupation

</td>
<td valign="top">

BusinessPartner/person

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

BirthPlaceName

</td>
<td valign="top">

Birthplace of business partner.

</td>
<td valign="top">

BusinessPartner/Common/Person/BirthPlaceName

</td>
<td valign="top">

birthplaceName

</td>
<td valign="top">

BusinessPartner/person

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

DeathDate

</td>
<td valign="top">

Date of death of business partner.

</td>
<td valign="top">

BusinessPartner/Common/Person/DeathDate

</td>
<td valign="top">

deathDate

</td>
<td valign="top">

BusinessPartner/person

</td>
</tr>
<tr>
<td valign="top">

**NameDetails** 

</td>
<td valign="top">

GivenName

</td>
<td valign="top">

First Name of Business Partner \(Person\).

</td>
<td valign="top">

BusinessPartner/Common/Person/Name/GivenName

</td>
<td valign="top">

firstName

</td>
<td valign="top">

BusinessPartner/person/nameDetails

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

MiddleName

</td>
<td valign="top">

Middle name or second forename of a person.

</td>
<td valign="top">

BusinessPartner/Common/Person/Name/MiddleName

</td>
<td valign="top">

middleName

</td>
<td valign="top">

BusinessPartner/person/nameDetails

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

FamilyName

</td>
<td valign="top">

Last Name of Business Partner \(Person\).

</td>
<td valign="top">

BusinessPartner/Common/Person/Name/FamilyName

</td>
<td valign="top">

lastName

</td>
<td valign="top">

BusinessPartner/person/nameDetails

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

AdditionalFamilyName

</td>
<td valign="top">

Other Last Name of a Person.

</td>
<td valign="top">

BusinessPartner/Common/Person/Name/AdditionalFamilyName

</td>
<td valign="top">

secondLastName

</td>
<td valign="top">

BusinessPartner/person/nameDetails

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

NickName

</td>
<td valign="top">

Nickname of Business Partner \(Person\).

</td>
<td valign="top">

BusinessPartner/Common/Person/Name/NickName

</td>
<td valign="top">

nickName

</td>
<td valign="top">

BusinessPartner/person/nameDetails

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

BirthName

</td>
<td valign="top">

Name at birth of business partner.

</td>
<td valign="top">

BusinessPartner/Common/Person/Name/BirthName

</td>
<td valign="top">

birthName

</td>
<td valign="top">

BusinessPartner/person/nameDetails

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

InitialsName

</td>
<td valign="top">

"Middle Initial" or personal initials.

</td>
<td valign="top">

BusinessPartner/Common/Person/Name/InitialsName

</td>
<td valign="top">

initials

</td>
<td valign="top">

BusinessPartner/person/nameDetails

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

FormOfAddressCode

</td>
<td valign="top">

Title of Business Partner created.

</td>
<td valign="top">

BusinessPartner/Common/Person/Name/FormOfAddressCode

</td>
<td valign="top">

formOfAddress

</td>
<td valign="top">

BusinessPartner/person/nameDetails

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

AcademicTitleCode

</td>
<td valign="top">

Describes a name component that is an additional title of a natural person to indicate academic training.

</td>
<td valign="top">

BusinessPartner/Common/Person/Name/AcademicTitleCode

</td>
<td valign="top">

academicTitle

</td>
<td valign="top">

BusinessPartner/person/nameDetails

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

AdditionalAcademicTitleCode

</td>
<td valign="top">

Possible academic titles \(or academic qualifications\).

</td>
<td valign="top">

BusinessPartner/Common/Person/Name/AdditionalAcademicTitleCode

</td>
<td valign="top">

additionalAcademicTitle

</td>
<td valign="top">

BusinessPartner/person/nameDetails

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

NamePrefixCode

</td>
<td valign="top">

Key for name prefix.

</td>
<td valign="top">

BusinessPartner/Common/Person/Name/NamePrefixCode

</td>
<td valign="top">

namePrefix

</td>
<td valign="top">

BusinessPartner/person/nameDetails

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

AdditionalNamePrefixCode

</td>
<td valign="top">

An addition to the last name that is usually a title of nobility.

</td>
<td valign="top">

BusinessPartner/Common/Person/Name/AdditionalNamePrefixCode

</td>
<td valign="top">

additionalNamePrefix

</td>
<td valign="top">

BusinessPartner/person/nameDetails

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

NameSupplementCode

</td>
<td valign="top">

Describes a name component that is an additional title of a natural person to indicate noble origin. This could be a title of nobility, but there are other possibilities.

</td>
<td valign="top">

BusinessPartner/Common/Person/Name/NameSupplementCode

</td>
<td valign="top">

nameSuffix

</td>
<td valign="top">

BusinessPartner/person/nameDetails

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

NameFormatCountryCode

</td>
<td valign="top">

A country can have several formats which correspond to different rules. Formatting rules describe the format of a person name.

</td>
<td valign="top">

BusinessPartner/Common/Person/Name/NameFormatCountryCode

</td>
<td valign="top">

nameCountry

</td>
<td valign="top">

BusinessPartner/person/nameDetails

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

NameFormatCode

</td>
<td valign="top">

The name format specifies the sequence in which name components are assembled to present the name of a person in a complete form.

</td>
<td valign="top">

BusinessPartner/Common/Person/Name/NameFormatCode

</td>
<td valign="top">

nameFormat

</td>
<td valign="top">

BusinessPartner/person/nameDetails

</td>
</tr>
</table>



<a name="loio8a9a1305ac764111b648e3303f24c784__businesspartnersuitebulkreplicaterequest---organization"/>

## BusinessPartnerSUITEBulkReplicateRequest - Organization

This service node contains the following parameters:



<a name="loio8a9a1305ac764111b648e3303f24c784__soap-and-odm-mapping-information-2"/>

## SOAP and ODM Mapping Information


<table>
<tr>
<th valign="top">

SOAP Field Name

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

ODM Field Name

</th>
<th valign="top">

ODM Path

</th>
</tr>
<tr>
<td valign="top">

**Organization** 

</td>
<td valign="top">

FoundationDate

</td>
<td valign="top">

Indicates the official registration of a company in the Commercial Register.

</td>
<td valign="top">

BusinessPartner/Common/Organisation/FoundationDate

</td>
<td valign="top">

foundationDate

</td>
<td valign="top">

BusinessPartner/organization

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

CompanyLegalFormCode

</td>
<td valign="top">

Denotes certain legal norms that are of significance for the organization of a company.

</td>
<td valign="top">

BusinessPartner/Common/Organisation/CompanyLegalFormCode

</td>
<td valign="top">

legalForm

</td>
<td valign="top">

BusinessPartner/organization

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

LiquidationDate

</td>
<td valign="top">

Term for the end of bankruptcy proceedings. This date also indicates that the company no longer exists.

</td>
<td valign="top">

BusinessPartner/Common/Organisation/LiquidationDate

</td>
<td valign="top">

liquidationDate

</td>
<td valign="top">

BusinessPartner/organization

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

LocationStandardID

</td>
<td valign="top">

This field represents combination of InternationLocationNumber1, InternationLocationNumber2, InternationLocationNumber3.

</td>
<td valign="top">

BusinessPartner/Common/LocationStandardID

</td>
<td valign="top">

globalLocationNumber

</td>
<td valign="top">

BusinessPartner/organization

</td>
</tr>
<tr>
<td valign="top">

**OrganizationNameDetails** 

</td>
<td valign="top">

FirstLineName

</td>
<td valign="top">

Organisation Name Line1. First name field for business partners in the Organization category.

</td>
<td valign="top">

BusinessPartner/Common/Organisation/Name/FirstLineName

</td>
<td valign="top">

formattedOrgNameLine1

</td>
<td valign="top">

BusinessPartner/organization

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

SecondLineName

</td>
<td valign="top">

Organisation Name Line 2. Second name field for business partners in the Organization category.

</td>
<td valign="top">

BusinessPartner/Common/Organisation/Name/SecondLineName

</td>
<td valign="top">

formattedOrgNameLine2

</td>
<td valign="top">

BusinessPartner/organization

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

ThirdLineName

</td>
<td valign="top">

Organization Name Line 3. Third name field for business partners in the Organization category.

</td>
<td valign="top">

BusinessPartner/Common/Organisation/Name/ThirdLineName

</td>
<td valign="top">

formattedOrgNameLine3

</td>
<td valign="top">

BusinessPartner/organization

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

FourthLineName

</td>
<td valign="top">

Organisation Name Line 4. Fourth name field for business partners in the Organization category.

</td>
<td valign="top">

BusinessPartner/Common/Organisation/Name/FourthLineName

</td>
<td valign="top">

formattedOrgNameLine4

</td>
<td valign="top">

BusinessPartner/organization

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

FormOfAddressCode

</td>
<td valign="top">

Form-of-Address Key. Key for form of address text.

</td>
<td valign="top">

BusinessPartner/Common/Organisation/Name/FormOfAddressCode

</td>
<td valign="top">

formOfAddress

</td>
<td valign="top">

BusinessPartner/organization

</td>
</tr>
<tr>
<td valign="top">

**IndustrySector** 

</td>
<td valign="top">

IndustrialSectorCode

</td>
<td valign="top">

Describes an industry. An industry is a classification of companies according to their main business activity. For example, you can use Commerce, Banking, Services, Industry, Healthcare, Public Sector, Media, and so on, as industries.

</td>
<td valign="top">

BusinessPartner/IndustrySector/IndustrialSectorCode

</td>
<td valign="top">

industrySector

</td>
<td valign="top">

BusinessPartner/organization

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

DefaultIndicator

</td>
<td valign="top">

Identifies the industry in an industry system that can be defined as the standard industry.

</td>
<td valign="top">

BusinessPartner/IndustrySector/DefaultIndicator

</td>
<td valign="top">

isStandardIndustry

</td>
<td valign="top">

BusinessPartner/organization

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

IndustryClassificationSystemCode

</td>
<td valign="top">

Industry System. Serves to combine and categorize several industries into a group.

</td>
<td valign="top">

BusinessPartner/IndustrySector/IndustryClassificationSystemCode

</td>
<td valign="top">

industrySystemType

</td>
<td valign="top">

BusinessPartner/organization

</td>
</tr>
</table>



<a name="loio8a9a1305ac764111b648e3303f24c784__businesspartnersuitebulkreplicaterequest---identification"/>

## BusinessPartnerSUITEBulkReplicateRequest - Identification

This service node contains the following parameters:



<a name="loio8a9a1305ac764111b648e3303f24c784__soap-and-odm-mapping-information-3"/>

## SOAP and ODM Mapping Information


<table>
<tr>
<th valign="top">

SOAP Field Name

</th>
<th valign="top">

Description

</th>
<th valign="top">

SOAP Path

</th>
<th valign="top">

ODM Field Name

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

BusinessPartnerID

</td>
<td valign="top">

Number that serves to identify a business partner, such as driver's licence, or ID card number.

</td>
<td valign="top">

BusinessPartner/Identification/BusinessPartnerID

</td>
<td valign="top">

identificationNumber

</td>
<td valign="top">

BusinessPartner/identifications

</td>
<td valign="top">

Optional

</td>
</tr>
<tr>
<td valign="top">

PartyIdentifierTypeCode

</td>
<td valign="top">

A document \(such as an ID card or driver's licence\) or an entry in a system of records \(such as a commercial register\) whose key can be stored as an attribute for a business partner.

</td>
<td valign="top">

BusinessPartner/Identification/PartyIdentifierTypeCode

</td>
<td valign="top">

identificationType

</td>
<td valign="top">

BusinessPartner/identifications

</td>
<td valign="top">

Optional

</td>
</tr>
<tr>
<td valign="top">

EntryDate

</td>
<td valign="top">

Date of Entry for ID Number. Date on which the ID number was registered or assigned by the appropriate authority.

</td>
<td valign="top">

BusinessPartner/Identification/EntryDate

</td>
<td valign="top">

entryDate

</td>
<td valign="top">

BusinessPartner/identifications

</td>
<td valign="top">

Optional

</td>
</tr>
<tr>
<td valign="top">

AreaOfValidityCountryCode

</td>
<td valign="top">

Country in which ID number is valid or was assigned.

</td>
<td valign="top">

BusinessPartner/Identification/AreaOfValidityCountryCode

</td>
<td valign="top">

country

</td>
<td valign="top">

BusinessPartner/identifications

</td>
<td valign="top">

Optional

</td>
</tr>
<tr>
<td valign="top">

AreaOfValidityRegionCode

</td>
<td valign="top">

Region in which ID number is valid or was assigned.

</td>
<td valign="top">

BusinessPartner/Identification/AreaOfValidityRegionCode

</td>
<td valign="top">

region

</td>
<td valign="top">

BusinessPartner/identifications

</td>
<td valign="top">

Optional

</td>
</tr>
<tr>
<td valign="top">

IdentifierIssuingAgencyName

</td>
<td valign="top">

Institution that administers or assigns an ID number.

</td>
<td valign="top">

BusinessPartner/Identification/IdentifierIssuingAgencyName

</td>
<td valign="top">

institute

</td>
<td valign="top">

BusinessPartner/identifications

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

Validity Start Date of the master data object.

</td>
<td valign="top">

BusinessPartner/Identification/ValidityPeriod/StartDate

</td>
<td valign="top">

validFrom

</td>
<td valign="top">

BusinessPartner/identifications

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

Validity End Date of the master data object.

</td>
<td valign="top">

BusinessPartner/Identification/ValidityPeriod/EndDate

</td>
<td valign="top">

validTo

</td>
<td valign="top">

BusinessPartner/identifications

</td>
<td valign="top">

Optional

</td>
</tr>
</table>



<a name="loio8a9a1305ac764111b648e3303f24c784__businesspartnersuitebulkreplicaterequest---bankdetails"/>

## BusinessPartnerSUITEBulkReplicateRequest - BankDetails

This service node contains the following parameters:



<a name="loio8a9a1305ac764111b648e3303f24c784__soap-and-odm-mapping-information-4"/>

## SOAP and ODM Mapping Information


<table>
<tr>
<th valign="top">

SOAP Field Name

</th>
<th valign="top">

Description

</th>
<th valign="top">

SOAP Path

</th>
<th valign="top">

ODM Field Name

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

BankAccountID

</td>
<td valign="top">

The bank key \(under which the bank data is stored in the appropriate country\) is specified in this field.

</td>
<td valign="top">

BusinessPartner/BankDetails/BankAccountID

</td>
<td valign="top">

bankAccount

</td>
<td valign="top">

BusinessPartner/bankAccounts

</td>
<td valign="top">

Mandatory

</td>
</tr>
<tr>
<td valign="top">

BankCountryCode

</td>
<td valign="top">

Identifies the country in which the bank is based.

</td>
<td valign="top">

BusinessPartner/BankDetails/BankDirectoryReference/BankCountryCode

</td>
<td valign="top">

bankCountry

</td>
<td valign="top">

BusinessPartner/bankAccounts

</td>
<td valign="top">

Optional

</td>
</tr>
<tr>
<td valign="top">

BankInternalID

</td>
<td valign="top">

The bank key \(under which the bank data is stored in the appropriate country\) is specified in this field.The country-specific meaning of this bank key is specified when defining country key.

</td>
<td valign="top">

BusinessPartner/BankDetails/BankDirectoryReference/BankInternalID

</td>
<td valign="top">

bankNumber

</td>
<td valign="top">

BusinessPartner/bankAccounts

</td>
<td valign="top">

Optional

</td>
</tr>
<tr>
<td valign="top">

BankControlKey

</td>
<td valign="top">

The field contains a check key for the combination bank number and bank account number.

</td>
<td valign="top">

BusinessPartner/BankDetails/BankControlKey

</td>
<td valign="top">

bankControlKey

</td>
<td valign="top">

BusinessPartner/bankAccounts

</td>
<td valign="top">

Optional

</td>
</tr>
<tr>
<td valign="top">

BusinessPartnerExternalBankID

</td>
<td valign="top">

The field contains ID in the external system that provides information on the number under which the bank details were created in the legacy or operational system.

</td>
<td valign="top">

BusinessPartner/BankDetails/BusinessPartnerExternalBankID

</td>
<td valign="top">

businessPartnerExternalBankId

</td>
<td valign="top">

BusinessPartner/bankAccounts

</td>
<td valign="top">

Optional

</td>
</tr>
<tr>
<td valign="top">

Name

</td>
<td valign="top">

Name of Bank Account.

</td>
<td valign="top">

BusinessPartner/BankDetails/Name

</td>
<td valign="top">

bankAccountName

</td>
<td valign="top">

BusinessPartner/bankAccounts

</td>
<td valign="top">

Optional

</td>
</tr>
<tr>
<td valign="top">

BankAccountHolderName

</td>
<td valign="top">

Bank Account Holder Name. Here you can enter another name that the payment program can use if the name of the account holder is not the same as the name of the Business Partner.

</td>
<td valign="top">

BusinessPartner/BankDetails/BankAccountHolderName

</td>
<td valign="top">

bankAccountHolderName

</td>
<td valign="top">

BusinessPartner/bankAccounts

</td>
<td valign="top">

Optional

</td>
</tr>
<tr>
<td valign="top">

BankAccountStandardID

</td>
<td valign="top">

An IBAN \(International Bank Account Number\) has a maximum of 34 alphanumeric characters and is a combination of the following elements: Country key of the bank \(ISO code\), two-digit check number, country-specific account number.

</td>
<td valign="top">

BusinessPartner/BankDetails/BankAccountStandardID

</td>
<td valign="top">

IBAN

</td>
<td valign="top">

BusinessPartner/bankAccounts

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

Validity Start of Business Partner Bank Details

</td>
<td valign="top">

BusinessPartner/BankDetails/ValidityPeriod/StartDate

</td>
<td valign="top">

validFrom

</td>
<td valign="top">

BusinessPartner/bankAccounts

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

Validity End of Business Partner Bank Details.

</td>
<td valign="top">

BusinessPartner/BankDetails/ValidityPeriod/EndDate

</td>
<td valign="top">

validTo

</td>
<td valign="top">

BusinessPartner/bankAccounts

</td>
<td valign="top">

Optional

</td>
</tr>
<tr>
<td valign="top">

SpecificationsDescription

</td>
<td valign="top">

In some countries the data for the bank details of the business partner \(bank number, bank account number, name of the account holder\) have to be supplemented by other details in order to be able to use certain payment processes. This supplementary details are defined here.

</td>
<td valign="top">

BusinessPartner/BankDetails/SpecificationsDescription

</td>
<td valign="top">

bankAccountReference

</td>
<td valign="top">

BusinessPartner/bankAccounts

</td>
<td valign="top">

Optional

</td>
</tr>
<tr>
<td valign="top">

ID

</td>
<td valign="top">

Key identifying a business partner's bank details.

</td>
<td valign="top">

BusinessPartner/BankDetails/ID

</td>
<td valign="top">

id

</td>
<td valign="top">

BusinessPartner/bankAccounts

</td>
<td valign="top">

Mandatory

</td>
</tr>
</table>



<a name="loio8a9a1305ac764111b648e3303f24c784__businesspartnersuitebulkreplicaterequest---taxnumber"/>

## BusinessPartnerSUITEBulkReplicateRequest - TaxNumber

This service node contains the following parameters:



<a name="loio8a9a1305ac764111b648e3303f24c784__soap-and-odm-mapping-information-5"/>

## SOAP and ODM Mapping Information


<table>
<tr>
<th valign="top">

SOAP Field Name

</th>
<th valign="top">

Description

</th>
<th valign="top">

SOAP Path

</th>
<th valign="top">

ODM Field Name

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

PartyTaxID

</td>
<td valign="top">

Specifies the tax number.

</td>
<td valign="top">

BusinessPartner/TaxNumber/PartyTaxID

</td>
<td valign="top">

taxNumber

</td>
<td valign="top">

BusinessPartner/taxNumbers

</td>
<td valign="top">

Optional

</td>
</tr>
<tr>
<td valign="top">

PartyRoleCode

</td>
<td valign="top">

Specifies the tax number category.

</td>
<td valign="top">

BusinessPartner/TaxNumber/PartyRoleCode

</td>
<td valign="top">

taxNumberType

</td>
<td valign="top">

BusinessPartner/taxNumbers

</td>
<td valign="top">

Optional

</td>
</tr>
</table>



<a name="loio8a9a1305ac764111b648e3303f24c784__businesspartnersuitebulkreplicaterequest---role"/>

## BusinessPartnerSUITEBulkReplicateRequest - Role

This service node contains the following parameters:



<a name="loio8a9a1305ac764111b648e3303f24c784__soap-and-odm-mapping-information-6"/>

## SOAP and ODM Mapping Information


<table>
<tr>
<th valign="top">

SOAP Field Name

</th>
<th valign="top">

Description

</th>
<th valign="top">

SOAP Path

</th>
<th valign="top">

ODM Field Name

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

Function that a business partner takes on, depending on a business transaction. You can define business partner roles along with their attributes in Customizing.

</td>
<td valign="top">

BusinessPartner/Role/RoleCode

</td>
<td valign="top">

role

</td>
<td valign="top">

BusinessPartner/roles

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

Validity Start Date of the master data object.

</td>
<td valign="top">

BusinessPartner/Role/ValidityPeriod/StartDate

</td>
<td valign="top">

validFrom

</td>
<td valign="top">

BusinessPartner/roles

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

Validity End Date of the master data object.

</td>
<td valign="top">

BusinessPartner/Role/ValidityPeriod/EndDate

</td>
<td valign="top">

validTo

</td>
<td valign="top">

BusinessPartner/roles

</td>
<td valign="top">

Optional

</td>
</tr>
</table>



<a name="loio8a9a1305ac764111b648e3303f24c784__businesspartnersuitebulkreplicaterequest---business-partner-group"/>

## BusinessPartnerSUITEBulkReplicateRequest - Business Partner Group

This service node contains the following parameters:



<a name="loio8a9a1305ac764111b648e3303f24c784__soap-and-odm-mapping-information-7"/>

## SOAP and ODM Mapping Information


<table>
<tr>
<th valign="top">

SOAP Field Name

</th>
<th valign="top">

Description

</th>
<th valign="top">

SOAP Path

</th>
<th valign="top">

ODM Field Name

</th>
<th valign="top">

ODM Path

</th>
</tr>
<tr>
<td valign="top">

PartnerGroupTypeCode

</td>
<td valign="top">

Business partner that consists of several persons or organizations. For business partners belonging to the category "Group", you can specify the type of group involved. You can define the group types in Customizing.

</td>
<td valign="top">

BusinessPartner/Common/Group/PartnerGroupTypeCode

</td>
<td valign="top">

groupType

</td>
<td valign="top">

BusinessPartner/businessPartnerGroup

</td>
</tr>
<tr>
<td valign="top">

Name

</td>
<td valign="top">

First name field for business partners in the Group category.

</td>
<td valign="top">

BusinessPartner/Common/Group/Name

</td>
<td valign="top">

primaryGroupName

</td>
<td valign="top">

BusinessPartner/businessPartnerGroup

</td>
</tr>
<tr>
<td valign="top">

AdditionalName

</td>
<td valign="top">

Second name field for business partners in the Group category.

</td>
<td valign="top">

BusinessPartner/Common/Group/AdditionalName

</td>
<td valign="top">

secondaryGroupName

</td>
<td valign="top">

BusinessPartner/businessPartnerGroup

</td>
</tr>
<tr>
<td valign="top">

FormOfAddress

</td>
<td valign="top">

Key for form of address text. You can also define a form of address text in Customizing. The form of address text can be maintained in different languages.

</td>
<td valign="top">

BusinessPartner/Common/Group/FormOfAddressCode

</td>
<td valign="top">

formOfAddress

</td>
<td valign="top">

BusinessPartner/businessPartnerGroup

</td>
</tr>
</table>



<a name="loio8a9a1305ac764111b648e3303f24c784__businesspartnersuitebulkreplicaterequest---address-data"/>

## BusinessPartnerSUITEBulkReplicateRequest - Address Data

This service node contains the following parameters:



<a name="loio8a9a1305ac764111b648e3303f24c784__soap-and-odm-mapping-information-8"/>

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

**Address Data** 

</td>
<td valign="top">

StartDate

</td>
<td valign="top">

Address validity start date.

</td>
<td valign="top">

BusinessPartner/AddressInformation/ValidityPeriod/StartDate

</td>
<td valign="top">

validFrom

</td>
<td valign="top">

BusinessPartner/addressData/

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

EndDate

</td>
<td valign="top">

Address validity end date.

</td>
<td valign="top">

BusinessPartner/AddressInformation/ValidityPeriod/EndDate

</td>
<td valign="top">

validTo

</td>
<td valign="top">

BusinessPartner/addressData/

</td>
</tr>
<tr>
<td valign="top">

**CommunicationPreference** 

</td>
<td valign="top">

CorrespondenceLanguage

</td>
<td valign="top">

Correspondence language \(written\) for business partners in the Person category. Correspondence Language; The language key indicates the language in which texts are displayed, the language in which you enter texts, the language in which the system prints texts.

</td>
<td valign="top">

BusinessPartner/AddressInformation/Address/CommunicationPreference/CorrespondenceLanguageCode

</td>
<td valign="top">

nonVerbalCommunicationLanguage

</td>
<td valign="top">

BusinessPartner/addressData/communicationPreferences

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

PreferredCommunicationMediumTypeCode

</td>
<td valign="top">

Preferred Medium of Communication \(Phone/Email etc.\).

</td>
<td valign="top">

BusinessPartner/AddressInformation/Address/CommunicationPreference/PreferredCommunicationMediumTypeCode

</td>
<td valign="top">

communicationMethod

</td>
<td valign="top">

BusinessPartner/addressData/communicationPreferences

</td>
</tr>
<tr>
<td valign="top">

**Email Address** 

</td>
<td valign="top">

URI

</td>
<td valign="top">

E-Mail Address. Internet mail address, also called e-mail address.

</td>
<td valign="top">

BusinessPartner/AddressInformation/Address/Email/URI, BusinessPartnerRelationship/ContactPerson/WorkplaceAddressInformation/Address/Email/URI

</td>
<td valign="top">

address

</td>
<td valign="top">

BusinessPartner/addressData/emailAddresses

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

UsageDeniedIndicator

</td>
<td valign="top">

 

</td>
<td valign="top">

BusinessPartner/AddressInformation/Address/Email/UsageDeniedIndicator,BusinessPartnerRelationship/ContactPerson/WorkplaceAddressInformation/Address/Email/UsageDeniedIndicator

</td>
<td valign="top">

usageDeniedIndicator

</td>
<td valign="top">

BusinessPartner/addressData/emailAddresses

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

StartDate

</td>
<td valign="top">

Validity for email address Start Date.

</td>
<td valign="top">

BusinessPartner/AddressInformation/Address/Email/ValidityPeriod/StartDate,BusinessPartnerRelationship/ContactPerson/WorkplaceAddressInformation/Address/Email/ValidityPeriod/StartDate

</td>
<td valign="top">

validFrom

</td>
<td valign="top">

BusinessPartner/addressData/emailAddresses

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

EndDate

</td>
<td valign="top">

Validity for email address End Date.

</td>
<td valign="top">

BusinessPartner/AddressInformation/Address/Email/ValidityPeriod/EndDate,BusinessPartnerRelationship/ContactPerson/WorkplaceAddressInformation/Address/Email/ValidityPeriod/EndDate

</td>
<td valign="top">

validTo

</td>
<td valign="top">

BusinessPartner/addressData/emailAddresses

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

IsDefaultEmailAddress

</td>
<td valign="top">

Flag: this address is the default address.

</td>
<td valign="top">

BusinessPartner/AddressInformation/Address/Email/IsDefaultEmailAddress,BusinessPartnerRelationship/ContactPerson/WorkplaceAddressInformation/Address/Email/IsDefaultEmailAddress

</td>
<td valign="top">

isDefault

</td>
<td valign="top">

BusinessPartner/addressData/emailAddresses

</td>
</tr>
<tr>
<td valign="top">

**Fax Numbers** 

</td>
<td valign="top">

CountryCode

</td>
<td valign="top">

The country for the telephone number or fax number is maintained here.

</td>
<td valign="top">

BusinessPartner/AddressInformation/Address/Facsimile/Number/CountryCode,BusinessPartnerRelationship/ContactPerson/WorkplaceAddressInformation/Address/Facsimile/Number/CountryCode

</td>
<td valign="top">

country

</td>
<td valign="top">

BusinessPartner/addressData/faxNumbers

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

SubscriberID

</td>
<td valign="top">

Fax number, consisting of dialing code and number, but without country dialing code.

</td>
<td valign="top">

BusinessPartner/AddressInformation/Address/Facsimile/Number/SubscriberID, BusinessPartnerRelationship/ContactPerson/WorkplaceAddressInformation/Address/Facsimile/Number/SubscriberID

</td>
<td valign="top">

number

</td>
<td valign="top">

BusinessPartner/addressData/faxNumbers

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

ExtensionID

</td>
<td valign="top">

If the fax number consists of a company number and an extension, the extension must be entered here.

</td>
<td valign="top">

BusinessPartner/AddressInformation/Address/Facsimile/Number/ExtensionID, BusinessPartnerRelationship/ContactPerson/WorkplaceAddressInformation/Address/Facsimile/Number/ExtensionID

</td>
<td valign="top">

numberExtension

</td>
<td valign="top">

BusinessPartner/addressData/faxNumbers

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

UsageDeniedIndicator

</td>
<td valign="top">

 

</td>
<td valign="top">

BusinessPartner/AddressInformation/Address/Facsimile/UsageDeniedIndicator,BusinessPartnerRelationship/ContactPerson/WorkplaceAddressInformation/Address/Facsimile/UsageDeniedIndicator

</td>
<td valign="top">

usageDeniedIndicator

</td>
<td valign="top">

BusinessPartner/addressData/faxNumbers

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

StartDate

</td>
<td valign="top">

Validity for fax address Start date.

</td>
<td valign="top">

BusinessPartner/AddressInformation/Address/Facsimile/ValidityPeriod/StartDate,BusinessPartnerRelationship/ContactPerson/WorkplaceAddressInformation/Address/Facsimile/ValidityPeriod/StartDate

</td>
<td valign="top">

validFrom

</td>
<td valign="top">

BusinessPartner/addressData/faxNumbers

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

EndDate

</td>
<td valign="top">

Validity for fax address end date.

</td>
<td valign="top">

BusinessPartner/AddressInformation/Address/Facsimile/ValidityPeriod/EndDate,BusinessPartnerRelationship/ContactPerson/WorkplaceAddressInformation/Address/Facsimile/ValidityPeriod/EndDate

</td>
<td valign="top">

validTo

</td>
<td valign="top">

BusinessPartner/addressData/faxNumbers

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

IsDefaultFaxNumber

</td>
<td valign="top">

Standard Sender Address in this Communication Type.

</td>
<td valign="top">

BusinessPartner/AddressInformation/Address/Telephone/IsDefaultFaxNumber, BusinessPartnerRelationship/ContactPerson/WorkplaceAddressInformation/Address/Telephone/IsDefaultFaxNumber

</td>
<td valign="top">

isDefault

</td>
<td valign="top">

BusinessPartner/addressData/faxNumbers

</td>
</tr>
<tr>
<td valign="top">

**Phone Numbers** 

</td>
<td valign="top">

CountryCode

</td>
<td valign="top">

The country for the telephone number or fax number is maintained here.

</td>
<td valign="top">

BusinessPartner/AddressInformation/Address/Telephone/Number/CountryCode,BusinessPartnerRelationship/ContactPerson/WorkplaceAddressInformation/Address/Telephone/Number/CountryCode

</td>
<td valign="top">

country

</td>
<td valign="top">

BusinessPartner/addressData/phoneNumbers

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

SubscriberID

</td>
<td valign="top">

Telephone number, consisting of dialing code and number, but without country dialing code.

</td>
<td valign="top">

BusinessPartner/AddressInformation/Address/Telephone/Number/SubscriberID, BusinessPartnerRelationship/ContactPerson/WorkplaceAddressInformation/Address/Telephone/Number/SubscriberID

</td>
<td valign="top">

number

</td>
<td valign="top">

BusinessPartner/addressData/phoneNumbers

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

ExtensionID

</td>
<td valign="top">

If the telephone number consists of a company number and an extension, the extension should be entered here.

</td>
<td valign="top">

BusinessPartner/AddressInformation/Address/Telephone/Number/ExtensionID, BusinessPartnerRelationship/ContactPerson/WorkplaceAddressInformation/Address/Telephone/Number/ExtensionID

</td>
<td valign="top">

numberExtension

</td>
<td valign="top">

BusinessPartner/addressData/phoneNumbers

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

UsageDeniedIndicator

</td>
<td valign="top">

 

</td>
<td valign="top">

BusinessPartner/AddressInformation/Address/Telephone/UsageDeniedIndicator,BusinessPartnerRelationship/ContactPerson/WorkplaceAddressInformation/Address/Telephone/UsageDeniedIndicator

</td>
<td valign="top">

usageDeniedIndicator

</td>
<td valign="top">

BusinessPartner/addressData/phoneNumbers

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

StartDate

</td>
<td valign="top">

Validity Start Date of the master data object.

</td>
<td valign="top">

BusinessPartner/AddressInformation/Address/Telephone/ValidityPeriod/StartDate,BusinessPartnerRelationship/ContactPerson/WorkplaceAddressInformation/Address/Telephone/ValidityPeriod/StartDate

</td>
<td valign="top">

validFrom

</td>
<td valign="top">

BusinessPartner/addressData/phoneNumbers

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

EndDate

</td>
<td valign="top">

Validity End Date of the master data object.

</td>
<td valign="top">

BusinessPartner/AddressInformation/Address/Telephone/ValidityPeriod/EndDate,BusinessPartnerRelationship/ContactPerson/WorkplaceAddressInformation/Address/Telephone/ValidityPeriod/EndDate

</td>
<td valign="top">

validTo

</td>
<td valign="top">

BusinessPartner/addressData/phoneNumbers

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

SMSEnabledIndicator

</td>
<td valign="top">

Indicator: Telephone is SMS-Enabled.

</td>
<td valign="top">

BusinessPartner/AddressInformation/Address/Telephone/SMSEnabledIndicator,BusinessPartnerRelationship/ContactPerson/WorkplaceAddressInformation/Address/Telephone/SMSEnabledIndicator

</td>
<td valign="top">

smsEnabledIndicator

</td>
<td valign="top">

BusinessPartner/addressData/phoneNumbers

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

UUID

</td>
<td valign="top">

 

</td>
<td valign="top">

BusinessPartner/AddressInformation/UUID

</td>
<td valign="top">

id

</td>
<td valign="top">

BusinessPartner/addressData/phoneNumbers

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

IsDefaultPhoneNumber

</td>
<td valign="top">

Standard Sender Address in this Communication Type.

</td>
<td valign="top">

BusinessPartner/AddressInformation/Address/Telephone/IsDefaultPhoneNumber,BusinessPartnerRelationship/ContactPerson/WorkplaceAddressInformation/Address/Telephone/IsDefaultPhoneNumber

</td>
<td valign="top">

isDefault

</td>
<td valign="top">

BusinessPartner/addressData/phoneNumbers

</td>
</tr>
<tr>
<td valign="top">

**Websites** 

</td>
<td valign="top">

IsDefaultUri

</td>
<td valign="top">

Flag: this URI is the default URI.

</td>
<td valign="top">

BusinessPartner/AddressInformation/Address/Web/IsDefaultUri, BusinessPartnerRelationship/ContactPerson/WorkplaceAddressInformation/Address/Web/IsDefaultUri

</td>
<td valign="top">

isDefault

</td>
<td valign="top">

BusinessPartner/addressData/websites

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

URI

</td>
<td valign="top">

Website Address. Universal Resource Identifier \(URI\).

</td>
<td valign="top">

BusinessPartner/AddressInformation/Address/Web/URI, BusinessPartnerRelationship/ContactPerson/WorkplaceAddressInformation/Address/Web/URI

</td>
<td valign="top">

url

</td>
<td valign="top">

BusinessPartner/addressData/websites

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

URITypeCode

</td>
<td valign="top">

URI type flag Eg. HPG: Homepage, FTP, Log : Company Logo etc.

</td>
<td valign="top">

BusinessPartner/AddressInformation/Address/Web/URITypeCode, BusinessPartnerRelationship/ContactPerson/WorkplaceAddressInformation/Address/Web/URITypeCode

</td>
<td valign="top">

uriType

</td>
<td valign="top">

BusinessPartner/addressData/websites

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

StartDate

</td>
<td valign="top">

Validity Start Date of the master data object.

</td>
<td valign="top">

BusinessPartner/AddressInformation/Address/Web/ValidityPeriod/StartDate, BusinessPartnerRelationship/ContactPerson/WorkplaceAddressInformation/Address/Web/ValidityPeriod/StartDate

</td>
<td valign="top">

validFrom

</td>
<td valign="top">

BusinessPartner/addressData/websites

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

EndDate

</td>
<td valign="top">

Validity End Date of the master data object.

</td>
<td valign="top">

BusinessPartner/AddressInformation/Address/Web/ValidityPeriod/EndDate,BusinessPartnerRelationship/ContactPerson/WorkplaceAddressInformation/Address/Web/ValidityPeriod/EndDate

</td>
<td valign="top">

validTo

</td>
<td valign="top">

BusinessPartner/addressData/websites

</td>
</tr>
<tr>
<td valign="top">

**Person Postal Address** 

</td>
<td valign="top">

RoomID

</td>
<td valign="top">

Room or Apartment Number in an address.

</td>
<td valign="top">

BusinessPartner/AddressInformation/Address/PostalAddress/RoomID

</td>
<td valign="top">

door

</td>
<td valign="top">

BusinessPartner/addressData/personPostalAddress

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

CountryCode

</td>
<td valign="top">

The country key contains information which the system uses to check entries such as the length of the postal code or bank account number.

</td>
<td valign="top">

BusinessPartner/AddressInformation/Address/PostalAddress/CountryCode

</td>
<td valign="top">

country

</td>
<td valign="top">

BusinessPartner/addressData/personPostalAddress

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

GivenName

</td>
<td valign="top">

First Name of Business Partner \(Person\).

</td>
<td valign="top">

BusinessPartner/Common/Person/Name/GivenName

</td>
<td valign="top">

firstName

</td>
<td valign="top">

BusinessPartner/person/nameDetails

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

MiddleName

</td>
<td valign="top">

Middle name or second forename of a person.

</td>
<td valign="top">

BusinessPartner/Common/Person/Name/MiddleName

</td>
<td valign="top">

middleName

</td>
<td valign="top">

BusinessPartner/person/nameDetails

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

FamilyName

</td>
<td valign="top">

Last Name of Business Partner \(Person\).

</td>
<td valign="top">

BusinessPartner/Common/Person/Name/FamilyName

</td>
<td valign="top">

lastName

</td>
<td valign="top">

BusinessPartner/person/nameDetails

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

AdditionalFamilyName

</td>
<td valign="top">

Other Last Name of a Person.

</td>
<td valign="top">

BusinessPartner/Common/Person/Name/AdditionalFamilyName

</td>
<td valign="top">

secondLastName

</td>
<td valign="top">

BusinessPartner/person/nameDetails

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

InitialsName

</td>
<td valign="top">

"Middle Initial" or personal initials.

</td>
<td valign="top">

BusinessPartner/Common/Person/Name/InitialsName

</td>
<td valign="top">

initials

</td>
<td valign="top">

BusinessPartner/person/nameDetails

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

FormOfAddressCode

</td>
<td valign="top">

Title of Business Partner created.

</td>
<td valign="top">

BusinessPartner/Common/Person/Name/FormOfAddressCode

</td>
<td valign="top">

formOfAddress

</td>
<td valign="top">

BusinessPartner/person/nameDetails

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

AcademicTitleCode

</td>
<td valign="top">

Key for academic title. Describes a name component that is an additional title of a natural person to indicate academic training.

</td>
<td valign="top">

BusinessPartner/Common/Person/Name/AcademicTitleCode

</td>
<td valign="top">

academicTitle

</td>
<td valign="top">

BusinessPartner/person/nameDetails

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

AdditionalAcademicTitleCode

</td>
<td valign="top">

Second academic title \(key\). Possible academic titles \(or academic qualifications\).

</td>
<td valign="top">

BusinessPartner/Common/Person/Name/AdditionalAcademicTitleCode

</td>
<td valign="top">

additionalacademicTitle

</td>
<td valign="top">

BusinessPartner/person/nameDetails

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

NamePrefixCode

</td>
<td valign="top">

Key for name prefix. An addition to the last name that is usually a title of nobility.

</td>
<td valign="top">

BusinessPartner/Common/Person/Name/NamePrefixCode

</td>
<td valign="top">

namePrefix

</td>
<td valign="top">

BusinessPartner/person/nameDetails

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

AdditionalNamePrefixCode

</td>
<td valign="top">

2nd name prefix \(key\). An addition to the last name that is usually a title of nobility.

</td>
<td valign="top">

BusinessPartner/Common/Person/Name/AdditionalNamePrefixCode

</td>
<td valign="top">

additionalNamePrefix

</td>
<td valign="top">

BusinessPartner/person/nameDetails

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

NameSupplementCode

</td>
<td valign="top">

Describes a name component that is an additional title of a natural person to indicate noble origin. This could be a title of nobility, but there are other possibilities.

</td>
<td valign="top">

BusinessPartner/Common/Person/Name/NameSupplementCode

</td>
<td valign="top">

nameSuffix

</td>
<td valign="top">

BusinessPartner/person/nameDetails

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

NameFormatCountryCode

</td>
<td valign="top">

A country can have several formats which correspond to different rules. Formatting rules describe the format of a person name.

</td>
<td valign="top">

BusinessPartner/Common/Person/Name/NameFormatCountryCode

</td>
<td valign="top">

nameCountry

</td>
<td valign="top">

BusinessPartner/person/nameDetails

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

NameFormatCode

</td>
<td valign="top">

The name format specifies the sequence in which name components are assembled to present the name of a person in a complete form.

</td>
<td valign="top">

BusinessPartner/Common/Person/Name/NameFormatCode

</td>
<td valign="top">

nameFormat

</td>
<td valign="top">

BusinessPartner/person/nameDetails

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

NickName

</td>
<td valign="top">

Nickname of Business Partner \(Person\).

</td>
<td valign="top">

BusinessPartner/Common/Person/Name/NickName

</td>
<td valign="top">

nickName

</td>
<td valign="top">

BusinessPartner/person/nameDetails

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

BirthName

</td>
<td valign="top">

Name at birth of business partner.

</td>
<td valign="top">

BusinessPartner/Common/Person/Name/BirthName

</td>
<td valign="top">

birthName

</td>
<td valign="top">

BusinessPartner/person/nameDetails

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

DeviatingFullName

</td>
<td valign="top">

If the SOAP field DeviatingFullName is left blank, then the corresponding ODM field, formattedPersonName will also remains blank.

</td>
<td valign="top">

BusinessPartner/Common/Person/Name/DeviatingFullName

</td>
<td valign="top">

formattedPersonName

</td>
<td valign="top">

BusinessPartner/addressData/personPostalAddress

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

HouseID

</td>
<td valign="top">

House number as part of an address.

</td>
<td valign="top">

BusinessPartner/AddressInformation/Address/PostalAddress/HouseID

</td>
<td valign="top">

houseNumber

</td>
<td valign="top">

BusinessPartner/addressData/personPostalAddress

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

POBoxIDVisibleIndicator

</td>
<td valign="top">

PO Box address without PO Box number flag.

</td>
<td valign="top">

BusinessPartner/AddressInformation/Address/PostalAddress/POBoxIDVisibleIndicator

</td>
<td valign="top">

postBoxIsWithoutNumber

</td>
<td valign="top">

BusinessPartner/addressData/personPostalAddress

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

StreetName

</td>
<td valign="top">

Street name as part of the address.

</td>
<td valign="top">

BusinessPartner/AddressInformation/Address/PostalAddress/StreetName

</td>
<td valign="top">

street

</td>
<td valign="top">

BusinessPartner/addressData/personPostalAddress

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

StreetSuffixName

</td>
<td valign="top">

Additional address text line for Street.

</td>
<td valign="top">

BusinessPartner/AddressInformation/Address/PostalAddress/StreetSuffixName

</td>
<td valign="top">

streetSuffix1

</td>
<td valign="top">

BusinessPartner/addressData/personPostalAddress

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

StreetPrefixName

</td>
<td valign="top">

Additional address field which is printed below the Street line.

</td>
<td valign="top">

BusinessPartner/AddressInformation/Address/PostalAddress/StreetPrefixName

</td>
<td valign="top">

streetPrefix1

</td>
<td valign="top">

BusinessPartner/addressData/personPostalAddress

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

AdditionalStreetPrefixName

</td>
<td valign="top">

Additional address field which is printed above the Street line.

</td>
<td valign="top">

BusinessPartner/AddressInformation/Address/PostalAddress/AdditionalStreetPrefixName

</td>
<td valign="top">

streetPrefix2

</td>
<td valign="top">

BusinessPartner/addressData/personPostalAddress

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

AdditionalStreetSuffixName

</td>
<td valign="top">

Additional address field which is printed under the Street line.

</td>
<td valign="top">

BusinessPartner/AddressInformation/Address/PostalAddress/AdditionalStreetSuffixName

</td>
<td valign="top">

streetSuffix2

</td>
<td valign="top">

BusinessPartner/addressData/personPostalAddress

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

FloorID

</td>
<td valign="top">

Floor of the building as more exact specification of an address.

</td>
<td valign="top">

BusinessPartner/AddressInformation/Address/PostalAddress/FloorID

</td>
<td valign="top">

floor

</td>
<td valign="top">

BusinessPartner/addressData/personPostalAddress

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

CompanyPostalCode

</td>
<td valign="top">

This field is used for countries where major companies are assigned their own postal code by the national post office.

</td>
<td valign="top">

BusinessPartner/AddressInformation/Address/PostalAddress/CompanyPostalCode

</td>
<td valign="top">

companyPostalCode

</td>
<td valign="top">

BusinessPartner/addressData/personPostalAddress

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

RegionCode

</td>
<td valign="top">

Region Key. For example, Washington is a Region of USA, Karnataka is region of India etc.

</td>
<td valign="top">

BusinessPartner/AddressInformation/Address/PostalAddress/RegionCode

</td>
<td valign="top">

primaryRegion

</td>
<td valign="top">

BusinessPartner/addressData/personPostalAddress

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

CountyName

</td>
<td valign="top">

 

</td>
<td valign="top">

BusinessPartner/AddressInformation/Address/PostalAddress/CountyName

</td>
<td valign="top">

secondaryRegion

</td>
<td valign="top">

BusinessPartner/addressData/personPostalAddress

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

CityName

</td>
<td valign="top">

 

</td>
<td valign="top">

BusinessPartner/AddressInformation/Address/PostalAddress/CityName

</td>
<td valign="top">

town

</td>
<td valign="top">

BusinessPartner/addressData/personPostalAddress

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

POBoxDeliveryServiceID

</td>
<td valign="top">

 

</td>
<td valign="top">

BusinessPartner/AddressInformation/Address/PostalAddress/POBoxDeliveryServiceID

</td>
<td valign="top">

deliveryServiceNumber

</td>
<td valign="top">

BusinessPartner/addressData/personPostalAddress

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

TimeZoneCode

</td>
<td valign="top">

Address Time Zone.

</td>
<td valign="top">

BusinessPartner/AddressInformation/Address/PostalAddress/TimeZoneCode

</td>
<td valign="top">

timeZone

</td>
<td valign="top">

BusinessPartner/addressData/personPostalAddress

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

AdditionalRegionalStructureCityCode

</td>
<td valign="top">

 

</td>
<td valign="top">

BusinessPartner/AddressInformation/Address/PostalAddress/AdditionalRegionalStructureCityCode

</td>
<td valign="top">

additionalCityName

</td>
<td valign="top">

BusinessPartner/addressData/personPostalAddress

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

CareOfName

</td>
<td valign="top">

c/o name; Part of the address \(c/o = care of\) if the recipient is different from the occupant and the names are not similar \(e.g. subtenants\).

</td>
<td valign="top">

BusinessPartner/AddressInformation/Address/PostalAddress/CareOfName

</td>
<td valign="top">

careOf

</td>
<td valign="top">

BusinessPartner/addressData/personPostalAddress

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

TransportationZoneID

</td>
<td valign="top">

Transportation zone to or from which the goods are delivered.

</td>
<td valign="top">

BusinessPartner/AddressInformation/Address/PostalAddress/TransportationZoneID

</td>
<td valign="top">

transportationZone

</td>
<td valign="top">

BusinessPartner/addressData/personPostalAddress

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

TaxJurisdictionCode

</td>
<td valign="top">

The tax jurisdiction code defines the tax authority to which taxes must be paid.

</td>
<td valign="top">

BusinessPartner/AddressInformation/Address/PostalAddress/TaxJurisdictionCode

</td>
<td valign="top">

taxJurisdiction

</td>
<td valign="top">

BusinessPartner/addressData/personPostalAddress

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

DistrictName

</td>
<td valign="top">

In some countries, this entry is appended with a hyphen to the city name by the automatic address formatting, other countries, it is output on a line of its own or \(For example, in the USA\) not printed.

</td>
<td valign="top">

BusinessPartner/AddressInformation/Address/PostalAddress/DistrictName

</td>
<td valign="top">

district

</td>
<td valign="top">

BusinessPartner/addressData/personPostalAddress

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

AdditionalHouseID

</td>
<td valign="top">

House number supplement.

</td>
<td valign="top">

BusinessPartner/AddressInformation/Address/PostalAddress/AdditionalHouseID

</td>
<td valign="top">

houseNumberSupplement

</td>
<td valign="top">

BusinessPartner/addressData/personPostalAddress

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

StreetPostalCode

</td>
<td valign="top">

If different postal codes are maintained for the PO Box and Street address of an address, this field contains the Street address postal code.

</td>
<td valign="top">

BusinessPartner/AddressInformation/Address/PostalAddress/StreetPostalCode

</td>
<td valign="top">

postCode

</td>
<td valign="top">

BusinessPartner/addressData/personPostalAddress

</td>
</tr>
<tr>
<td valign="top">

**Alternative - Person Address** 

</td>
<td valign="top">

POBoxDeviatingCountryCode

</td>
<td valign="top">

PO Box Country

</td>
<td valign="top">

BusinessPartner/AddressInformation/Address/PostalAddress/POBoxDeviatingCountryCode

</td>
<td valign="top">

country

</td>
<td valign="top">

BusinessPartner/addressData/personPostalAddress/alternative

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

POBoxDeviatingRegionCode

</td>
<td valign="top">

Region for PO Box \(Country, State, Province, etc.\).

</td>
<td valign="top">

BusinessPartner/AddressInformation/Address/PostalAddress/POBoxDeviatingRegionCode

</td>
<td valign="top">

primaryRegion

</td>
<td valign="top">

BusinessPartner/addressData/personPostalAddress/alternative

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

POBoxDeviatingCityName

</td>
<td valign="top">

PO Box city.

</td>
<td valign="top">

BusinessPartner/AddressInformation/Address/PostalAddress/POBoxDeviatingCityName

</td>
<td valign="top">

town

</td>
<td valign="top">

BusinessPartner/addressData/personPostalAddress/alternative

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

POBoxPostalCode

</td>
<td valign="top">

Postal code that is required for a unique assignment of the PO box; This field is used for countries where a different postal code applies to mail that is sent to the PO box rather than to the street address of a particular business partner.

</td>
<td valign="top">

BusinessPartner/AddressInformation/Address/PostalAddress/POBoxPostalCode

</td>
<td valign="top">

postCode

</td>
<td valign="top">

BusinessPartner/addressData/personPostalAddress/alternative

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

POBoxLobbyName

</td>
<td valign="top">

PO Box Lobby.

</td>
<td valign="top">

BusinessPartner/AddressInformation/Address/PostalAddress/POBoxLobbyName

</td>
<td valign="top">

deliveryServiceQualifier

</td>
<td valign="top">

BusinessPartner/addressData/personPostalAddress/alternative

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

POBoxDeliveryServiceTypeCode

</td>
<td valign="top">

 

</td>
<td valign="top">

BusinessPartner/AddressInformation/Address/PostalAddress/POBoxDeliveryServiceTypeCode

</td>
<td valign="top">

deliveryServiceType

</td>
<td valign="top">

BusinessPartner/addressData/personPostalAddress/alternative

</td>
</tr>
<tr>
<td valign="top">

**Script Variants - Person Address** 

</td>
<td valign="top">

AddressRepresentationCode

</td>
<td valign="top">

Version indicator of an address.

</td>
<td valign="top">

BusinessPartner/AddressInformation/Address/PostalAddress/AddressRepresentationCode

</td>
<td valign="top">

scriptCode

</td>
<td valign="top">

BusinessPartner/addressData/personPostalAddress/scriptVariants

</td>
</tr>
<tr>
<td valign="top">

**Organization Postal Address** 

</td>
<td valign="top">

RoomID

</td>
<td valign="top">

RoomID Room or Apartment Number.

</td>
<td valign="top">

BusinessPartner/AddressInformation/Address/PostalAddress/RoomID

</td>
<td valign="top">

door

</td>
<td valign="top">

BusinessPartner/addressData/organizationPostalAddress

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

CountryCode

</td>
<td valign="top">

Country Code.

</td>
<td valign="top">

BusinessPartner/AddressInformation/Address/PostalAddress/CountryCode

</td>
<td valign="top">

country

</td>
<td valign="top">

BusinessPartner/addressData/organizationPostalAddress

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

FirstLineName

</td>
<td valign="top">

Organisation Name Line 1. First name field for business partners in the Organization category.

</td>
<td valign="top">

BusinessPartner/AddressInformation/Address/OrganisationName/Name/FirstLineName

</td>
<td valign="top">

formattedOrgNameLine1

</td>
<td valign="top">

BusinessPartner/addressData/organizationPostalAddress

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

SecondLineName

</td>
<td valign="top">

Organisation Name Line 2. Second name field for business partners in the Organization category.

</td>
<td valign="top">

BusinessPartner/AddressInformation/Address/OrganisationName/Name/SecondLineName

</td>
<td valign="top">

formattedOrgNameLine2

</td>
<td valign="top">

BusinessPartner/addressData/organizationPostalAddress

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

ThirdLineName

</td>
<td valign="top">

Organization Name Line 3. Third name field for business partners in the Organization category.

</td>
<td valign="top">

BusinessPartner/AddressInformation/Address/OrganisationName/Name/ThirdLineName

</td>
<td valign="top">

formattedOrgNameLine3

</td>
<td valign="top">

BusinessPartner/addressData/organizationPostalAddress

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

FourthLineName

</td>
<td valign="top">

Organisation Name Line 4. Fourth name field for business partners in the Organization category.

</td>
<td valign="top">

BusinessPartner/AddressInformation/Address/OrganisationName/Name/FourthLineName

</td>
<td valign="top">

formattedOrgNameLine4

</td>
<td valign="top">

BusinessPartner/addressData/organizationPostalAddress

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

HouseID

</td>
<td valign="top">

House Number.

</td>
<td valign="top">

BusinessPartner/AddressInformation/Address/PostalAddress/HouseID

</td>
<td valign="top">

houseNumber

</td>
<td valign="top">

BusinessPartner/addressData/organizationPostalAddress

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

POBoxIDVisibleIndicator

</td>
<td valign="top">

 

</td>
<td valign="top">

BusinessPartner/AddressInformation/Address/PostalAddress/POBoxIDVisibleIndicator

</td>
<td valign="top">

postBoxIsWithoutNumber

</td>
<td valign="top">

BusinessPartner/addressData/organizationPostalAddress

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

StreetName

</td>
<td valign="top">

Street Address.

</td>
<td valign="top">

BusinessPartner/AddressInformation/Address/PostalAddress/StreetName

</td>
<td valign="top">

street

</td>
<td valign="top">

BusinessPartner/addressData/organizationPostalAddress

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

StreetSuffixName

</td>
<td valign="top">

Additional address text line for Street.

</td>
<td valign="top">

BusinessPartner/AddressInformation/Address/PostalAddress/StreetSuffixName

</td>
<td valign="top">

streetSuffix1

</td>
<td valign="top">

BusinessPartner/addressData/organizationPostalAddress

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

StreetPrefixName

</td>
<td valign="top">

Additional address text line for Street.

</td>
<td valign="top">

BusinessPartner/AddressInformation/Address/PostalAddress/StreetPrefixName

</td>
<td valign="top">

streetPrefix1

</td>
<td valign="top">

BusinessPartner/addressData/organizationPostalAddress

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

AdditionalStreetPrefixName

</td>
<td valign="top">

Additional address text line for Street.

</td>
<td valign="top">

BusinessPartner/AddressInformation/Address/PostalAddress/AdditionalStreetPrefixName

</td>
<td valign="top">

streetPrefix2

</td>
<td valign="top">

BusinessPartner/addressData/organizationPostalAddress

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

AdditionalStreetSuffixName

</td>
<td valign="top">

Additional address text line for Street.

</td>
<td valign="top">

BusinessPartner/AddressInformation/Address/PostalAddress/AdditionalStreetSuffixName

</td>
<td valign="top">

streetSuffix2

</td>
<td valign="top">

BusinessPartner/addressData/organizationPostalAddress

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

FloorID

</td>
<td valign="top">

Floor in building.

</td>
<td valign="top">

BusinessPartner/AddressInformation/Address/PostalAddress/FloorID

</td>
<td valign="top">

floor

</td>
<td valign="top">

BusinessPartner/addressData/organizationPostalAddress

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

CompanyPostalCode

</td>
<td valign="top">

This field is used for countries where major companies are assigned their own postal code by the national post office.

</td>
<td valign="top">

BusinessPartner/AddressInformation/Address/PostalAddress/CompanyPostalCode

</td>
<td valign="top">

companyPostalCode

</td>
<td valign="top">

BusinessPartner/addressData/organizationPostalAddress

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

RegionCode

</td>
<td valign="top">

Region Key. For example, Washington is a Region of USA, Karnataka is a region of India etc.

</td>
<td valign="top">

BusinessPartner/AddressInformation/Address/PostalAddress/RegionCode

</td>
<td valign="top">

primaryRegion

</td>
<td valign="top">

BusinessPartner/addressData/organizationPostalAddress

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

CountyName

</td>
<td valign="top">

 

</td>
<td valign="top">

BusinessPartner/AddressInformation/Address/PostalAddress/CountyName

</td>
<td valign="top">

secondaryRegion

</td>
<td valign="top">

BusinessPartner/addressData/organizationPostalAddress

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

CityName

</td>
<td valign="top">

 

</td>
<td valign="top">

BusinessPartner/AddressInformation/Address/PostalAddress/CityName

</td>
<td valign="top">

town

</td>
<td valign="top">

BusinessPartner/addressData/organizationPostalAddress

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

POBoxDeliveryServiceID

</td>
<td valign="top">

 

</td>
<td valign="top">

BusinessPartner/AddressInformation/Address/PostalAddress/POBoxDeliveryServiceID

</td>
<td valign="top">

deliveryServiceNumber

</td>
<td valign="top">

BusinessPartner/addressData/organizationPostalAddress

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

TimeZoneCode

</td>
<td valign="top">

Address Time Zone.

</td>
<td valign="top">

BusinessPartner/AddressInformation/Address/PostalAddress/TimeZoneCode

</td>
<td valign="top">

timeZone

</td>
<td valign="top">

BusinessPartner/addressData/organizationPostalAddress

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

AdditionalRegionalStructureCityCode

</td>
<td valign="top">

 

</td>
<td valign="top">

BusinessPartner/AddressInformation/Address/PostalAddress/AdditionalRegionalStructureCityCode

</td>
<td valign="top">

additionalCityName

</td>
<td valign="top">

BusinessPartner/addressData/organizationPostalAddress

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

CareOfName

</td>
<td valign="top">

c/o name; Part of the address \(c/o = care of\) if the recipient is different from the occupant and the names are not similar \(e.g. subtenants\).

</td>
<td valign="top">

BusinessPartner/AddressInformation/Address/PostalAddress/CareOfName

</td>
<td valign="top">

careOf

</td>
<td valign="top">

BusinessPartner/addressData/organizationPostalAddress

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

TransportationZoneID

</td>
<td valign="top">

Transportation zone to or from which the goods are delivered.

</td>
<td valign="top">

BusinessPartner/AddressInformation/Address/PostalAddress/TransportationZoneID

</td>
<td valign="top">

transportationZone

</td>
<td valign="top">

BusinessPartner/addressData/organizationPostalAddress

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

TaxJurisdictionCode

</td>
<td valign="top">

The tax jurisdiction code defines the tax authority to which taxes must be paid.

</td>
<td valign="top">

BusinessPartner/AddressInformation/Address/PostalAddress/TaxJurisdictionCode

</td>
<td valign="top">

taxJurisdiction

</td>
<td valign="top">

BusinessPartner/addressData/organizationPostalAddress

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

DistrictName

</td>
<td valign="top">

In some countries this entry is appended with a hyphen to the city name by the automatic address formatting. In other countries, it is output on a line of its own or \(for example, in the USA\) not printed.

</td>
<td valign="top">

BusinessPartner/AddressInformation/Address/PostalAddress/DistrictName

</td>
<td valign="top">

district

</td>
<td valign="top">

BusinessPartner/addressData/organizationPostalAddress

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

AdditionalHouseID

</td>
<td valign="top">

House number supplement.

</td>
<td valign="top">

BusinessPartner/AddressInformation/Address/PostalAddress/AdditionalHouseID

</td>
<td valign="top">

houseNumberSupplement

</td>
<td valign="top">

BusinessPartner/addressData/organizationPostalAddress

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

StreetPostalCode

</td>
<td valign="top">

If different postal codes are maintained for the PO Box and Street address of an address, this field contains the Street address postal code.

</td>
<td valign="top">

BusinessPartner/AddressInformation/Address/PostalAddress/StreetPostalCode

</td>
<td valign="top">

postCode

</td>
<td valign="top">

BusinessPartner/addressData/organizationPostalAddress

</td>
</tr>
<tr>
<td valign="top">

**Organization Address - Alternative** 

</td>
<td valign="top">

POBoxDeviatingCountryCode

</td>
<td valign="top">

PO Box Country.

</td>
<td valign="top">

BusinessPartner/AddressInformation/Address/PostalAddress/POBoxDeviatingCountryCode

</td>
<td valign="top">

country

</td>
<td valign="top">

BusinessPartner/addressData/personPostalAddress/alternative

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

POBoxDeviatingRegionCode

</td>
<td valign="top">

Region for PO Box \(Country, State, Province, etc.\),

</td>
<td valign="top">

BusinessPartner/AddressInformation/Address/PostalAddress/POBoxDeviatingRegionCode

</td>
<td valign="top">

primaryRegion

</td>
<td valign="top">

BusinessPartner/addressData/personPostalAddress/alternative

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

POBoxDeviatingCityName

</td>
<td valign="top">

PO Box city.

</td>
<td valign="top">

BusinessPartner/AddressInformation/Address/PostalAddress/POBoxDeviatingCityName

</td>
<td valign="top">

town

</td>
<td valign="top">

BusinessPartner/addressData/personPostalAddress/alternative

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

POBoxPostalCode

</td>
<td valign="top">

Postal code that is required for a unique assignment of the PO box; This field is used for countries where a different postal code applies to mail that is sent to the PO box rather than to the street address of a particular business partner.

</td>
<td valign="top">

BusinessPartner/AddressInformation/Address/PostalAddress/POBoxPostalCode

</td>
<td valign="top">

postCode

</td>
<td valign="top">

BusinessPartner/addressData/personPostalAddress/alternative

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

POBoxLobbyName

</td>
<td valign="top">

PO Box Lobby.

</td>
<td valign="top">

BusinessPartner/AddressInformation/Address/PostalAddress/POBoxLobbyName

</td>
<td valign="top">

deliveryServiceQualifier

</td>
<td valign="top">

BusinessPartner/addressData/personPostalAddress/alternative

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

POBoxDeliveryServiceTypeCode

</td>
<td valign="top">

 

</td>
<td valign="top">

BusinessPartner/AddressInformation/Address/PostalAddress/POBoxDeliveryServiceTypeCode

</td>
<td valign="top">

deliveryServiceType

</td>
<td valign="top">

BusinessPartner/addressData/personPostalAddress/alternative

</td>
</tr>
<tr>
<td valign="top">

**Script Variants - Organization Address** 

</td>
<td valign="top">

AddressRepresentationCode

</td>
<td valign="top">

Version indicator of an address.

</td>
<td valign="top">

BusinessPartner/AddressInformation/Address/PostalAddress/AddressRepresentationCode

</td>
<td valign="top">

scriptCode

</td>
<td valign="top">

BusinessPartner/addressData/personPostalAddress/scriptVariants

</td>
</tr>
</table>



<a name="loio8a9a1305ac764111b648e3303f24c784__businesspartnersuitebulkreplicaterequest---customer"/>

## BusinessPartnerSUITEBulkReplicateRequest - Customer

This service node contains the following parameters:



<a name="loio8a9a1305ac764111b648e3303f24c784__soap-and-odm-mapping-information-9"/>

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

**Customer Information** 

</td>
<td valign="top">

MaintenanceProfileCode

</td>
<td valign="top">

Customer Account Group. The account group is a classifying feature within customer master records. It determines number range of the customer account number, whether the number is assigned by the user or by the system and the necessary or possible specifications in the master record.

</td>
<td valign="top">

BusinessPartner/Customer/MaintenanceProfileCode

</td>
<td valign="top">

customerAccountGroup

</td>
<td valign="top">

BusinessPartner/customerInformation

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

CorporateGroupName

</td>
<td valign="top">

Relevant only for taxes/Group key. If the customer or the supplier belongs to a group, you can enter a group key here. The group key is freely assignable. If you create a matchcode using this group key, group evaluations are possible.

</td>
<td valign="top">

BusinessPartner/Customer/CorporateGroupName

</td>
<td valign="top">

customerCorporateGroup

</td>
<td valign="top">

BusinessPartner/customerInformation

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

DeletedIndicator

</td>
<td valign="top">

Central Deletion Flag for Master Record. Indicates that all data in this master record is to be deleted.

</td>
<td valign="top">

BusinessPartner/Customer/DeletedIndicator

</td>
<td valign="top">

isMarkedForDeletion

</td>
<td valign="top">

BusinessPartner/customerInformation

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

TaxGroupCode

</td>
<td valign="top">

Tax type. Classification of companies according to tax aspects.

</td>
<td valign="top">

BusinessPartner/Customer/TaxGroupCode

</td>
<td valign="top">

accountTaxType

</td>
<td valign="top">

BusinessPartner/customerInformation

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

OrderBlockingReasonCode

</td>
<td valign="top">

Order type block indicator \(for example, only cash sales\). Indicates if sales order processing is blocked for the customer in all sales areas.

</td>
<td valign="top">

BusinessPartner/Customer/SaleSalesAndDistributionBlocks/OrderBlockingReasonCode

</td>
<td valign="top">

orderBlockedReason

</td>
<td valign="top">

BusinessPartner/customerInformation

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

BillingBlockingReasonCode

</td>
<td valign="top">

Billing document type block \(for example, credit memos\). Indicates if the processing of billing documents is blocked for the customer in all sales areas.

</td>
<td valign="top">

BusinessPartner/Customer/SaleSalesAndDistributionBlocks/BillingBlockingReasonCode

</td>
<td valign="top">

billingBlockedReason

</td>
<td valign="top">

BusinessPartner/customerInformation

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

DeliveryBlockingReasonCode

</td>
<td valign="top">

Indicator: Delivery note block. Indicates if delivery processing is blocked for the customer in all sales areas.

</td>
<td valign="top">

BusinessPartner/Customer/SaleSalesAndDistributionBlocks/DeliveryBlockingReasonCode

</td>
<td valign="top">

deliveryBlockedReason

</td>
<td valign="top">

BusinessPartner/customerInformation

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

SalesSupportBlockedIndicator

</td>
<td valign="top">

Contact block \(Sales support\). Indicates if sales order processing is blocked for the customer in all sales areas \(company-wide, for example\).

</td>
<td valign="top">

BusinessPartner/Customer/SaleSalesAndDistributionBlocks/SalesSupportBlockedIndicator

</td>
<td valign="top">

salesBlockForCustomer

</td>
<td valign="top">

BusinessPartner/customerInformation

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

CustomerGroupCode

</td>
<td valign="top">

Customer classification. Specifies a classification of the customer \(for example, classifies the customer as a bulk purchaser\). The classifications are freely definable according to the needs of your organization.

</td>
<td valign="top">

BusinessPartner/Customer/MarketingAttributes/CustomerGroupCode

</td>
<td valign="top">

customerClassification

</td>
<td valign="top">

BusinessPartner/customerInformation

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

CustomerNielsenRegionCode

</td>
<td valign="top">

Nielsen ID. Specifies a regional division according to the market categories created by the A. C. Nielsen company. By allocating a Nielsen division, you can use the services of the Nielsen Institute to create a market analysis of your customers.

</td>
<td valign="top">

BusinessPartner/Customer/MarketingAttributes/CustomerNielsenRegionCode

</td>
<td valign="top">

nielsenRegion

</td>
<td valign="top">

BusinessPartner/customerInformation

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

IndustrialSectorCode

</td>
<td valign="top">

Industry Code 1.

</td>
<td valign="top">

BusinessPartner/Customer/IndustrySector/IndustrialSectorCode

</td>
<td valign="top">

industryCode1

</td>
<td valign="top">

BusinessPartner/customerInformation

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

FirstAdditionalIndustrialSectorCode

</td>
<td valign="top">

Industry Code 2.

</td>
<td valign="top">

BusinessPartner/Customer/IndustrySector/FirstAdditionalIndustrialSectorCode

</td>
<td valign="top">

industryCode2

</td>
<td valign="top">

BusinessPartner/customerInformation

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

SecondAdditionalIndustrialSectorCode

</td>
<td valign="top">

Industry Code 3.

</td>
<td valign="top">

BusinessPartner/Customer/IndustrySector/SecondAdditionalIndustrialSectorCode

</td>
<td valign="top">

industryCode3

</td>
<td valign="top">

BusinessPartner/customerInformation

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

ThirdAdditionalIndustrialSectorCode

</td>
<td valign="top">

Industry Code 4.

</td>
<td valign="top">

BusinessPartner/Customer/IndustrySector/ThirdAdditionalIndustrialSectorCode

</td>
<td valign="top">

industryCode4

</td>
<td valign="top">

BusinessPartner/customerInformation

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

FourthAdditionalIndustrialSectorCode

</td>
<td valign="top">

Industry Code 5.

</td>
<td valign="top">

BusinessPartner/Customer/IndustrySector/FourthAdditionalIndustrialSectorCode

</td>
<td valign="top">

industryCode5

</td>
<td valign="top">

BusinessPartner/customerInformation

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

EqualizationTaxRelevanceIndicator

</td>
<td valign="top">

Indicator to specify Business Partner Subject to Equalization Tax.

</td>
<td valign="top">

BusinessPartner/Customer/EqualizationTaxRelevanceIndicator

</td>
<td valign="top">

isEqualizationTaxSubject

</td>
<td valign="top">

BusinessPartner/customerInformation

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

AnnualSalesVolumeAmount

</td>
<td valign="top">

Indicator to specify Annual Sales.

</td>
<td valign="top">

BusinessPartner/Customer/MarketingAttributes/AnnualSalesVolumeAmount

</td>
<td valign="top">

plannedAnnualSalesAmount

</td>
<td valign="top">

BusinessPartner/customerInformation

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

currencyCode

</td>
<td valign="top">

Indicator to specify Currency of sales figure.

</td>
<td valign="top">

BusinessPartner/Customer/MarketingAttributes/AnnualSalesVolumeAmount/@currencyCode

</td>
<td valign="top">

plannedAnnualSalesCurrency

</td>
<td valign="top">

BusinessPartner/customerInformation

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

AnnualSalesVolumeAmountReportedYear

</td>
<td valign="top">

Indicator to specify Year For Which Sales are given.

</td>
<td valign="top">

BusinessPartner/Customer/MarketingAttributes/AnnualSalesVolumeAmountReportedYear

</td>
<td valign="top">

plannedAnnualSalesYear

</td>
<td valign="top">

BusinessPartner/customerInformation

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

ValueAddedTaxRelevanceIndicator

</td>
<td valign="top">

Indicator to specify Business Partner Liable for VAT.

</td>
<td valign="top">

BusinessPartner/Customer/ValueAddedTaxRelevanceIndicator

</td>
<td valign="top">

vatLiability

</td>
<td valign="top">

BusinessPartner/customerInformation

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

IndustryTypeName

</td>
<td valign="top">

Indicator to specify Industry Type.

</td>
<td valign="top">

BusinessPartner/Customer/IndustryTypeName

</td>
<td valign="top">

industryType

</td>
<td valign="top">

BusinessPartner/customerInformation

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

TradingPartnerCompanyID

</td>
<td valign="top">

Company ID of Trading Partner.

</td>
<td valign="top">

BusinessPartner/Customer/TradingPartnerCompanyID

</td>
<td valign="top">

customerTradingPartnerId

</td>
<td valign="top">

BusinessPartner/customerInformation

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

CFOPCategoryCode

</td>
<td valign="top">

Indicator to specify CFOP category of Customer.

</td>
<td valign="top">

BusinessPartner/Customer/CFOPCategoryCode

</td>
<td valign="top">

cfopCategory

</td>
<td valign="top">

BusinessPartner/customerInformation

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

FiscalYearVariantCode

</td>
<td valign="top">

Fiscal Year Variant.

</td>
<td valign="top">

BusinessPartner/Customer/MarketingAttributes/FiscalYearVariantCode

</td>
<td valign="top">

fiscalYearVariant

</td>
<td valign="top">

BusinessPartner/customerInformation

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

CustomerConditionGroupCode

</td>
<td valign="top">

Indicator to specify Customer condition group 1.

</td>
<td valign="top">

BusinessPartner/Customer/PriceSpecifications/CustomerConditionGroupCode

</td>
<td valign="top">

customerConditionGroup1

</td>
<td valign="top">

BusinessPartner/customerInformation

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

FirstAdditionalCustomerConditionGroupCode

</td>
<td valign="top">

Indicator to specify Customer condition group 2.

</td>
<td valign="top">

BusinessPartner/Customer/PriceSpecifications/FirstAdditionalCustomerConditionGroupCode

</td>
<td valign="top">

customerConditionGroup2

</td>
<td valign="top">

BusinessPartner/customerInformation

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

SecondAdditionalCustomerConditionGroupCode

</td>
<td valign="top">

Indicator to specify Customer condition group 3.

</td>
<td valign="top">

BusinessPartner/Customer/PriceSpecifications/SecondAdditionalCustomerConditionGroupCode

</td>
<td valign="top">

customerConditionGroup3

</td>
<td valign="top">

BusinessPartner/customerInformation

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

ThirdAdditionalCustomerConditionGroupCode

</td>
<td valign="top">

Indicator to specify Customer condition group 4.

</td>
<td valign="top">

BusinessPartner/Customer/PriceSpecifications/ThirdAdditionalCustomerConditionGroupCode

</td>
<td valign="top">

customerConditionGroup4

</td>
<td valign="top">

BusinessPartner/customerInformation

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

FourthAdditionalCustomerConditionGroupCode

</td>
<td valign="top">

Indicator to specify Customer condition group 5.

</td>
<td valign="top">

BusinessPartner/Customer/PriceSpecifications/FourthAdditionalCustomerConditionGroupCode

</td>
<td valign="top">

customerConditionGroup5

</td>
<td valign="top">

BusinessPartner/customerInformation

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

CustomerPartyWithFiscalAddressInternalID

</td>
<td valign="top">

Indicator to specify Account number of the master record with the fiscal address.

</td>
<td valign="top">

BusinessPartner/Customer/CustomerPartyWithFiscalAddressInternalID

</td>
<td valign="top">

fiscalAddress

</td>
<td valign="top">

BusinessPartner/customerInformation

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

ExpressTrainStationLocationName

</td>
<td valign="top">

Indicator to specify Express train station.

</td>
<td valign="top">

BusinessPartner/Customer/ExpressTrainStationLocationName

</td>
<td valign="top">

expressTrainStationName

</td>
<td valign="top">

BusinessPartner/customerInformation

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

DataMediumExchangeInstructionCode

</td>
<td valign="top">

Indicator to specify Instruction key for data medium exchange.

</td>
<td valign="top">

BusinessPartner/Customer/DataMediumExchangeInstructionCode

</td>
<td valign="top">

dataExchangeInstruction

</td>
<td valign="top">

BusinessPartner/customerInformation

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

AlternativePayeeAllowedIndicator

</td>
<td valign="top">

Indicator to specify is an alternative payer allowed in document.

</td>
<td valign="top">

BusinessPartner/Customer/AlternativePayeeAllowedIndicator

</td>
<td valign="top">

alternativePayerIsAllowed

</td>
<td valign="top">

BusinessPartner/customerInformation

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

CustomerExtensionCode

</td>
<td valign="top">

Indicator to specify Customer Extension Code 1.

</td>
<td valign="top">

BusinessPartner/Customer/CustomerExtensionCode

</td>
<td valign="top">

customerExtensionCode01

</td>
<td valign="top">

BusinessPartner/customerInformation

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

FirstAdditionalCustomerExtensionCode

</td>
<td valign="top">

Indicator to specify Customer Extension Code 2.

</td>
<td valign="top">

BusinessPartner/Customer/FirstAdditionalCustomerExtensionCode,

</td>
<td valign="top">

customerExtensionCode02

</td>
<td valign="top">

BusinessPartner/customerInformation

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

SecondAdditionalCustomerExtensionCode

</td>
<td valign="top">

Indicator to specify Customer Extension Code 3.

</td>
<td valign="top">

BusinessPartner/Customer/SecondAdditionalCustomerExtensionCode

</td>
<td valign="top">

customerExtensionCode03

</td>
<td valign="top">

BusinessPartner/customerInformation

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

ThirdAdditionalCustomerExtensionCode

</td>
<td valign="top">

Indicator to specify Customer Extension Code 4.

</td>
<td valign="top">

BusinessPartner/Customer/ThirdAdditionalCustomerExtensionCode

</td>
<td valign="top">

customerExtensionCode04

</td>
<td valign="top">

BusinessPartner/customerInformation

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

FourthAdditionalCustomerExtensionCode

</td>
<td valign="top">

Indicator to specify Customer Extension Code 5.

</td>
<td valign="top">

BusinessPartner/Customer/FourthAdditionalCustomerExtensionCode

</td>
<td valign="top">

customerExtensionCode05

</td>
<td valign="top">

BusinessPartner/customerInformation

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

FifthAdditionalCustomerExtensionCode

</td>
<td valign="top">

Indicator to specify Customer Extension Code 6.

</td>
<td valign="top">

BusinessPartner/Customer/FifthAdditionalCustomerExtensionCode

</td>
<td valign="top">

customerExtensionCode06

</td>
<td valign="top">

BusinessPartner/customerInformation

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

SixthAdditionalCustomerExtensionCode

</td>
<td valign="top">

Indicator to specify Customer Extension Code 7.

</td>
<td valign="top">

BusinessPartner/Customer/SixthAdditionalCustomerExtensionCode

</td>
<td valign="top">

customerExtensionCode07

</td>
<td valign="top">

BusinessPartner/customerInformation

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

SeventhAdditionalCustomerExtensionCode

</td>
<td valign="top">

Indicator to specify Customer Extension Code 8.

</td>
<td valign="top">

BusinessPartner/Customer/SeventhAdditionalCustomerExtensionCode

</td>
<td valign="top">

customerExtensionCode08

</td>
<td valign="top">

BusinessPartner/customerInformation

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

EighthAdditionalCustomerExtensionCode

</td>
<td valign="top">

Indicator to specify Customer Extension Code 9.

</td>
<td valign="top">

BusinessPartner/Customer/EighthAdditionalCustomerExtensionCode

</td>
<td valign="top">

customerExtensionCode09

</td>
<td valign="top">

BusinessPartner/customerInformation

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

NinthAdditionalCustomerExtensionCode

</td>
<td valign="top">

Indicator to specify Customer Extension Code 10.

</td>
<td valign="top">

BusinessPartner/Customer/NinthAdditionalCustomerExtensionCode

</td>
<td valign="top">

customerExtensionCode10

</td>
<td valign="top">

BusinessPartner/customerInformation

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

BusinessTypeName

</td>
<td valign="top">

Indicator to specify Business Type.

</td>
<td valign="top">

BusinessPartner/Customer/BusinessTypeName

</td>
<td valign="top">

businessType

</td>
<td valign="top">

BusinessPartner/customerInformation

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

RepresentativeName

</td>
<td valign="top">

Indicator to specify Representative Name.

</td>
<td valign="top">

BusinessPartner/Customer/RepresentativeName

</td>
<td valign="top">

representativeName

</td>
<td valign="top">

BusinessPartner/customerInformation

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

PostingBlockedIndicator

</td>
<td valign="top">

Central posting block.

</td>
<td valign="top">

BusinessPartner/Customer/PostingBlockedIndicator

</td>
<td valign="top">

postingIsBlocked

</td>
<td valign="top">

BusinessPartner/customerInformation

</td>
</tr>
<tr>
<td valign="top">

**SalesArrangement** 

</td>
<td valign="top">

TransferLocationName

</td>
<td valign="top">

Additional information for the primary Incoterm.

</td>
<td valign="top">

BusinessPartner/Customer/SalesArrangement/DeliveryTerms/Incoterms/TransferLocationName

</td>
<td valign="top">

incotermsTransferLocationName

</td>
<td valign="top">

BusinessPartner/customerInformation/salesArrangements

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

SalesOrderCompleteDeliveryIndicator

</td>
<td valign="top">

Indicates whether a sales order must be delivered completely in a single delivery or whether the order can be partially delivered and completed over a number of deliveries.

</td>
<td valign="top">

BusinessPartner/Customer/SalesArrangement/DeliveryTerms/SalesOrderCompleteDeliveryIndicator

</td>
<td valign="top">

completeDeliveryIsDefined

</td>
<td valign="top">

BusinessPartner/customerInformation/salesArrangements

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

PartialDeliveryControlCode

</td>
<td valign="top">

Specifies whether the customer requires full or partial delivery for the item.

</td>
<td valign="top">

BusinessPartner/Customer/SalesArrangement/DeliveryTerms/PartialDeliveryControlCode

</td>
<td valign="top">

partialDelivery

</td>
<td valign="top">

BusinessPartner/customerInformation/salesArrangements

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

ClassificationCode

</td>
<td valign="top">

Commonly used trading terms that comply with the standards established by the International Chamber of Commerce \(ICC\).

</td>
<td valign="top">

BusinessPartner/Customer/SalesArrangement/DeliveryTerms/Incoterms/ClassificationCode

</td>
<td valign="top">

incotermsClassification

</td>
<td valign="top">

BusinessPartner/customerInformation/salesArrangements

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

OrderBlockingReasonCode

</td>
<td valign="top">

Customer order block \(sales area\). Indicates if further sales order processing is blocked for the customer. The block applies throughout the specified sales area.

</td>
<td valign="top">

BusinessPartner/Customer/SalesArrangement/OrderBlockingReasonCode

</td>
<td valign="top">

orderBlockedReason

</td>
<td valign="top">

BusinessPartner/customerInformation/salesArrangements

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

GroupCode

</td>
<td valign="top">

Customer group. Identifies a particular group of customers \(for example, wholesale or retail\) for the purpose of pricing or generating statistics.

</td>
<td valign="top">

BusinessPartner/Customer/SalesArrangement/GroupCode

</td>
<td valign="top">

salesArrangementGroup

</td>
<td valign="top">

BusinessPartner/customerInformation/salesArrangements

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

PriceGroupCode

</td>
<td valign="top">

Price group \(customer\). A grouping of customers who share the same pricing requirements. You can define price groups according to the needs of your organization and create pricing records for each group. You can, for example, define a group of customers to whom you want to give the same kind of discount. You can assign a price group to an individual customer either in the customer master record or in the sales document.

</td>
<td valign="top">

BusinessPartner/Customer/SalesArrangement/PriceGroupCode

</td>
<td valign="top">

salesArrangementPriceGroup

</td>
<td valign="top">

BusinessPartner/customerInformation/salesArrangements

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

DeliveryBlockingReasonCode

</td>
<td valign="top">

Customer delivery block \(sales area\). Indicates if further delivery processing is blocked for the customer. The block applies throughout the specified sales area. If you enter a blocking indicator, delivery processing that is already underway is continued. However, no new processing can take place.

</td>
<td valign="top">

BusinessPartner/Customer/SalesArrangement/DeliveryBlockingReasonCode

</td>
<td valign="top">

deliveryBlockedReason

</td>
<td valign="top">

BusinessPartner/customerInformation/salesArrangements

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

BillingBlockingReasonCode

</td>
<td valign="top">

Billing block for customer \(sales and distribution\). Indicates if further billing activities are blocked for the customer. The block applies throughout the specified sales area.

</td>
<td valign="top">

BusinessPartner/Customer/SalesArrangement/BillingBlockingReasonCode

</td>
<td valign="top">

billingBlockedReason

</td>
<td valign="top">

BusinessPartner/customerInformation/salesArrangements

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

CurrencyCode

</td>
<td valign="top">

Currency. Customer's currency for a sales area. This currency will be used to settle the customer's charges for the given sales organization.

</td>
<td valign="top">

BusinessPartner/Customer/SalesArrangement/CurrencyCode

</td>
<td valign="top">

currency

</td>
<td valign="top">

BusinessPartner/customerInformation/salesArrangements

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

SalesGroupCode

</td>
<td valign="top">

Sales group. A group of sales people who are responsible for processing sales of certain products or services. By using sales groups you can designate different areas of responsibility within a sales office. When you generate sales statistics, you can use the sales group as one of the selection criteria.

</td>
<td valign="top">

BusinessPartner/Customer/SalesArrangement/SalesGroupCode

</td>
<td valign="top">

salesGroupDisplayId

</td>
<td valign="top">

BusinessPartner/customerInformation/salesArrangements

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

SalesOfficeCode

</td>
<td valign="top">

Sales office. A physical location \(for example, a branch office\) that has responsibility for the sale of certain products or services within a given geographical area.

</td>
<td valign="top">

BusinessPartner/Customer/SalesArrangement/SalesOfficeCode

</td>
<td valign="top">

salesOfficeDisplayId

</td>
<td valign="top">

BusinessPartner/customerInformation/salesArrangements

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

SalesSupportBlockedIndicator

</td>
<td valign="top">

Sales block for customer \(sales area\).

</td>
<td valign="top">

BusinessPartner/Customer/SalesArrangement/SalesSupportBlockedIndicator

</td>
<td valign="top">

salesBlockForCustomer

</td>
<td valign="top">

BusinessPartner/customerInformation/salesArrangements

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

CashDiscountTermsCode

</td>
<td valign="top">

Key for defining payment terms composed of cash discount percentages and payment periods.

</td>
<td valign="top">

BusinessPartner/Customer/SalesArrangement/CashDiscountTermsCode

</td>
<td valign="top">

paymentTermCode

</td>
<td valign="top">

BusinessPartner/customerInformation/salesArrangements

</td>
</tr>
<tr>
<td valign="top">

**Sales Area Reference** 

</td>
<td valign="top">

DivisionCode

</td>
<td valign="top">

Division. A way of grouping materials, products, or services. The system uses divisions to determine the sales areas and the business areas for a material, product, or service.

</td>
<td valign="top">

BusinessPartner/Customer/SalesArrangement/DivisionCode

</td>
<td valign="top">

division

</td>
<td valign="top">

BusinessPartner/customerInformation/salesArrangements/salesAreaRef

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

SalesOrganisationID

</td>
<td valign="top">

Sales Organization. An organizational unit responsible for the sale of certain products or services. The responsibility of a sales organization may include legal liability for products and customer claims.

</td>
<td valign="top">

BusinessPartner/Customer/SalesArrangement/SalesOrganisationID

</td>
<td valign="top">

salesOrganizationDisplayId

</td>
<td valign="top">

BusinessPartner/customerInformation/salesArrangements/salesAreaRef

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

DistributionChannelCode

</td>
<td valign="top">

Distribution Channel.The way in which products or services reach the customer. Typical examples of distribution channels are wholesale, retail, or direct sales.

</td>
<td valign="top">

BusinessPartner/Customer/SalesArrangement/DistributionChannelCode

</td>
<td valign="top">

distributionChannel

</td>
<td valign="top">

BusinessPartner/customerInformation/salesArrangements/salesAreaRef

</td>
</tr>
<tr>
<td valign="top">

**PartnerFunctions** 

</td>
<td valign="top">

PartyRoleCode

</td>
<td valign="top">

Partner Function. The abbreviated form of the name that identifies the partner function. The same is determined based on the Customer / Supplier Account Group. Also, if the outbound is SenderHANA, the same will be filled and sent. If some third party is having their specific outbound implementation, they should fill it and explicitly send it.

</td>
<td valign="top">

BusinessPartner/Customer/SalesArrangement/PartnerFunctions/PartyRoleCode

</td>
<td valign="top">

functionCode

</td>
<td valign="top">

BusinessPartner/customerInformation/salesArrangements/functions

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

PartyInternalID

</td>
<td valign="top">

Identifier of the corresponding partner based on PartnerType.

</td>
<td valign="top">

BusinessPartner/Customer/SalesArrangement/PartnerFunctions/PartyInternalID

</td>
<td valign="top">

partnerNumber

</td>
<td valign="top">

BusinessPartner/customerInformation/salesArrangements/functions

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

PartnerType

</td>
<td valign="top">

Type of partner for Ex: Customer, Supplier or Personnel.

</td>
<td valign="top">

BusinessPartner/Customer/SalesArrangement/PartnerFunctions/PartnerType

</td>
<td valign="top">

functionPartnerType

</td>
<td valign="top">

BusinessPartner/customerInformation/salesArrangements/functions

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

DefaultIndicator

</td>
<td valign="top">

Default Partner. Specifies a partner as the default for a particular partner function. When you enter more than one partner for a particular partner function \(for example, you define three different ship-to parties\), you can select one partner as the default. During sales or purchasing processing, if you have defined multiple partners for a partner function, the system prompts you to choose just one partner. The system presents the default partner as the first choice in the pop-up window.

</td>
<td valign="top">

BusinessPartner/Customer/SalesArrangement/PartnerFunctions/DefaultIndicator

</td>
<td valign="top">

isDefault

</td>
<td valign="top">

BusinessPartner/customerInformation/salesArrangements/functions

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

PartnerDescription

</td>
<td valign="top">

Customer description of partner \(plant, storage location\).

</td>
<td valign="top">

BusinessPartner/Customer/SalesArrangement/PartnerFunctions/PartnerDescription

</td>
<td valign="top">

partnerDescription

</td>
<td valign="top">

BusinessPartner/customerInformation/salesArrangements/functions

</td>
</tr>
<tr>
<td valign="top">

**TaxClassification** 

</td>
<td valign="top">

TaxCountryCode

</td>
<td valign="top">

Departure country \(country from which the goods are sent\). Identifies the country in which the delivery originates. You can define the country key in a table. As a rule, it is a good idea to use the existing international standards for identifying vehicles from different countries \(for example: USA = United States, I = Italy, and so on\). The system uses the key to \(1\) help determine the relevant taxes during pricing, \(2\) determine important country-specific standards \(the length of postal codes and bank account numbers, for example\).

</td>
<td valign="top">

BusinessPartner/Customer/TaxClassification/TaxCountryCode

</td>
<td valign="top">

country

</td>
<td valign="top">

BusinessPartner/customerInformation/taxClassifications

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

TaxTypeCode

</td>
<td valign="top">

Tax category \(sales tax, federal sales tax,...\). Identifies the condition that the system uses to automatically determine country-specific taxes during pricing. You can define one or more tax categories for each country. During sales order processing, the system applies the tax category according to \(1\) the geographical location of your delivering plant and the location of the customer receiving the goods. \(2\) tax classifications in the customer master record and the material master record.

</td>
<td valign="top">

BusinessPartner/Customer/TaxClassification/TaxTypeCode

</td>
<td valign="top">

taxCategory

</td>
<td valign="top">

BusinessPartner/customerInformation/taxClassifications

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

TaxGroupCode

</td>
<td valign="top">

Specifies the tax liability of the customer, based on the tax structure of the customers' country.

</td>
<td valign="top">

BusinessPartner/Customer/TaxClassification/TaxGroupCode

</td>
<td valign="top">

taxClassification

</td>
<td valign="top">

BusinessPartner/customerInformation/taxClassifications

</td>
</tr>
</table>



<a name="loio8a9a1305ac764111b648e3303f24c784__businesspartnersuitebulkreplicaterequest---supplier"/>

## BusinessPartnerSUITEBulkReplicateRequest - Supplier

This service node contains the following parameters:



<a name="loio8a9a1305ac764111b648e3303f24c784__soap-and-odm-mapping-information-10"/>

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

**Supplier Information** 

</td>
<td valign="top">

TaxGroupCode

</td>
<td valign="top">

Fiscal Type. Classification of companies according to tax aspects.

</td>
<td valign="top">

BusinessPartner/Supplier/TaxGroupCode

</td>
<td valign="top">

responsibleType

</td>
<td valign="top">

BusinessPartner/supplierInformation

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

PostingBlockedIndicator

</td>
<td valign="top">

Yes/No field/Central posting block. Indicates that the account is blocked for posting for all company codes.

</td>
<td valign="top">

BusinessPartner/Supplier/PostingBlockedIndicator

</td>
<td valign="top">

isPostingBlocked

</td>
<td valign="top">

BusinessPartner/supplierInformation

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

PurchasingBlockedIndicator

</td>
<td valign="top">

Yes/No field / Centrally imposed purchasing block.Indicates whether or not the supplier master record is blocked for all departments \(that is, whether or not posting to this record is allowed at all\).

</td>
<td valign="top">

BusinessPartner/Supplier/PurchasingTerms/PurchasingBlockedIndicator

</td>
<td valign="top">

isPurchasingBlocked

</td>
<td valign="top">

BusinessPartner/supplierInformation

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

ValueAddedTaxRelevanceIndicator

</td>
<td valign="top">

Yes/No field / Liable for VAT. Determines whether the company is liable to value-added tax \(VAT\).

</td>
<td valign="top">

BusinessPartner/Supplier/ValueAddedTaxRelevanceIndicator

</td>
<td valign="top">

vatLiability

</td>
<td valign="top">

BusinessPartner/supplierInformation

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

DeletedIndicator

</td>
<td valign="top">

Yes/No field / Central Deletion Flag for Master Record. Indicates that all data in this master record is to be deleted.

</td>
<td valign="top">

BusinessPartner/Supplier/DeletedIndicator

</td>
<td valign="top">

deletionIndicator

</td>
<td valign="top">

BusinessPartner/supplierInformation

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

RelatedCustomerInternalID

</td>
<td valign="top">

Gives an alphanumeric key, which clearly identifies the customer or supplier in the SAP system.

</td>
<td valign="top">

BusinessPartner/Supplier/RelatedCustomerInternalID

</td>
<td valign="top">

customerId

</td>
<td valign="top">

BusinessPartner/supplierInformation

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

AlternativePayeePartyInternalID

</td>
<td valign="top">

The account number of the supplier with whom automatic payment transactions are carried out.

</td>
<td valign="top">

BusinessPartner/Supplier/AlternativePayeePartyInternalID

</td>
<td valign="top">

alternativePayees

</td>
<td valign="top">

BusinessPartner/supplierInformation/alternativePayees

</td>
</tr>
<tr>
<td valign="top">

**Purchasing Arrangements** 

</td>
<td valign="top">

TransferLocationName

</td>
<td valign="top">

Additional information for the primary Incoterm.

</td>
<td valign="top">

BusinessPartner/Supplier/ProcurementArrangement/PurchasingTerms/Incoterms/TransferLocationName

</td>
<td valign="top">

incotermsTransferLocationName

</td>
<td valign="top">

BusinessPartner/supplierInformation/purchasingArrangements

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

DeletedIndicator

</td>
<td valign="top">

Yes/No field / Central Deletion Flag for Master Record. Indicates whether or not the supplier master record is marked for deletion.

</td>
<td valign="top">

BusinessPartner/Supplier/ProcurementArrangement/DeletedIndicator

</td>
<td valign="top">

isMarkedForDeletion

</td>
<td valign="top">

BusinessPartner/supplierInformation/purchasingArrangements

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

PurchasingBlockedIndicator

</td>
<td valign="top">

Yes/No field/Centrally imposed purchasing block. Indicates whether or not the supplier master record is blocked for the purchasing organization for posting purposes.

</td>
<td valign="top">

BusinessPartner/Supplier/ProcurementArrangement/PurchasingTerms/PurchasingBlockedIndicator

</td>
<td valign="top">

isPurchasingBlocked

</td>
<td valign="top">

BusinessPartner/supplierInformation/purchasingArrangements

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

ClassificationCode

</td>
<td valign="top">

Commonly used trading terms that comply with the standards established by the International Chamber of Commerce \(ICC\).

</td>
<td valign="top">

BusinessPartner/Supplier/ProcurementArrangement/PurchasingTerms/Incoterms/ClassificationCode

</td>
<td valign="top">

incotermsClassification

</td>
<td valign="top">

BusinessPartner/supplierInformation/purchasingArrangements

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

PurchaseOrderCurrencyCode

</td>
<td valign="top">

Purchase order currency: Key for the currency on which an order placed with a supplier is based.

</td>
<td valign="top">

BusinessPartner/Supplier/ProcurementArrangement/PurchasingTerms/PurchaseOrderCurrencyCode

</td>
<td valign="top">

currency

</td>
<td valign="top">

BusinessPartner/supplierInformation/purchasingArrangements

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

SupplierABCClassificationCode

</td>
<td valign="top">

ABC indicator: Means of classifying suppliers according to their significance to your company.

</td>
<td valign="top">

BusinessPartner/Supplier/ProcurementArrangement/SupplierABCClassificationCode

</td>
<td valign="top">

classification

</td>
<td valign="top">

BusinessPartner/supplierInformation/purchasingArrangements

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

PriceSpecificationSupplierGroupCode

</td>
<td valign="top">

Group for Calculation Schema \(Supplier\): Determines which calculation schema \(pricing procedure\) is to be used in purchasing documents containing this supplier number.

</td>
<td valign="top">

BusinessPartner/Supplier/ProcurementArrangement/PurchasingTerms/PriceSpecificationSupplierGroupCode

</td>
<td valign="top">

calculationSchema

</td>
<td valign="top">

BusinessPartner/supplierInformation/purchasingArrangements

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

PurchasingOrganisationID

</td>
<td valign="top">

Denotes the purchasing organization.

</td>
<td valign="top">

BusinessPartner/Supplier/ProcurementArrangement/PurchasingOrganisationID

</td>
<td valign="top">

purchasingOrganizationDisplayId

</td>
<td valign="top">

BusinessPartner/supplierInformation/purchasingArrangements

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

PurchasingGroupID

</td>
<td valign="top">

Purchasing Group: Key for a buyer or a group of buyers, who are responsible for certain purchasing activities.

</td>
<td valign="top">

BusinessPartner/Supplier/ProcurementArrangement/PurchasingGroupID

</td>
<td valign="top">

purchasingGroupDisplayId

</td>
<td valign="top">

BusinessPartner/supplierInformation/purchasingArrangements

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

AutomaticPurchaseOrderGenerationAllowedIndicator

</td>
<td valign="top">

Automatic Generation of Purchase Order Allowed.

</td>
<td valign="top">

BusinessPartner/Supplier/ProcurementArrangement/PurchasingTerms/AutomaticPurchaseOrderGenerationAllowedIndicator

</td>
<td valign="top">

isAutoGenerationOfPurchaseOrdersAllowed

</td>
<td valign="top">

BusinessPartner/supplierInformation/purchasingArrangements

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

CashDiscountTermsCode

</td>
<td valign="top">

Key for defining payment terms composed of cash discount percentages and payment periods.

</td>
<td valign="top">

BusinessPartner/Supplier/ProcurementArrangement/PurchasingTerms/CashDiscountTermsCode

</td>
<td valign="top">

paymentTermCode

</td>
<td valign="top">

BusinessPartner/supplierInformation/purchasingArrangements

</td>
</tr>
<tr>
<td valign="top">

**Accounting Information** 

</td>
<td valign="top">

PaymentBlockCode

</td>
<td valign="top">

Block key for payment. Block key \(enqueue key\) that is used to block an open item or an account to payment transactions. You can use the block key as described below. • **Automatic Payment Transactions** In automatic payment transactions, the block takes effect when it is entered in the system as follows:◦In the master record. ◦ **In the document** If you enter the block in the master record then all open items for this account are contained in the exception list.The following block keys have a special meaning in the master record: ◦The block key \* has the effect that all items of the account are skipped in automatic payment transactions. ◦The block key + has the effect that all items are skipped in which a payment method was not entered explicitly. ◦The block key A is always set automatically when a down payment is entered. Therefore, you must not delete the block key A or use it for other purposes. Whether a block key can be set or removed in payment proposal processing depends on the attribute Changeable in payment proposal of the block key. • **Manual Payments** ◦ Manual payments are only affected by a block key in the document if you set the attribute Blocked for manual payments in the block key. ◦ A block key that was set in the master record does not have any effect on manual payments. You can have the system issue a warning message in that case. To do so, you have to make system settings. Set up message 671 of work area F5 in message control accordingly.• **Release for Payment** If you want to use a block key for payment release in accounting, then you have to set the attribute Not Changeable for the block key.

</td>
<td valign="top">

BusinessPartner/Supplier/AccountingInformation/PaymentBlockCode

</td>
<td valign="top">

paymentBlockingReason

</td>
<td valign="top">

BusinessPartner/supplierInformation/accountingInformation

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

SortCode

</td>
<td valign="top">

Selection key for allocation number layout. Indicates the layout rule for the Allocation field in the document line item.

</td>
<td valign="top">

BusinessPartner/Supplier/AccountingInformation/SortCode

</td>
<td valign="top">

invoiceSortingOrder

</td>
<td valign="top">

BusinessPartner/supplierInformation/accountingInformation

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

PlanningGroupCode

</td>
<td valign="top">

Cash management and forecast group \(risk group\).Planning group. In cash management, customers and suppliers are allocated to planning groups by means of an entry made in the master record.

</td>
<td valign="top">

BusinessPartner/Supplier/AccountingInformation/PlanningGroupCode

</td>
<td valign="top">

cashPlanningGroup

</td>
<td valign="top">

BusinessPartner/supplierInformation/accountingInformation

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

MinorityIndicatorsCode

</td>
<td valign="top">

Minority indicators.

</td>
<td valign="top">

BusinessPartner/Supplier/AccountingInformation/MinorityIndicatorsCode

</td>
<td valign="top">

minorityGroup

</td>
<td valign="top">

BusinessPartner/supplierInformation/accountingInformation

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

DeletedIndicator

</td>
<td valign="top">

Deletion Indicator for Supplier at Purchasing Level. Indicates that the company code data in this master record is to be deleted.

</td>
<td valign="top">

BusinessPartner/Supplier/AccountingInformation/DeletedIndicator

</td>
<td valign="top">

isMarkedForDeletion

</td>
<td valign="top">

BusinessPartner/supplierInformation/accountingInformation

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

BlockedIndicator

</td>
<td valign="top">

Yes/No field / Posting block for company code. Indicates that the account is blocked for posting in the specified company code.

</td>
<td valign="top">

BusinessPartner/Supplier/AccountingInformation/BlockedIndicator

</td>
<td valign="top">

isPostingBlocked

</td>
<td valign="top">

BusinessPartner/supplierInformation/accountingInformation

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

HouseBankInternalID

</td>
<td valign="top">

Short key for a house bank. All bank data is determined using this key.

</td>
<td valign="top">

BusinessPartner/Supplier/AccountingInformation/HouseBankInternalID

</td>
<td valign="top">

houseBank

</td>
<td valign="top">

BusinessPartner/supplierInformation/accountingInformation

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

CompanyID

</td>
<td valign="top">

Company Code. The company code is an organizational unit within financial accounting.

</td>
<td valign="top">

BusinessPartner/Supplier/AccountingInformation/CompanyID

</td>
<td valign="top">

companyCodeDisplayId

</td>
<td valign="top">

BusinessPartner/supplierInformation/accountingInformation

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

GeneralLedgerAccountReference

</td>
<td valign="top">

G/L account number. The reconciliation account in G/L accounting is the account which is updated parallel to the subledger account for normal postings \(for example, invoice or payment\). For special postings \(for example, down payment or bill of exchange\), this account is replaced by another account \(for example, 'down payments received' instead of 'receivables'\). The replacement takes place due to the special G/L indicator which you must specify for these types of postings.

</td>
<td valign="top">

BusinessPartner/Supplier/AccountingInformation/GeneralLedgerAccountReference/ID

</td>
<td valign="top">

reconciliationAccountNumber

</td>
<td valign="top">

BusinessPartner/supplierInformation/accountingInformation

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

DoubleEntriesCheckIndicator

</td>
<td valign="top">

Yes/No field. When incoming invoices are entered or when memos are entered in Financial Accounting \(FI\), the system checks whether an invoice or credit memo has already been entered for the same date.

</td>
<td valign="top">

BusinessPartner/Supplier/AccountingInformation/DoubleEntriesCheckIndicator

</td>
<td valign="top">

isDoubleInvoice

</td>
<td valign="top">

BusinessPartner/supplierInformation/accountingInformation

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

EmployeeResponsiblePartyWebAddress

</td>
<td valign="top">

Correspondence / Internet address of partner company clerk.

</td>
<td valign="top">

BusinessPartner/Supplier/AccountingInformation/EmployeeResponsiblePartyWebAddress

</td>
<td valign="top">

accountingClerkInternetAddress

</td>
<td valign="top">

BusinessPartner/supplierInformation/accountingInformation

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

CashDiscountTermsCode

</td>
<td valign="top">

Terms of Payment Key: Key for defining payment terms composed of cash discount percentages and payment periods.

</td>
<td valign="top">

BusinessPartner/Supplier/AccountingInformation/CashDiscountTermsCode

</td>
<td valign="top">

paymentTermCode

</td>
<td valign="top">

BusinessPartner/supplierInformation/accountingInformation

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

AccountingClerkInitialsCode

</td>
<td valign="top">

The name of the accounting clerk defined by this identification code can be used in the payment program for correspondence and reporting \(for example, open item lists\).

</td>
<td valign="top">

BusinessPartner/Supplier/AccountingInformation/AccountingClerkInitialsCode

</td>
<td valign="top">

accountingClerkInitials

</td>
<td valign="top">

supplierInformation/accountingInformation/accountingClerkInitials

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

AlternativePayeePartyInternalID

</td>
<td valign="top">

The account number of the supplier with whom automatic payment transactions are to be carried out.

</td>
<td valign="top">

BusinessPartner/Supplier/AccountingInformation/AlternativePayeePartyInternalID

</td>
<td valign="top">

alternativePayees

</td>
<td valign="top">

supplierInformation/accountingInformation/alternativePayees

</td>
</tr>
<tr>
<td valign="top">

**WithholdingTaxes** 

</td>
<td valign="top">

VendorRecipientTypeCode

</td>
<td valign="top">

The type of recipient can be defined in the vendor master record.

</td>
<td valign="top">

BusinessPartner/Supplier/AccountingInformation/WithholdingTax/VendorRecipientTypeCode

</td>
<td valign="top">

recipientType

</td>
<td valign="top">

BusinessPartner/supplierInformation/withholdingTaxes

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

WithholdingTaxExemptionCertificateID

</td>
<td valign="top">

Exemption Certificate Number: Numbered assigned by the relevant authorities for exemption from withholding tax.

</td>
<td valign="top">

BusinessPartner/Supplier/AccountingInformation/WithholdingTax/WithholdingTaxExemptionCertificateID

</td>
<td valign="top">

taxNumber

</td>
<td valign="top">

BusinessPartner/supplierInformation/withholdingTaxes

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

WithholdingTaxCode

</td>
<td valign="top">

Withholding Tax Code: One or more "withholding tax codes" are assigned to each withholding tax type. One of the things these codes determine is the various percentage rates for the withholding tax type.

</td>
<td valign="top">

BusinessPartner/Supplier/AccountingInformation/WithholdingTax/WithholdingTaxCode

</td>
<td valign="top">

subType

</td>
<td valign="top">

BusinessPartner/supplierInformation/withholdingTaxes

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

WithholdingTaxTypeCode

</td>
<td valign="top">

Indicator for Withholding Tax Type: This indicator is used to classify the different types of withholding tax.

</td>
<td valign="top">

BusinessPartner/Supplier/AccountingInformation/WithholdingTax/WithholdingTaxTypeCode

</td>
<td valign="top">

type

</td>
<td valign="top">

BusinessPartner/supplierInformation/withholdingTaxes

</td>
</tr>
<tr>
<td valign="top">

**Exemption** 

</td>
<td valign="top">

WithholdingTaxExemptionReasonCode

</td>
<td valign="top">

Reason for Exemption: Indicator used to classify different types of exemption from liability to a particular withholding tax.These indicators can be defined per withholding tax type in the supplier master record.

</td>
<td valign="top">

BusinessPartner/Supplier/AccountingInformation/WithholdingTax/WithholdingTaxExemptionReasonCode

</td>
<td valign="top">

reason

</td>
<td valign="top">

BusinessPartner/supplierInformation/exemption

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

WithholdingTaxExemptionCertificateID

</td>
<td valign="top">

Exemption Certificate Number: Numbered assigned by the relevant authorities for exemption from withholding tax.

</td>
<td valign="top">

BusinessPartner/Supplier/AccountingInformation/WithholdingTax/WithholdingTaxExemptionCertificateID

</td>
<td valign="top">

certificateNumber

</td>
<td valign="top">

BusinessPartner/supplierInformation/exemption

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

WithholdingTaxExemptionRate

</td>
<td valign="top">

Exemption Rate: Rate of exemption from withholding tax.Those persons/activities subject to withholding tax can be exempted from withholding tax up to the percentage rate you enter here. This exemption rate refers to the withholding tax amount itself and not to the whole amount liable to withholding tax \(withholding tax base amount\).

</td>
<td valign="top">

BusinessPartner/Supplier/AccountingInformation/WithholdingTax/WithholdingTaxExemptionRate

</td>
<td valign="top">

percentage

</td>
<td valign="top">

BusinessPartner/supplierInformation/exemption

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

StartDate

</td>
<td valign="top">

Date from which withholding tax exemption applies.

</td>
<td valign="top">

BusinessPartner/Supplier/AccountingInformation/WithholdingTax/WithholdingTaxExemptionValidityPeriod/StartDate

</td>
<td valign="top">

validFrom

</td>
<td valign="top">

BusinessPartner/supplierInformation/exemption

</td>
</tr>
<tr>
<td valign="top">

 

</td>
<td valign="top">

EndDate

</td>
<td valign="top">

Date on which withholding tax exemption expires.

</td>
<td valign="top">

BusinessPartner/Supplier/AccountingInformation/WithholdingTax/WithholdingTaxExemptionValidityPeriod/EndDate

</td>
<td valign="top">

validTo

</td>
<td valign="top">

BusinessPartner/supplierInformation/exemption

</td>
</tr>
</table>

