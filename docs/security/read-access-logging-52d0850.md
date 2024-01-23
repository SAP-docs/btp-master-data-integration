<!-- loio52d08503ba944f61841a25584e446fee -->

# Read Access Logging

Read access logging records have access to sensitive personal data. Currently it is done on Data Protection and Privacy annotations in the SAP One Domain Model. SAP Master Data Integration supports read access logging configuration by using following annotations:

For more information, refer to the Read-Access Logging section in the SAP Business Technology Platform page: **[SAP Business Technology Platform](https://help.sap.com/viewer/product/CP/Cloud/en-US?task=operate_task) \> Security \> Data Protection and Privacy \> Change Logging and Read-Access Logging**.

-   `@AuditLog.Operation: {Read: true, Insert: true, Update: true, Delete: true}` : Read property is used to enable/disable read-access logging. If the annotation is not present, then by default Master Data Integration performs read-access logging.

-   `@PersonalData.FieldSemantics: 'DataSubjectID'` `DataSubjectID` `DataSubjectID` : If this annotation is present, the annotated attribute's value is used asin the log entry. If there are multiple attributes annotated, all of them need to be included. However, theis only included in the log entry if the annotated attribute's value is not filtered out from the message sent to the client. If the annotation is not present, instance id is used.

-   `@PersonalData.IsPotentiallySensitive` : The annotated attribute's name is used as attribute in the log entry to represent potentially sensitive personal data. If there is no attribute annotated with this annotation, no read access log entry is written.


> ### Note:  
> Read access logging is done only when attributes representing sensitive personal data are exposed to downstream system.

