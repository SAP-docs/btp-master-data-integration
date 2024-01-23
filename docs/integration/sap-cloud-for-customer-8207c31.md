<!-- loio8207c31b665a4f39b7dfa621c2fb80fe -->

# SAP Cloud for Customer

Refer to [SAP Cloud for Customer documentation](https://help.sap.com/docs/SAP_CLOUD_FOR_CUSTOMER/f7cae081face472dacb159c51be473e7/6dc7a90e297a419e8ce47f2bb8a6b93c.html) to learn more about the configurations required to replicate business partner master data using the SAP Master Data Integration service.

The types of master data that can be replicated between SAP Cloud for Customer and SAP Master Data Integration include, for example, the following:

-   Business Partner: Follow the steps in Determination and Business Configuration to perform necessary configurations on partner determination data.




<a name="loio8207c31b665a4f39b7dfa621c2fb80fe__business-partner"/>

## Business Partner



<a name="loio8207c31b665a4f39b7dfa621c2fb80fe__determination-and-business-configuration"/>

## Determination and Business Configuration

Business Partner determination logic for customer master is required in SAP Master Data Integration service to address the following scenario gap:

In SAP S/4HANA, reflexive partner functions can be mandatory in the sales area part of the Business Partner: Customer.

However, SAP Cloud for Customer does not support reflexive partner functions. These functions are implicitly assigned to every business partner with sales area data.

Reflexive partner functions, these are, partner functions for which business partner can be assigned to itself are listed below:

Thus, when a business partner is replicated from SAP Cloud for Customer to SAP S/4HANA, below error can occur:

`Mandatory partner function xx is missing for sales area` .

In order to address this gap, Master Data Integration provides a feature to upload of partner determination logic.

This feature allows you to upload configurations at one go. You need to download configuration data from the back-office system, fill the template, and upload using the REST endpoint in the excel format.

Partner determination configurations need to be downloaded from the back-office system and uploaded to SAP Master Data Integration - Business Partners to validate incoming master data via SOAP channel.

In the back-office system, you should define the rules according to which automatic partner determination is to be carried out. According to the rules defined, the partners are adopted from the customer master records of the sold-to parties to the sales and distribution documents.

-   Sold to party

-   Ship to Party

-   Bill to party

-   Payer




<a name="loio8207c31b665a4f39b7dfa621c2fb80fe__configurations-to-be-uploaded"/>

## Configurations to Be Uploaded

Following are the configurations that should be uploaded:

1.  **Customer partner determination procedures** : List of all partner determinations

2.  **Customer partner functions in procedure** : Partner functions in each procedure, defining the mandatory ones as well

3.  **Customer partner determination procedure assignment** : Partner determination to account group assignment

4.  **Customer partner functions** : Partner functions to partner type assignment, also defining unique constraint

5.  **Customer account group partner function assignment** : Partner function to account group assignment

6.  **Customer partner function assignment** : Language-dependent keys for partner functions




<a name="loio8207c31b665a4f39b7dfa621c2fb80fe__prepare-data-for-upload"/>

## Prepare Data for Upload

**Prerequisite:** Save the excel file template from the [SAP Note](https://launchpad.support.sap.com/#/notes/2987243). This template contains sheets for each of the views required for Partner Function Determination and Business Configurations.

> ### Note:  
> Delete the sheets from the excel file that you don’t want to use. If an empty excel sheet is uploaded then existing data could be deleted.

Follow the steps below for SAP S/4HANA Cloud and On-premise systems to prepare the data for upload:

-   **Configuration in SAP S/4HANA On-premise****** : Download the existing data from ABAP system and add them to the respective sheet names in the MS Excel template. For more information on the **Template for Business Configurations and Business Partner Determination**, refer to excel attached in the [SAP Note 2987243](http://help.sap.com/disclaimer?site=https://launchpad.support.sap.com/#/notes/2987243).


For more information, refer to [Partner Determination in Sales and Distribution](https://help.sap.com/viewer/7b24a64d9d0941bda1afa753263d9e39/2021.000/en-US/0271bd534f22b44ce10000000a174cb4.html) .

-   **Configuration in SAP S/4HANA Cloud** : Follow the steps to extract customer partner function related configuration from SAP S/4HANA Cloud system and upload it in a SAP Cloud Platform tenant that is subscribed to the service.


> ### Note:  
> Your user in SAP S/4HANA Cloud should have access to**Manage your Solution** fiori application.

a. Open the **Manage your Solution** tile in the S/4HANA Cloud system.

b. Click on **Configure your Solution**.

c. Search for SSCUI **101286**. Click on **Configure**.

For more information on SSCUIs, refer to [Configuring Your Solution](https://help.sap.com/viewer/082b48bfe4dd4e37b4032ed3d8fdec8d/2202.500/en-US/427d9605efa54a7cb8d89abf0a9b4b02.html).

d. Copy the values from the below Partner Determination Views and add them to the respective sheet names in the MS Excel template. For more information on the **Template for Business Configurations and Business Partner Determination**, refer to excel attached in the [SAP Note 2987243](http://help.sap.com/disclaimer?site=https://launchpad.support.sap.com/#/notes/2987243).


<table>
<tr>
<th valign="top">

View Name

</th>
<th valign="top">

Sheet Name in Template

</th>
</tr>
<tr>
<td valign="top">

Partner Determination Procedures \(Cust\)

</td>
<td valign="top">

CUST\_PartnerDetermineProcedure

</td>
</tr>
<tr>
<td valign="top">

Partner Functions in Procedure

</td>
<td valign="top">

CUST\_DeterminProcedure\_Function

</td>
</tr>
<tr>
<td valign="top">

Partner Determination Procedure Assignment \(Cust\)

</td>
<td valign="top">

CUST\_DetermineProcedure\_AccGrp

</td>
</tr>
<tr>
<td valign="top">

Partner Functions

</td>
<td valign="top">

CUST\_PartnerFunction

</td>
</tr>
<tr>
<td valign="top">

Account Groups - Function Assignment

</td>
<td valign="top">

CUST\_PartnerFunction\_AccGrp

</td>
</tr>
<tr>
<td valign="top">

Partner Function Conversion

</td>
<td valign="top">

CUST\_PartnerFunctionText

</td>
</tr>
</table>



<a name="loio8207c31b665a4f39b7dfa621c2fb80fe__steps-to-upload-configuration-data"/>

## Steps to Upload Configuration Data

> ### Note:  
> Use a REST client.

> ### Restriction:  
> The following API can be used only by Business Users. For more information, refer to [Authentication in Master Data Integration](../initial-setup-and-administration/authentication-of-business-users-ef53987.md).

> ### Note:  
> You need to insert the appropriate region to indicate in which data center the configuration is done. You can find the base URI from the **Service Key** of your subaccount.
> 
> Examples:
> 
> `https://one-mds.cfapps.eu10.hana.ondemand.com` `https://one- mds.cfapps.eu10.hana.ondemand.com/businesspartner/v0/configuration/ConfigurationUpload` For,, the region is EU10. Therefore, the complete URL is
> 
> `https://one-mds.cfapps.us10.hana.ondemand.com` `https://one-mds.cfapps.us10.hana.ondemand.com/businesspartner/v0/configuration/ConfigurationUpload` For,, the region is US10. Therefore, the complete URL is

1.  **URL** `https://one-mds.cfapps.{region}.hana.ondemand.com/businesspartner/v0/configuration/ConfigurationUpload` :

    This a **POST** request


1.  **Authentication**: Please refer to [Authentication in MDI](../initial-setup-and-administration/authentication-of-business-users-ef53987.md) to request for the right authentication.

2.  For this POST request, follow the below instructions for the request body:

    a. Select **form-data** as the data type for the request body

    b. Next, add a name-value or key-value pair with name or key as **file** and for value browse to select the file that you prepared.

3.  Choose **Send** to upload the data.




<a name="loio8207c31b665a4f39b7dfa621c2fb80fe__steps-to-download-configuration-data"/>

## Steps to Download Configuration Data

> ### Note:  
> Use a REST client.

> ### Restriction:  
> The following API can be used only by Business Users. For more information, refer to [Authentication in Master Data Integration](../initial-setup-and-administration/authentication-of-business-users-ef53987.md) .

> ### Note:  
> **Service Key** You need to insert the appropriate region to indicate in which data center the configuration is done. You can find the base URI from theof your subaccount.
> 
> Examples:
> 
> `https://one-mds.cfapps.eu10.hana.ondemand.com` `https://one-mds.cfapps.eu10.hana.ondemand.com/businesspartner/v0/configuration/configurationDownload/all` For, the region is EU10. Therefore, the complete URL is
> 
> `https://one-mds.cfapps.us10.hana.ondemand.com` `https://one-mds.cfapps.us10.hana.ondemand.com/businesspartner/v0/configuration/configurationDownload/all` For, the region is US10. Therefore, the complete URL is

1.  **URL** `https://one-mds.cfapps.{region}.hana.ondemand.com/businesspartner/v0/configuration/configurationDownload/all` :


1.  **Authentication**: Please refer to [Authentication in MDI](../initial-setup-and-administration/authentication-of-business-users-ef53987.md) to request for the right authentication.

2.  Execute the request.

3.  Download the data. You can download the data for six configuration tables listed below:


    <table>
    <tr>
    <th valign="top">

    Table List
    
    </th>
    </tr>
    <tr>
    <td valign="top">
    
    Partner determination procedure
    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    Customer account group function assignment
    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    Partnerfunction
    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    Partner function procedure
    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    Partner determination procedure assignment
    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    Partner function conversion
    
    </td>
    </tr>
    </table>
    



<a name="loio8207c31b665a4f39b7dfa621c2fb80fe__template-for-business-configurations-and-business-partner-determination"/>

## Template for Business Configurations and Business Partner Determination

Please refer to [SAP Note 2987243](https://help.sap.com/docs/link-disclaimer?site=https%3A%2F%2Flaunchpad.support.sap.com%2F#/notes/2987243) for the MS Excel template.



<a name="loio8207c31b665a4f39b7dfa621c2fb80fe__sap-customer-data-platform"/>

## SAP Customer Data Platform

Refer to [SAP Customer Data Platform documentation](https://help.sap.com/docs/SAP_CUSTOMER_DATA_PLATFORM/8438f051ded544d2ba1303e67fc5ff86/0eeae3ec78324b89b74abc882af49475.html) to know more about the configurations required to replicate business partner master data using the SAP Master Data Integration service.

