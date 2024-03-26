<!-- loio1352e053fb69487abd73a15d560066af -->

# Authentication of Applications

For each application that is connected to an SAP Master Data Integration tenant, there is exactly one service instance of the SAP Master Data Integration service in the BTP subaccount. This service instance is used to establish technical connectivity between the application and the tenant of SAP Master Data Integration. The credentials are managed using service key, also called a service binding, via BTP Cockpit. Each service key contains a set of credentials. The kind of credentials depends on which kind was used at the creation of the service.

SAP Master Data Integration allows two kinds of credentials, which can be used with two OAuth 2.0 authentication flows:

-   [OAuth 2.0 Mutual-TLS Client Authentication and Certificate-Bound Access Tokens](https://tools.ietf.org/html/rfc8705) for authentication using mutual-TLS \(mTLS\), based on X.509 client certificates. This is the recommended way of authentication. Choose this when it is supported.

-   [OAuth 2.0 Client Credentials Grant](https://tools.ietf.org/html/rfc6749#section-4.4) for authentication using `client_id` / `client_secret` pairs.


In all authentication methods, the URL of the XSUAA service and the credentials are present in the `uaa` field of the service key. For example,

```
{
			...
			"uaa": {
			"clientid": "<<client_id>>",
			"url": "<<xsuaa_url>>",
			...
			"certificate": "<<certificate>>",
			...
			"key": "<<private key>>"
			...
			}
			...
			}
```

```
{
			...
			"uaa": {
			"clientid": "<<client_id>>",
			"clientsecret": "<<client_secret>>",
			"url": "<<xsuaa_url>>",
			...
			}
			...
			}
```



<a name="loio1352e053fb69487abd73a15d560066af__authentication-using-mutual-tls-and-x509-client-certificates"/>

## Authentication Using Mutual-TLS and X.509 Client Certificates

There are two possibilities to generate service keys for X.509 mTLS-based authentication.

-   The public key can be provided by the user; or

-   XSUAA can generate a key-pair and certificates for you.




<a name="loio1352e053fb69487abd73a15d560066af__configuring-the-service-key"/>

## Configuring the Service Key

Create a service key with the excerpt below passed as a parameter:

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



<a name="loio1352e053fb69487abd73a15d560066af__using-curl-to-authenticate"/>

## Using cURL to Authenticate

```
curl --location --request POST "$xsuaa_url/oauth/token" \
				--header "Content-Type: application/x-www-form-urlencoded" \
				--header "Accept: application/json" \
				--user "$client_id:$client_secret" \
				--data-urlencode "client_id=$client_id" \
				--data-urlencode "grant_type=client_credentials"
```

```
curl --location --request POST "$xsuaa_url/oauth/token" \
				--header "Content-Type: application/x-www-form-urlencoded" \
				--header "Accept: application/json" \
				--user "$client_id:$client_secret" \
				--data-urlencode "client_id=$client_id" \
				--data-urlencode "grant_type=client_credentials"
```



<a name="loio1352e053fb69487abd73a15d560066af__authentication-using-client-idclient-secret"/>

## Authentication Using client\_id/client\_secret



<a name="loio1352e053fb69487abd73a15d560066af__configuration-of-the-service-key"/>

## Configuration of the Service Key

For historical reasons, the service keys are configured by default for authentication based on client\_it/client\_secret. No parameter is necessary during the creation of these service keys.



<a name="loio1352e053fb69487abd73a15d560066af__using-curl-to-authenticate-1"/>

## Using cURL to Authenticate

```
curl --location --request POST "$xsuaa_url/oauth/token" \
				--header "Content-Type: application/x-www-form-urlencoded" \
				--header "Accept: application/json" \
				--user "$client_id:$client_secret" \
				--data-urlencode "client_id=$client_id" \
				--data-urlencode "grant_type=client_credentials"
```



<a name="loio1352e053fb69487abd73a15d560066af__related-information"/>

## Related Information

-   [Retrieve Access Token](https://help.sap.com/docs/BTP/65de2977205c403bbc107264b8eccf4b/6391b5dfe4704c6c8b71a32126828e9c.html?locale=en-US) documentation about access token.

-   [Add users in subaccount](https://help.sap.com/products/BTP/65de2977205c403bbc107264b8eccf4b/2c91f88e60ea4677a076212085b42d02.html?locale=en-US) documentation for more details.

-   [Add users to your IDP](https://help.sap.com/viewer/e61957c3eb584a7ba8e49bf687f65ad5/latest/en-US/67bb7ceef8b04cf981a9e0cfde07d415.html) documentation for more details.


