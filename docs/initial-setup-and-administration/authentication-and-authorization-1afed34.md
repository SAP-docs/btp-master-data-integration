<!-- loio1afed34e287640ee90a27d29043e0f34 -->

# Authentication and Authorization

SAP Master Data Integration has two main kinds of users:

-   SAP Master Data Integration clients, machines that consume master data APIs, herein after called "clients"; and

-   People or machines that consume administrative APIs, herein after called "business users".


Both of them can only use SAP Master Data Integration in the context of a tenant. The tenant is identified by the BTP subaccount that the service instance belongs to or that the business users belongs to.

The identities of each of those kinds of users are managed in the following ways:

-   Clients are represented by service instances of the SAP Master Data Integration service in the BTP subaccount that represent their tenants.

-   Business users are provided by the Identity Provider that is connected to the BTP subaccount that represent the respective tenant.




<a name="loio1afed34e287640ee90a27d29043e0f34__authentication-protocol"/>

## Authentication protocol

Both clients and business users authenticate against SAP Master Data Integration through the XSUAA service using OAuth 2.0 authentication flows.

```
{
  "access_token": "...",
  "token_type": "bearer",
  "id_token": "...",
  "expires_in": 43199,
  "scope": "...",
  "jti": "..."
}
```

The user must then use this token in the `Authorization: Bearer <<session_token>>` HTTP header to authenticate the requests it sends to SAP Master Data Integration, as specified in [RFC 6750](https://www.rfc-editor.org/rfc/rfc6750) .

