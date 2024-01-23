<!-- loioadbf8efbda2e4514b7f2776a9eb879c7 -->

# Integrating with SAP S/4HANA \(On-Premise\)

SAP S/4HANA provides integrations to SAP Master Data Integration for the following objects:

Refer to the [Central Integration Chapter](https://help.sap.com/docs/SAP_S4HANA_ON-PREMISE/d761beaeedd949c18213f449f4617250/34ee350171bf41bb8d015f8061a5a918.html) on SAP S/4HANA help page, to learn more about the capabilities of SAP S/4HANA for replicating master data using the SAP Master Data Integration service.

*Limitations* :

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


-   A single SAP S/4HANA system cannot be connected to multiple SAP Master Data Integration tenants




<a name="loioadbf8efbda2e4514b7f2776a9eb879c7__business-partner"/>

## Business Partner

To perform the necessary configuration to connect an SAP S/4HANA on-premise system with an SAP Master Data Integration tenant, follow the PDF guide mentioned in [SAP Note-3065614](https://launchpad.support.sap.com/#/notes/3065614) .



<a name="loioadbf8efbda2e4514b7f2776a9eb879c7__data-replication-framework-customizing"/>

## Data Replication Framework Customizing

In the S/4HANA or MDG system, the Data Replication Framework is used to invoke the SAP Master Data Integration — Business Partners SOAP services. Follow the steps below:

1.  `drfimg` **Data Replication** **Define Custom Settings for Data Replication** **Define Technical Settings** **Define Technical Settings for Business Systems** Run transactionand define technical settings for business system under\>\>\>.

    1.  **New Entries** Chooseto define a new business system and to maintain the logical system for the receiving systems.

    2.  **business system value** Enter a. This value will be used to identify your SAP Master Data Integration tenant. Recommendations:

        -   Use the subdomain name for both business system value and ConfigurationValue. The subdomain name can be found in the subaccount overview in SAP BTP Cockpit.

        -   The **business system value** and the **ConfigurationValue** defined in [Configuring Business System](../initial-setup-and-administration/configuring-own-business-system-id-75d55b7.md) should always be same.


    3.  **Define Bus. Systems, BOs** **New Entries** **986** Select the business system maintained in above step and choose. Next, selectand addfor Business Partner inlcuding Relationships and save the entry.

    4.  **Define Bus. Systems, BOs, Communication Channel** **New Entries** **Replication via Services** **C. Channel** Select the entry created in above step and choose. Next, selectand addunder. Save the entry.

    5.  **1376** Repeat steps 3 to 5 above to maintain entry asfor Key Mapping \(if the integration scenario requires key mapping replication\)


2.  `drfimg` **Data Replication** **Define Custom Settings for Data Replication** **Define Replication Models** Run transactionand define replication model \(replication of business partner\) under\>\>.

    1.  **New Entries** Choose, create a new replication model, and enter a description.

    2.  **Assign Outbound Implementation** Select the row, and choose.

    3.  **New Entries** Create a new entry by choosingand enter the following values using the input help:

        -   Outbound Implementation: 986\_3 Outbound Impl. for BP/REL via Services


    4.  **Assign Target Systems for Repl. Model /Outb.Impl** Select the row and choose.

    5.  Create a new entry and enter the business system name for the receiving system created previously.

    6.  **Assign Outbound Parameter** Select the row and choose.

    7.  Create a new entry, enter the following values, and save.

        -   Outbound Parameter: PACK\_SIZE\_BULK

        -   Outbound Parameter Value: Enter the required value \(for example, 100\)


    8.  **Log Days** Return to the Define Replication Model view. Optionally, you can also add an expiration time for the log in thecolumn.

    9.  **Activate** Select the newly created replication model and choose.

    10. **1376** Repeat steps 3 to 9 to maintain outbound implementation for Key Mapping as\(if the integration scenario requires key mapping replication\).



