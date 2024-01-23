<!-- loio7701dff87ab249c5bee643b233e037ef -->

# OAuth2-based Authentication

[Connecting Applications](connecting-applications-69ae614.md) As an alternative to the authentication via Client ID and Client Secret described in theSAP Master Data integration also supports OAuth2-based authentication with mutual TLS. Details on the support of OAuth2-based authentication from the client side can be found in the respective client documentation. Different clients can be connected via different authentication methods with the SAP Master Data Integration service.



<a name="loio7701dff87ab249c5bee643b233e037ef__oauth2-client-credentials"/>

## OAuth2 Client Credentials

If no parameters are provided during service binding or service key creation, a binding-level client ID and client secret is created by default for an OAuth2 client credentials flow.



<a name="loio7701dff87ab249c5bee643b233e037ef__xsuaa-managed-certificates"/>

## XSUAA-managed Certificates

If the following configuration is passed during service binding or service key creation, a private key and corresponding certificate are generated in the service binding. You can specify the desired key length and validity of the generated certificate.

Please note that authentication will only work as long as the certificate is valid. To renew or revoke the certificate, renew or delete the service binding or service key.

Configuration to be passed during service binding or service key creation for XSUAA-managed certificates:

-   `key-length` `2048` specifies the byte length of the generated private key, defaults to.

-   `validity-type` `DAYS` `MONTHS` `YEAR` `DAYS` specifies the validity time unit, only,andS are supported, defaults to.

-   `validity` `validity-type` `7` `7` specifies the number of time units in, defaults to, thus the complete validity defaults todays.


```
{
				"xsuaa": {
				"credential-type": "x509",
				"x509": {
				"key-length": 2048,
				"validity": 7,
				"validity-type": "DAYS"
				}
				}
				}
```



<a name="loio7701dff87ab249c5bee643b233e037ef__externally-managed-certificates"/>

## Externally-managed Certificates

If the following configuration is passed during service binding or service key creation, a user-provided certificate is used for authentication.

Configuration to be passed during service binding or service key creation for externally-managed certificates:

The base URL for token retrieval with X.509 authentication is slightly different compared to the one used in the OAuth2 client credentials flow:

`<uaa.url>/.well-known/openid-configuration` `mtls_endpoint_aliases` The specific endpoints for your subaccount can be retrieved via theendpoint of XSUAA, where they appear as.

`client_credentials` `client_secret` `client_id` The grant type for X.509-based OAuth2 authentication remains. Furthermore, you can omit the parameter, while the parameterstill needs to be passed.

-   `ensure-uniqueness` `false` ensures that the certificate has to be unique among all following instances, defaults to.

-   `certificate-pinning` `false` `false` `true` `false` set toallows for an eased credential rotation: The incoming certificate's subject and issuer distinguished name is compared to those of the stored certificate. If they match and the certificate was issued on or after the stored issuer date, the authentication is accepted. Afterwards, the incoming certificate's issuer date is stored for future authentication attempts. For instance, at first, assume a binding is created with a certificate specified in the binding request. This certificate can then be used normally until it expires. However, when the certificate should be rotated and certificate pinning is set to, the service allows for a rotation without creating a new binding or rebinding the service: When a token request is performed with a new certificate \(issued by the same root CA, with the same subject distinguished name, and with a newer issuer date\) the service will save the new issuer date and will only accept certificates that are issued at this or a newer point of time. Thus, the old/initial certificate will automatically not be accepted anymore. Defaults todue to compatibility reasons,is recommended for an easier rotation.


-   `<uaa.certurl>/oauth/token` X.509-based OAuth2:

-   `<uaa.url>/oauth/token` OAuth2 client credentials:


```
{
				"xsuaa": {
				"credential-type": "x509",
				"x509": {
				"certificate": "-----BEGIN CERTIFICATE-----...-----END CERTIFICATE-----",
				"ensure-uniqueness": false,
				"certificate-pinning": false
				}
				}
				}
```

> ### Note:  
> To renew credentials of a client, navigate to the service instance that represents this client and perform the following steps:
> 
> -   Create a new service binding for the same service instance. This will enable the new credentials of the new service binding.
> 
> -   [disconnecting the client](disconnecting-applications-d09d7b9.md) Delete the service binding belonging to the credentials that are supposed be invalidated. This disables authentication with credentials of the deleted service binding. Follow the same steps to create the service binding and copy the credentials into your client. But make sure to only delete the service key and not the service instance, as this will have the effect of.

