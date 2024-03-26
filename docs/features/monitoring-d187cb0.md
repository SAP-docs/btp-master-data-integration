<!-- loiod187cb03f2dc4c3aba5a5393d22f5210 -->

# Monitoring

Monitoring in SAP Master Data Orchestration offers an end-to-end monitoring of the distribution of master data. It visualizes the distribution process of the master data objects throughout the landscape via SAP Master Data Integration service. The distribution processes are configured by distribution models. The distribution model describes per connection\(combination of provider and consumer\), which master data objects are distributed and contains parameters controlling the distribution. Monitoring supports the administrator and the business user to check the correctness of the distribution setup, to observe the distribution of object changes and to resolve distribution errors.

You can have different views on the distribution statuses:

-   **Landscape-wise** : In "Monitor Master Data Distribution", the clients and their connections are displayed with a graph. The coloring represents the status\(failed, warning, success\), the size and width the number of distributed objects.

-   **Connection-wise** : In "Display Distribution Status", the status is displayed as per connection between clients. The app lists the individual object distribution status. They can be filtered by status. The detail of the distribution status shows warning or error messages\(if any\) as provided by the responsible application.

-   **Object-wise** : In "Locate Object", you get the distribution status of a single master data object displayed. You get the information regarding the involved systems and individual distribution status there.




<a name="loiod187cb03f2dc4c3aba5a5393d22f5210__architecture-of-monitoring"/>

## Architecture of Monitoring

Any client sending or receiving master data objects reports the processing of the message as SAP Passport Event to SAP Cloud ALM. These events also contain logging information regarding the objects contained in the message and their individual processing status.

The central monitoring platform for monitoring the integration of SAP products is SAP Cloud ALM, mainly with the application "Integration & Exception Monitoring". You can configure business services there representing the configured connections between the clients. In this context, SAP Cloud ALM also supports a correlation of the SAP Passport Events by the logging information between provider and consumer.

The logging information regarding the distributed master data is also used by SAP Master Data Orchestration. SAP Master Data Orchestration will import every five minutes the logging information from SAP Cloud ALM and aggregate it to the distribution status.

SAP Cloud ALM offers a message oriented and technical point of view to the distribution process, while SAP Master Data Orchestration has a master data object oriented and distribution model-driven point of view.

Refer to [SOAP monitoring events](list-of-soap-events-5fd5903.md) for more details on SOAP events and to [REST monitoring events](list-of-rest-events-422e8f6.md) for more details on REST events that are sent to SAP Cloud ALM.



<a name="loiod187cb03f2dc4c3aba5a5393d22f5210__steps-to-configure-monitoring"/>

## Steps to Configure Monitoring

1.  You must subscribe to SAP Cloud ALM, which may result in additional costs depending on the amount of buffered data.

2.  You must register any client participating at the master data replication to SAP Cloud ALM to enable, that the SAP Passport Events are accepted by it. In addition, also the replication of the SAP Passport Events to SAP Cloud ALM must be set up individually per client. SAP Master Data Orchestration must be registered with “Configure Monitoring” in the same way. This step also registers implicitly Master Data Integration and enables the replication of the SAP Passport Events to SAP Cloud ALM.

3.  You must configure a mapping between the service instances used in Master Data Integration\(defined in the Business Cloud Cockpit\) to the services known in SAP Cloud ALM. This enables SAP Master Data Orchestration to read and identify the logging information from SAP Cloud ALM.




<a name="loiod187cb03f2dc4c3aba5a5393d22f5210__alerting"/>

## Alerting

Altering, that is, informing administrators in case of warnings or errors, is a functionality of SAP Cloud ALM and the “Integration & Exception Monitoring”.



<a name="loiod187cb03f2dc4c3aba5a5393d22f5210__error-resolution"/>

## Error Resolution

If the reason of a distribution error is solved, the monitors of SAP Master Data Orchestration can be used to retrigger the distribution of the failed master data objects.



<a name="loiod187cb03f2dc4c3aba5a5393d22f5210__recommendation"/>

## Recommendation

Don't disable or filter in SAP Cloud ALM the SAP Passport Events regarding master data replication. If the collection of the events is filtered, a comprehensive monitoring would not be possible anymore as events are missed.



<a name="loiod187cb03f2dc4c3aba5a5393d22f5210__restrictions"/>

## Restrictions

The monitoring in SAP Master Data Orchestration focus on the distribution process. Changes of business-related status of the master data objects are not reflected in this monitoring.

Currently SAP Master Data Orchestration only offers the connection-centric view with “Display Distribution Status”.

