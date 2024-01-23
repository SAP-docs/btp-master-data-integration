<!-- loioff2fc4ddd74a4b049948e711ca74aa20 -->

# Read Access Logging via SAP Audit Log Service

SAP Master Data Integration service integrates with SAP Audit Log service. Read access logging is performed for every access to data that is potentially sensitive personal data. The read access logging feature uses SAP Audit Log.

The identification of personal data is done based on annotations in the SAP One Domain Model. Master Data Integration supports read access logging configuration by using below-mentioned annotations:

-   `@AuditLog.Operation: {Read: <read>, Insert: <insert>, Update: <update>, Delete: <delete>}` :

    Read-access logging is disabled if `<read>` is `false`. If the annotation is not present, then by default Master Data Integration will perform read-access logging.

-   `@PersonalData.FieldSemantics: 'DataSubjectID'` :

    If this annotation is present, the value of the annotated attribute should be used as data subject ID in the audit log entry. If there are multiple attributes annotated, all of them should be included.


-   `@PersonalData.IsPotentiallySensitive` :

    The name of the annotated attribute should be used as an attribute in the log entry to represent potentially sensitive personal data. If there is no attribute annotated with this annotation, no read access log entry will be written.


> ### Caution:  
> The data subject ID is only included in the audit log entry if the value of annotated attribute is not filtered out from the message sent to the client. If the annotation is not present, instance ID will be used.

> ### Note:  
> Read access logging is triggered only, when attributes, representing sensitive personal data, are in fact exposed to downstream systems.

