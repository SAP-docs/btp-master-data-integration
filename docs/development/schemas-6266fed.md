<!-- loio6266feda9fb34ff9afdde787910e4d52 -->

# Schemas

SAP Master Data Integration derives a *physical data model* from the *logical data model* defined by [SAP One Domain Model](https://github.wdf.sap.corp/pages/DMA/ODM/) . The physical model is the interchange format when communicating with Master Data Integration.

The *schema API* of Master Data Integration provides [JSON schemas](https://json-schema.org/) describing the payload structure for a specific entity type and version.

The endpoints of the schema API are protected and require [authentication](../initial-setup-and-administration/authentication-of-business-users-ef53987.md) with each request. The schema API is available to both technical users and business users.



<a name="loio6266feda9fb34ff9afdde787910e4d52__schema-for-instance-data"/>

## Schema for Instance Data

To retrieve the schema of the instance data for an entity type `{entityTypeName}` in One Domain Model version `{odmVersion}` , send a `GET` request to the instance schema endpoint.

```
curl --location --request GET '{mdi_url}/v1/odm/{odmVersion}/{entityTypeName}/api/instance' \
				--header 'Content-Type: application/json' \
				--header 'Authorization: Bearer {access_token}'
```

For instance, requesting the instance schema for `sap.odm.workforce.WorkforcePerson` in One Domain Model version `3.0.0` yields a response like shown in the following example.

```
{
				"type": "object",
				"required": ["id", "externalId"],
				"properties": {
				"id": {
				"type": "string",
				"pattern": "^[0-9a-f]{8}-[0-9a-f]{4}-[0-9a-f]{4}-[0-9a-f]{4}-[0-9a-f]{12}$"
				},
				"purposes": {
				"type": "array",
				"items": {
				"type": "object",
				"properties": {
				"purpose": {
				"type": "object",
				"required": ["id"],
				"properties": {
				"id": {
				"type": "string",
				"pattern": "^[0-9a-f]{8}-[0-9a-f]{4}-[0-9a-f]{4}-[0-9a-f]{4}-[0-9a-f]{12}$"
				}
				}
				}
				}
				}
				},
				"externalId": {
				"type": "string",
				"maxLength": 100
				}
				// ... (more optional properties)
				}
				}
```



<a name="loio6266feda9fb34ff9afdde787910e4d52__extensions"/>

## Extensions

Any custom [extensions](../initial-setup-and-administration/extensibility-7612e09.md) defined on the One Domain Model entity and version is included in the schema returned by the Schema API of Master Data Integration.

