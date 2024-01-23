<!-- loio7612e09f5908445a92f08db5ca33c18f -->

# Extensibility

SAP Master Data Integration service provides the possibility to add custom fields and nodes to the integration models. The default way of defining these fields is via the Manage Business Object Typeconfiguration UI. This UI allows adding custom fields and nodes to all integration model entities of the SAP One Domain Model that are annotated with `@odm.extensible`.

All extension fields and nodes are valid for the One Domain Model version in which they are defined and for all following versions that are compatible. For more information, see [Integration Models](../about-this-service/integration-models-8882bf9.md).

Extension fields are not applied to previous versions, even if they are compatible. By default, extensions can be used in filters in REST-based extensions.

**Example:** Extending the `WorkforcePerson` object with the field `pilotLicense` in SAP One Domain Model version 2.0.0 will make the same extension fieldalso available in the *compatible*`WorkforcePerson` of SAP One Domain Model version 3.0.0.

If the field was added to `WorkforcePerson` on version 3.0.0, it would not be available in `WorkforcePerson` on version 2.0.0. It is possible to define the same extension field additionally in version 2.0.0, though the fields are exactly matching.

> ### Note:  
> An alternative way of using the Extensibility APIs directly is as described in this section. Composition based extensions can only be created with Extensibility APIs right now.



<a name="loio7612e09f5908445a92f08db5ca33c18f__extensibility-api"/>

## Extensibility API

The extensibility API allows adding custom fields to all integration model entities of the SAP One Domain Model that are annotated with `@odm.extensible`. Extensibility API supports `IsPotentiallySensitive` annotation. All extension fields, which are marked `IsPotentiallySensitive` will be audited. Extension configuration must not contain personal data. For more information on sensitive data, refer [Data Protection and Privacy](../security/data-protection-and-privacy-0fd158f.md). SOAP extensions would by default point to the corresponding parent entity. SOAP parameters have a target, which is the SOAP extension field name \(including prefix\) in the target system.



<a name="loio7612e09f5908445a92f08db5ca33c18f__prerequisites"/>

## Prerequisites

The Extensibility API can be used only by Business Users with the role

`ExtensionDeveloper`. Refer to [Authorization for Business Users](authorization-for-business-users-1e7e229.md) to request for the right authorization.

1.  Assign the role **ExtensionDeveloper** to the user who needs to conduct extensibility configuration.




<a name="loio7612e09f5908445a92f08db5ca33c18f__adding-node-level-and-field-level-extensions"/>

## Adding Node Level and Field Level Extensions

> **Caution** 

> Extension fields cannot be updated or deleted.


<table>
<tr>
<th valign="top">

Request body parameters

</th>
<th valign="top">

Description for Node Level Extension

</th>
<th valign="top">

Description for Field Level Extension

</th>
</tr>
<tr>
<td valign="top">

`extensionId` 

</td>
<td valign="top">

Unique id of the extension. It is a randomly generated UUID and must be provided by the user.

</td>
<td valign="top">

Unique id of the extension. It is a randomly generated UUID and must be provided by the user.

</td>
</tr>
<tr>
<td valign="top">

`extensionPoint` 

</td>
<td valign="top">

The name of entity/type/aspect to be extended, It should be annotated with `@odm.extensible: ['primitives']` in the model.

</td>
<td valign="top">

The name of entity/type/aspect to be extended, It should be annotated with `@odm.extensible: ['primitives']` in the model.

</td>
</tr>
<tr>
<td valign="top">

`namespace` 

</td>
<td valign="top">

Namespace of the extension. Namespace cannot start with `sap.odm` .

</td>
<td valign="top">

Namespace of the extension. Namespace cannot start with `sap.odm` 

</td>
</tr>
<tr>
<td valign="top">

`fieldName` 

</td>
<td valign="top">

The name of the new extension field. It should follow the pattern `ext__<namespace>__<customName>` .

</td>
<td valign="top">

The name of the new extension field. It should follow the pattern `ext__<namespace>__<customName>` .

</td>
</tr>
<tr>
<td valign="top">

`type` 

</td>
<td valign="top">

The type of the new node extension field. It should be one of the following - `Composition`.

</td>
<td valign="top">

The type of the new extension field. It should be one of the following -`String` `Boolean` `Date` `DateTime` `Double` `Time` `Integer` `Decimal` `UUID` .

