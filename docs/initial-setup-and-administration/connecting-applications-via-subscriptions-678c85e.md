<!-- loio678c85e0643a4ddba3c4fb62e0fdd952 -->

# Connecting Applications via Subscriptions

SAP Master Data Integration can also be used as a dependency of an SAP BTP application.

An SAP BTP application may rely on the SAP BTP tenant subscription mechanism to automatically create and connect a tenant of SAP Master Data Integration with itself.If a tenant subscribes to an SAP BTP application that has a dependency on SAP Master Data Integration, a corresponding subscription to SAP Master Data Integration will be created and maintained along with the SAP BTP application subscription.

This means that the connection and authentication between SAP Master Data Integration and the SAP BTP application is maintained automatically and no connectivity setup is required.

Nevertheless, it might be necessary to perform additional configuration steps.Please consult the documentation of the respective SAP BTP application for further details.

