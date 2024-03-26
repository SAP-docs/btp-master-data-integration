<!-- loioef53987fbbdd41e3a76eea95485ab0d2 -->

# Authentication of Business Users

There are two possible flows for authentication of business users:

-   `passcode` flow. Recommended where it is available.

-   `password` flow.


To work around limitations to identify the BTP subaccount that a user is trying to use when authenticating themselves in XSUAA, it is necessary to inform the credentials of a service instance in addition to the credentials of the own user. Because of that, we recommend that administrators create a service instance that does not represent any client, and that is only used to help in the authentication of business users.

The steps described in the sections below consider the `clientid` and `clientsecret` obtained from a service key of this administrative service instance.



<a name="loioef53987fbbdd41e3a76eea95485ab0d2__authentication-using-passcode-flow"/>

## Authentication Using Passcode Flow

Visit `<<xsuaa_url>>/passcode` to get the required passcode.

```
curl --location --request POST "$xsuaa_url/oauth/token" \
				--header "Content-Type: application/x-www-form-urlencoded" \
				--header "Accept: application/json" \
				--user "$client_id:$client_secret" \
				--data-urlencode "grant_type=password" \
				--data-urlencode "passcode=$passcode"
```



<a name="loioef53987fbbdd41e3a76eea95485ab0d2__authentication-using-password-flow"/>

## Authentication Using Password Flow

```
curl --location --request POST "$xsuaa_url/oauth/token?grant_type=password" \
				--header "Content-Type: application/x-www-form-urlencoded" \
				--user "$client_id:$client_secret" \
				--data-urlencode "username=$username" \
				--data-urlencode "password=$password"
```



<a name="loioef53987fbbdd41e3a76eea95485ab0d2__related-information"/>

## Related Information

-   [Retrieve Access Token](https://help.sap.com/docs/BTP/65de2977205c403bbc107264b8eccf4b/6391b5dfe4704c6c8b71a32126828e9c.html?locale=en-US) documentation about access token.

-   [Add users in subaccount](https://help.sap.com/products/BTP/65de2977205c403bbc107264b8eccf4b/2c91f88e60ea4677a076212085b42d02.html?locale=en-US) documentation for more details.

-   [Add users to your IDP](https://help.sap.com/viewer/e61957c3eb584a7ba8e49bf687f65ad5/latest/en-US/67bb7ceef8b04cf981a9e0cfde07d415.html) documentation for more details.