</td>
</tr>
<tr>
<td valign="top">

`typeParameters` 

</td>
<td valign="top">

-   `relationship` - one or many
-   `name` - name of the entity type that will be added to the extended ODM model
-   `fields` - array of field level extensions that the node will contain.

Should contain

</td>
<td valign="top">

Additional parameters to specify further restrictions on the type specified. This field is **optional** and is only applicable if the type is `String` or `Decimal` .

</td>
</tr>
<tr>
<td valign="top">

`isPotentiallySensitive` 

</td>
<td valign="top">

Determines if the new field could contain personal sensitive data.

</td>
<td valign="top">

Determines if the new field could contain personal sensitive data.

</td>
</tr>
<tr>
<td valign="top">

`soapParameters` 

</td>
<td valign="top">

Additional parameters required if the extension should also be used for applications integrating via SOAP \(only applicable for BusinessPartner and BusinessPartnerRelationship\).

</td>
<td valign="top">

Additional parameters required if the extension should also be used for applications integrating via SOAP \(only applicable for BusinessPartner and BusinessPartnerRelationship\).

</td>
</tr>
<tr>
<td valign="top">

`soapParameters.target` 

</td>
<td valign="top">

The name of the field in the SOAP model.

</td>
<td valign="top">

The name of the field in the SOAP model.

</td>
</tr>
<tr>
<td valign="top">

`soapParameters.type` 

</td>
<td valign="top">

The type of the field in the SOAP model.

</td>
<td valign="top">

The type of the field in the SOAP model.

</td>
</tr>
<tr>
<td valign="top">

`soapParameters.namespace` 

</td>
<td valign="top">

Namespace of the extension in the SOAP model.

</td>
<td valign="top">

Namespace of the extension in the SOAP model.

</td>
</tr>
<tr>
<td valign="top">

`soapParameters.namespace.prefix` 

</td>
<td valign="top">

Prefix/definition for the namespace url. It should start with `extns`.

</td>
<td valign="top">

Prefix/definition for the namespace url. It should start with `extns`.

</td>
</tr>
<tr>
<td valign="top">

`soapParameters.namespace.value` 

</td>
<td valign="top">

The namespace url/value.

</td>
<td valign="top">

The namespace url/value.

</td>
</tr>
<tr>
<td valign="top">

`soapParameters.overrides` 

</td>
<td valign="top">

This parameter is required for providing different soap parameters based for different destinations. Note that the values in the parameter will not be supported in the initial scope.

</td>
<td valign="top">

This parameter is required for providing different soap parameters based for different destinations. Note that the values in the parameter will not be supported in the initial scope.

</td>
</tr>
</table>

> ### Note:  
> `soapParameters` only supported for 2.1.1 businesspartner and 2.2.0 businesspartner relationship.

> ### Note:  
> `<namespace>.<name-from-type-parameters>` `BP1.BPDigitalIdentity` After creating a node extension, the extension point of that node extension would be in this format:. In case of the above sample payload, the extension point would be.

**Example \(Node Level Extension\):** You can extend the business partner entity by adding a new node starting with **ext\_\_** with pattern **ext\_\_comSomeCustomer\_nodeName**. Follow the steps below:

**Example \(Field Level Extension\):** **ext\_\_** **ext\_\_comSomeCustomer\_fieldName** You can extend the business partner entity by adding a new field starting withwith pattern. Follow the steps below:

**Example \(Field Level Extension\(BusinessPartnerRelationship\)\):** **ext\_\_** **ext\_\_comSomeCustomer\_fieldName** You can extend the business partner relationship entity by adding a new field starting withwith pattern.

**Example \(get extension\):** You can fetch all existing extensions. Follow the steps below:

**Example \(status\):** You can check the activation status of the extension. Follow the steps below:

