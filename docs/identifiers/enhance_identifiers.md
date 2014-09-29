# Identifiers:



## Goal:

 Validate dataset identifiers

- Is there a DOI
- Does the URL function
-- how deep should go in this step?
-- Is format correct



## Steps:

## Identifier Patterns
* DOI
* OrchidID
* 

## Validations:

- Is the identifier a known pattern





## Enhancements:



- Created Linked data references for elements without them. 

-





## Cinergi Object Example:
Two places:
- resourceURI
- relatedResource

[Link to github example](https://github.com/usgin/json-metadata/blob/master/ExampleNGDSJSONMetadata.json#)



```[json]

"jmd:describedResource": {
           "jmd:resourceTitle": "Title that identifies the resource for human users.",
           "jmd:resourceDescription": "Free text description of the resource.",
           "jmd:resourceURI": "example:FreestandingURI",
           "jmd:resourceURI": {
               "jmd:citationIdentifier": "usgin:dlio2011-13",
               "jmd:scopedIdentifierAuthority": {
                   "jmd:referenceLabel": "USGIN metadata 1.3",
                   "jmd:referenceURI": "http://usgin.org/specs/dummyURI/metadata"
               }
           },

            "jmd:relatedResource": {
                "description": "links to related resources. The relation property on the link defines the association type, and the link label provides the related resource name",
                "type": "array",
                "items": {
                    "$ref": "#/definitions/Link"
                }
            },

```



## Dublin Core Source:
the about string is an identifier.
The dc:identifier is the identifier of the resource

```
<rdf:Description rdf:about="http://data.nodc.noaa.gov/geoportal/csw?request=GetCapabilities&amp;service=csw&amp;version=2.0.2">

<dc:identifier>http://data.nodc.noaa.gov/geoportal/csw?request=GetCapabilities&amp;service=csw&amp;version=2.0.2</dc:identifier>
</rdf:Description >

```


## Iso Source:
Resource Identifier for  a metadata record
`/gmd:MD_Metadata/gmd:fileIdentifier[1]/gco:CharacterString[1]`



