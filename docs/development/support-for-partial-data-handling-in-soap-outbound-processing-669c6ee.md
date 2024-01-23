<!-- loio669c6eee90b74f3986c4ac9ae9fe02fe -->

# Support for Partial Data Handling in SOAP Outbound Processing



<a name="loio669c6eee90b74f3986c4ac9ae9fe02fe__overview"/>

## Overview

The partial data handling feature ensures that there is no data loss for the following scenarios when SOAP outbound is sent to the connected business system \(SAP S/4HANA or SAP MDG\):

-   SAP Master Data Integration service message contains limited set of entities. For example, bank / payment card entities are not supported on the service yet and no information on these entities is sent in the outbound message. The data for these entities are not overwritten.

-   The service message contains limited set of attributes for a given entity. For example, outbound messages for business partner node / entity does not contain death date field. For the entities where reduced data model scope handling is supported on the connected business system, this attribute’s data are not overwritten.

-   The service message does not contain all the instances of the entity. For example, in case new industries are added on connected system which are not replicated to the service, there is no data loss when replication happens to the connected system from Master Data Integration. You should maintain exclude / include filters on your connected system correctly for this to work.

-   The service does not support all roles. The data corresponding to a role which is not supported on the service is not present in the outbound message. If the role is properly maintained in the exclude filter on connected system, data corresponding to this role is not overwritten when replication happens to the connected system.


For more details about include / exclude filters, refer to the following documentation: [help.sap.com](https://help.sap.com/viewer/index) [**SAP S/4HANA \> Cross Components \> Data Replication Framework \> Define Filter Criteria** ](https://help.sap.com/viewer/8308e6d301d54584a33cd04a9861bc52/1809.000/en-US/bfc3b321489348a2892ec9e1eb357084.html) .



<a name="loio669c6eee90b74f3986c4ac9ae9fe02fe__more-information"/>

## More Information

For more details on reduced data model scope handling, refer to the following SAP notes:

-   [SAP Note 2659038](http://help.sap.com/disclaimer?site=https://launchpad.support.sap.com/#/notes/2659038) 

-   [SAP Note 2733112](http://help.sap.com/disclaimer?site=https://launchpad.support.sap.com/#/notes/2733112) 

-   [SAP Note 3087667](http://help.sap.com/disclaimer?site=https://launchpad.support.sap.com/#/notes/3087667) 

-   [DRF Configuration](https://help.sap.com/viewer/c7713d6177ad479d9ea00958db9f2f81/CLOUD/en-US/5877c7670348479889c3a756bfd87e90.html) 