**Example \(UI\):** [SAP Master Data Orchestration UI](https://help.sap.com/viewer/8ce78b673ef04cc1bcfeb01c93ef7885/CLOUD/en-US/4841c92c3aec46bbaeb5abf2fdab9d00.html) Entities can also be extended via.

1.  `<mdi-url>/v1/odm/2.1.1/sap.odm.businesspartner.BusinessPartner/extensions` Url:.

2.  To add a new Node to One Domain Model, perform PUT operation with the below payload:

    ```
    {
      "extensionId": "c142ef94-9ce2-414c-7d2d-4725299a9f29",
      "extensionPoint": "sap.odm.businesspartner.BusinessPartner",
      "namespace": "BP1",
      "fieldName": "ext__BP1_digitalIdentity",
      "type": "Composition",
      "typeParameters": {
        "relationship": "one",
        "name": "BPDigitalIdentity",
        "fields": [
          {
            "extensionId": "a94a9b80-7890-49e5-9578-493b2a8181ed",
            "fieldName": "ext__BP1_identityId",
            "isPotentiallySensitive": false,
            "type": "String",
            "typeParameters": {
              "length": 36
            }
          },
          {
            "extensionId": "302ddf4f-7456-40bc-bd37-ed2b924c1b83",
            "fieldName": "ext__BP1_login",
            "isPotentiallySensitive": false,
            "type": "String",
            "typeParameters": {
              "length": 36
            }
          },
          {
            "fieldName": "ext__BP1_idpName",
            "extensionId": "cc9ec69e-c5d2-4c19-aa8b-8c73f816f84c",
            "type": "String",
            "isPotentiallySensitive": false,
            "typeParameters": {
              "length": 20
            }
          }
        ]
      }
    }
    ```


1.  To add a new Node to One Domain Model and SOAP Model, perform PUT operation with the below payload:

    ```
    {
      "extensionId": "d161e9a5-1f52-47fb-8380-2fb7c81c5249",
      "extensionPoint": "sap.odm.businesspartner.BusinessPartner",
      "namespace": "BP1",
      "fieldName": "ext__BP1_digitalIdentity",
      "type": "Composition",
      "soapParameters": {
        "target": "BusinessPartner/Common/ZDigitalIdentity",
        "type": "xs:token",
        "namespace": {
          "prefix": "extns1",
          "value": "http://sapcustomfields2.example.com/"
        },
        "overrides": []
      },
      "typeParameters": {
        "relationship": "many",
        "name": "BPCustomEntity",
        "fields": [
          {
            "isKey": true,
            "extensionId": "cc38b126-a533-4944-a7a1-b249ccddbb14",
            "fieldName": "ext__BP1_identityId",
            "isPotentiallySensitive": false,
            "type": "String",
            "typeParameters": {
              "length": 36
            },
            "soapParameters": {
              "target": "Id",
              "type": "xs:token",
              "namespace": {
                "prefix": "extns1",
                "value": "http://sapcustomfields2.example.com/"
              },
              "overrides": []
            }
          },
          {
            "isKey": false,
            "fieldName": "ext__BP1_login",
            "extensionId": "0af2ea04-ca09-46ed-ba64-f77046ecb11a",
            "isPotentiallySensitive": true,
            "type": "String",
            "typeParameters": {
              "length": 255
            },
            "soapParameters": {
              "target": "Login",
              "type": "xs:string",
              "namespace": {
                "prefix": "extns1",
                "value": "http://sapcustomfields2.example.com/"
              },
              "overrides": []
            }
          },
          {
            "isKey": true,
            "fieldName": "ext__BP1_idpName",
            "extensionId": "85d4c08a-0496-446c-8e45-8bf57856bf06",
            "isPotentiallySensitive": false,
            "type": "String",
            "typeParameters": {
              "length": 20
            },
            "soapParameters": {
              "target": "IdpName",
              "type": "xs:string",
              "namespace": {
                "prefix": "extns1",
                "value": "http://sapcustomfields2.example.com/"
              },
              "overrides": []
            }
          }
        ]
      }
    }
    ```

2.  To add a field to an already added Node Entity, perform PUT operation with the below payload:

    ```
    {
      "extensionId": "262d7959-2a26-4d3a-ab09-2dc2b9befe38",
      "extensionPoint": "ext__BP1_BPDigitalIdentity",
      "namespace": "someOtherNamespace",
      "fieldName": "ext__someOtherNamespace_idpIdentifier",
      "type": "String",
      "typeParameters": {
        "length": 20
      },
      "isPotentiallySensitive": false,
      "soapParameters": {
        "target": "IdpIdentifier",
        "type": "xs:string",
        "namespace": {
          "prefix": "extns_1",
          "value": "http://sapcustomfield2.example.com/"
        },
        "overrides": []
      }
    }
    ```


1.  `<mdi-url>/v1/odm/2.1.1/sap.odm.businesspartner.BusinessPartner/extensions` Url:.

2.  Perform PUT operation with the below REST-based payload:

    ```
    {
      "extensionId": "bd3ba922-953d-49b2-bb37-7e9194efd883",
      "extensionPoint": "sap.odm.businesspartner.BusinessPartner",
      "namespace": "namespace",
      "fieldName": "ext__comNamespace_customFiel912",
      "type": "String",
      "typeParameters": {
        "length": 20
      },
      "isPotentiallySensitive": false
    }
    ```

3.  Perform PUT operation with the below REST+SOAP based payload:

    ```
    {
      "extensionId": "bd3ba922-953d-49b2-bb37-7e9194efd883",
      "extensionPoint": "sap.odm.businesspartner.BusinessPartner",
      "namespace": "namespace",
      "fieldName": "ext__comNamespace_customFiel912",
      "type": "String",
      "typeParameters": {
        "length": 20
      },
      "isPotentiallySensitive": false,
      "soapParameters": {
        "target": "z_bp_customField912",
        "type": "xs:token",
        "namespace": {
          "prefix": "extns_1",
          "value": "http://sapcustomfields.example.com/"
        },
        "overrides": []
      }
    }
    ```


1.  Url:. `<mdi-url>/v1/odm/<odm-version>/<odm-entity-name>/extensions` 

2.  Perform the GET operation. Response will have an array of all existing extensions.

    Sample response when all existing extensions are fetched:

    ```
    {
      "extensions": [
        {
          "extensionId": "36dba9e8-fe46-42b7-951f-df0777bec2a2",
          "extensionPoint": "sap.odm.businesspartner.BusinessPartner",
          "namespace": "namespace",
          "fieldName": "ext__comNamespace_customField912",
          "isPotentiallySensitive": false,
          "type": "String",
          "typeParameters": {
            "length": 20
          }
        },
        {
          "extensionId": "36dba9e8-fe46-42b7-951f-df0777bec2e1",
          "extensionPoint": "sap.odm.businesspartner.BusinessPartner",
          "namespace": "namespace",
          "fieldName": "ext__comNamespace_customField234",
          "isPotentiallySensitive": false,
          "type": "String",
          "typeParameters": {
            "length": 30
          }
        }
      ]
    }
    ```


1.  `<mdi-url>/v1/odm/<odm-version>/<odm-entity-name>Url:. /extensions/<extension-id>/status` 

2.  `<mdi-url>/v1/odm/2.1.1/sap.odm.businesspartner.BusinessPartner/extensions/bd3ba922-953d-49b2-bb37-7e9194efd883/status` Perform the GET operation, sample URL:.z

    `activationInProgress` `activated` `failed` Response will have status value as,ordepending upon extension's creation status.

    Sample response when extension is activated:

    Sample response when extension is rejected:

    ```
    {
      "status": "activated"
    }
    ```

    ```
    {
      "status": "failed",
      "rejectionReason": "Replication to Hana failed"
    }
    ```




<a name="loio7612e09f5908445a92f08db5ca33c18f__generate-extended-wsdl"/>

## Generate Extended WSDL

Once all the extensions are accurately defined and activated, the subsequent step involves generating an extended WSDL, which serves as a meta-document for SOAP services. Initiating this SOAP extension requires triggering an HTTP PUT request. This request is OAuth-protected, and the URL can be obtained through the following steps:

1.  Navigate to the service keys created for the service instance in your subaccount.

2.  The BASE\_URL is mentioned in the URI.




<a name="loio7612e09f5908445a92f08db5ca33c18f__sample"/>

## Sample

**To extend WSDL:** 

`Business Partner:<BASE_URL>/businesspartner/v0/soap/extend` 

**To retrieve extended WSDL:** 

`https://one-mds.cfapps.{region}.hana.ondemand.com` Here, the <BASE\_URL\> is. The corresponding region of the base URL can be fetched from "uri" present in service keys of the service instance for Generic Configuration, created as part of [Connecting SOAP Applications](connecting-soap-applications-14fcc48.md) .

-   `{}` Request type: PUT with empty body like -

-   Authorization token is needed in header


-   URL:

    `<BASE_URL>/businesspartner/v0/soap/BusinessPartnerBulkReplicateRequestIn.wsdl` Business Partner:

-   Request type: GET

-   Authorization token is needed in header


