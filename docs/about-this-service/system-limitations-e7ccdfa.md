<!-- loioe7ccdfa51ed3492bb8fb5adb7f97384b -->

# System Limitations



<a name="loioe7ccdfa51ed3492bb8fb5adb7f97384b__size-of-change-requests"/>

## Size of Change Requests

**Limit:** 256 kB

The size of change requests is limited to 256 KB.

As an exception, the size of change requests for the master data type `sap.odm.businesspartner.BusinessPartner` is limited to 512 KB instead.

If the size of a change request exceeds this limit, the change request gets rejected.



<a name="loioe7ccdfa51ed3492bb8fb5adb7f97384b__size-of-batches-of-change-requests"/>

## Size of Batches of Change Requests

**Limit:** 256 kB

The size of a batch of change requests is limited to 256 KB.

As an exception, the size of a batch of change requests for the master data type `sap.odm.businesspartner.BusinessPartner` is limited to 512 KB instead.

If the size of a batch of change request exceeds this limit, the batch of change requests gets rejected.



<a name="loioe7ccdfa51ed3492bb8fb5adb7f97384b__size-of-master-data-records"/>

## Size of Master Data Records

**Limit:** 512 kB

The size of a master data record is limited to 512 KB.

This limit is separate from the limit for the size of a change request because with patches, multiple smaller change requests could be used to construct a bigger record.

If processing of a change request leads to a size of a master data record that exceeds this limit, the change request gets rejected.



<a name="loioe7ccdfa51ed3492bb8fb5adb7f97384b__change-tokens"/>

## Change Tokens

**Limit:** 36 characters

The size of a change token is limited to 36 characters.

The allowed characters are:

-   Lower-case letters `a` to `z` 

-   Upper-case letters `A` to `Z` 

-   Digits `0` to `9` 

-   Dash `-` 

-   Underscore `_` 


Change tokens are chosen by clients and need to be unique per change request and client.

If a change request contains a change token that contains invalid characters or exceeds this limit, the change request gets rejected.



<a name="loioe7ccdfa51ed3492bb8fb5adb7f97384b__validity-of-delta-tokens"/>

## Validity of Delta Tokens

**Limit:** 28 days

Delta tokens expire after 28 days.

Clients that did not synchronize for 28 days will get an error response indicating that the delta token is outdated. Those clients have to perform an initial load.



<a name="loioe7ccdfa51ed3492bb8fb5adb7f97384b__size-of-soap-payload"/>

## Size of SOAP payload

**Limit:** 10 MB

The size of incoming SOAP requests is limited to 10 megabytes.



<a name="loioe7ccdfa51ed3492bb8fb5adb7f97384b__soap-distribution-of-business-partners"/>

## SOAP distribution of Business Partners

**Limit \#1:** Operators for data filtering

SOAP distribution supports `equals` and `not equals` operators only for filtering data.

**Limit \#2:** Once distributed always distributed

SOAP based distribution follows the `once distributed always distributed` logic. This means if any object instance\(Business Partner\) is distributed to a destination based on a model, then any changes to the object instance or changes to the maintained filter criteria of that model will not have any impact in future distribution of the object instance.

