<!-- loio2b6b9a66c8fb40a6ac561574b1d820f3 -->

# Security Guidelines

This section covers the security aspects related to SAP Master Data Integration service.

SAP Master Data Integration relies on SAP BTP infrastructure for protecting the connections using Transport Layer Security \(TLS\). Find more information about SAP Business Technology Platform TLS Connectivity support in the section **Transport Layer Security \(TLS\) Connectivity Support** at [SAP Business Technology Platform](https://help.sap.com/viewer/product/CP/Cloud/en-US?task=discover_task) Security.



<a name="loio2b6b9a66c8fb40a6ac561574b1d820f3__protect-your-credentials"/>

## Protect your credentials

Credentials used by clients may allow read and write access to the master data of your company. Make sure they are always stored securely. Credentials that have been stored insecurely should be rotated. See the [Rotate leaked credentials](security-guidelines-2b6b9a6.md#loio2b6b9a66c8fb40a6ac561574b1d820f3__rotate-leaked-credentials) section for instructions on how to do this.



<a name="loio2b6b9a66c8fb40a6ac561574b1d820f3__always-use-https"/>

## Always use HTTPS

Ensure that HTTPS is used in every communication with MDI or XSUAA. Pay attention not only to the configuration of the integration in the client applications and in the Destination Service, but also to requests sent manually in order to debug the integration. If for any reason HTTP is used in some request, follow the steps in the [Rotate leaked credentials](security-guidelines-2b6b9a6.md#loio2b6b9a66c8fb40a6ac561574b1d820f3__rotate-leaked-credentials)section.



<a name="loio2b6b9a66c8fb40a6ac561574b1d820f3__enforce-validation-of-https-certificates-in-the-client"/>

## Enforce validation of HTTPS certificates in the client

If your client application allows choosing to validate the certificates used in the HTTPS connection, make sure that it does validate them.

Disabling such validation allows attackers to impersonate the master data integration service or XSUAA, capture the used credentials or spy on the traffic between the client application and master data integration.

If for any reason HTTPS certificates are not validated in some request, follow the steps in the [Rotate leaked credentials](security-guidelines-2b6b9a6.md#loio2b6b9a66c8fb40a6ac561574b1d820f3__rotate-leaked-credentials) section.



<a name="loio2b6b9a66c8fb40a6ac561574b1d820f3__rotate-leaked-credentials"/>

## Rotate leaked credentials

If the protection mechanisms are not present in a request, the credentials used in this request may have been leaked and should be treated as such. The same applies when credentials have been stored insecurely.

Delete the service key corresponding to the leaked credentials from your service instance to ensure that they are invalidated. Create a new service key to replace the leaked one, and configure the respective client with the newly generated credentials.



<a name="loio2b6b9a66c8fb40a6ac561574b1d820f3__report-a-security-issue"/>

## Report a Security Issue

You can report security issues via SAP Security Management, at [Report a security issue](https://www.sap.com/about/trust-center/security/incident-management.html).

