<!-- loioadbf8efbda2e4514b7f2776a9eb879c7 -->

# Integrating with SAP S/4HANA \(On-Premise\)

SAP S/4HANA provides integrations to SAP Master Data Integration service for the following objects:

-   Bank

-   Budget Period

-   Business Partner

-   Business Partner Relationship

-   Cost Center

-   Exchange Rate

-   Functional Area

-   Fund

-   Funds Center

-   Grant

-   Product

-   Product Group

-   Project Controlling Object

-   Sales Controlling Object

-   Workforce Person


Refer to the [Central Integration Chapter](https://help.sap.com/docs/SAP_S4HANA_ON-PREMISE/d761beaeedd949c18213f449f4617250/34ee350171bf41bb8d015f8061a5a918.html) on SAP S/4HANA help page, to learn more about the capabilities of SAP S/4HANA for replicating master data using the SAP Master Data Integration service.

*Limitations* : A single SAP S/4HANA system cannot be connected to multiple SAP Master Data Integration tenants.



<a name="loioadbf8efbda2e4514b7f2776a9eb879c7__business-partner"/>

## Business Partner

To perform the necessary configuration to connect an SAP S/4HANA on-premise system with an SAP Master Data Integration tenant, follow the PDF guide mentioned in [SAP Note-3065614](https://launchpad.support.sap.com/#/notes/3065614) .



<a name="loioadbf8efbda2e4514b7f2776a9eb879c7__data-replication-framework-customizing"/>

## Data Replication Framework Customizing

In the S/4HANA or MDG system, the Data Replication Framework is used to invoke the SAP Master Data Integration — Business Partners SOAP services. Follow the steps below:

1.  Run transaction `drfimg` and define technical settings for business system under **Data Replication** \> **Define Custom Settings for Data Replication** \> **Define Technical Settings** \> **Define Technical Settings for Business Systems** .

    1.  Choose **New Entries** to define a new business system and to maintain the logical system for the receiving systems.

    2.  Enter a **business system value** . This value will be used to identify your SAP Master Data Integration tenant. Recommendations:

        -   Use the subdomain name for both business system value and **ConfigurationValue** . The subdomain name can be found in the subaccount overview in SAP BTP Cockpit.

        -   The **business system value** and the **ConfigurationValue** defined in [Configuring Business System](../initial-setup-and-administration/configuring-own-business-system-id-75d55b7.md) should always be the same.


    3.  Select the business system maintained in the above step and choose **Define Bus. Systems, BOs** . Next, select **New Entries** and add **986** for Business Partner including Relationships and save the entry.

    4.  Select the entry created in the above step and choose **Define Bus. Systems, BOs, Communication Channel** . Next, select **New Entries** and add **Replication via Services** under **C. Channel** . Save the entry.

    5.  If the integration scenario requires key mapping replication, repeat steps 3 to 5 above to maintain entry as **1376** for Key Mapping.


2.  Run transaction `drfimg` and define replication model \(replication of business partner\) under **Data Replication** \> **Define Custom Settings for Data Replication** \> **Define Replication Models** .

    1.  Choose **New Entries** , create a new replication model, and enter a description.

    2.  Select the row, and choose **Assign Outbound Implementation** .

    3.  Create a new entry by choosing **New Entries** , and enter the following values using the input help:

        -   Outbound Implementation: 986\_3 Outbound Impl. for BP/REL via Services


    4.  Select the row and choose **Assign Target Systems for Repl. Model /Outb.Impl** .

    5.  Create a new entry and enter the business system name for the receiving system created previously.

    6.  Select the row and choose **Assign Outbound Parameter** .

    7.  Create a new entry, enter the following values, and save.

        -   Outbound Parameter: PACK\_SIZE\_BULK

        -   Outbound Parameter Value: Enter the required value \(for example, 100\)


    8.  Return to the Define Replication Model view. Optionally, you can also add an expiration time for the log in the **Log Days** column.

    9.  Select the newly created replication model and choose **Activate** .

    10. Repeat steps 3 to 9 to maintain an outbound implementation for Key Mapping as **1376** \(if the integration scenario requires key mapping replication\).



