<!-- loio93d7b77378ad498da2f0a2f2d802fcf3 -->

# SOAP APIs for Business Partners

> ### Note:  
> Basic Authentication and OAuth authentication are supported for these endpoints. Refer to your service keys for the **clientid** and **clientsecret** . In Basic Authentication: **username** is the **clientid** and **password** is the **clientsecret** from your service keys.

> ### Note:  
> If using Basic Authentication, the URL query parameter **tenandId** is needed. For example:
> 
> ```
> 
> 				https://one-mds.cfapps.<region>.hana.ondemand.com:443/businesspartner/v0/soap/BusinessPartnerBulkReplicateRequestIn?tenantId=<identityzone>
> 			
> ```

Following are the endpoints for SOAP replication in SAP Master Data Integration - Business Partners. You can call these endpoints through HTTP POST request:

1.  BusinessPartner Inbound:


```

			Sample Code:
			https://one-mds.cfapps.{region}.hana.ondemand.com/businesspartner/v0/soap/BusinessPartnerBulkReplicateRequestIn
		
```

1.  BusinessPartner Confirmation Inbound:


```

			Sample Code:
			https://one-mds.cfapps.{region}.hana.ondemand.com/businesspartner/v0/soap/BusinessPartnerBulkReplicateRequestConfIn
		
```

1.  BusinessPartner Relationship Inbound:


```

			Sample Code:
			https://one-mds.cfapps.{region}.hana.ondemand.com/businesspartner/v0/soap/BusinessPartnerRelationshipBulkReplicateRequestIn
		
```

1.  BusinessPartner Relationship Confirmation Inbound:


```

			Sample Code:
			https://one-mds.cfapps.{region}.hana.ondemand.com/businesspartner/v0/soap/BusinessPartnerRelationshipBulkReplicateRequestConfirmIn
		
```

1.  KeyMapping Inbound:


```

			Sample Code:
			https://one-mds.cfapps.{region}.hana.ondemand.com/businesspartner/v0/soap/KeyMappingBulkReplicateRequestIn
		
```

1.  KeyMapping Confirmation Inbound:


```

			Sample Code:
			https://one-mds.cfapps.{region}.hana.ondemand.com/businesspartner/v0/soap/KeyMappingBulkReplicateRequestConfirmIn
		
```

> ### Note:  
> The values required can be retrieved from **SAP BTP Cockpit \> Subaccount \> Spaces \> Service \> Service Instance \> Service Keys** 
> 
> -   TenantHost/Subdomain: Value corresponding to identityzone
> 
> -   tenantId: Value corresponding to identityzone
> 
> -   BusinessSystemName/SourceSystem: Value for own system

