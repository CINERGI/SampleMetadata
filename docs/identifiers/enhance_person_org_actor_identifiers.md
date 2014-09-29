# Person Org Agent Identifiers:

## Goal:
  Associate names with known identifiers
- Find and associate with a name
- imporve metadata by allowing for links to outside services, like publications.
- maintain "roles" of person


## Steps:

## Validations:

- if identifier is a well known one (orcid, etc), is it valid.
- ISO, is there a known role type


## Enhancements:
- Do we have a known identifier for person/org/agent
-- Created Linked data references for elements without them. 
- Can we add a role, if there is none?


## Cinergi Object Example:
[Link to github example](https://github.com/usgin/json-metadata/blob/master/ExampleNGDSJSONMetadata.json#)

```[json]
"jmd:resourceContact": {
               "jmd:agentRole": {
                   "jmd:conceptPrefLabel": "compiler"
               },
               "jmd:individual": {
                   "jmd:personURI": "usgin:personIdentifer",
                   "jmd:personName": "Adrian the Great",
                   "jmd:personName": "theOther Author"
               },
               "jmd:organizationName": ["The Research Giant Company", "RGC"],
               "jmd:contactPhoneNumber": "520-888-0000",
               "jmd:contactEmail": "someEmail@researchgiant.com"
           },
            "jmd:resourceType": [{
                "jmd:conceptURI": "ResourceCategory1URI",
                "jmd:conceptPrefLabel": "category1 label "
                    }, 
                                 {
                "jmd:conceptURI": "resourceCategory2URI",
                "jmd:conceptPrefLabel": "category label"
                    }],
            "jmd:resourceStatus": {
                "jmd:conceptURI": "resourceStatusTermURI",
                "jmd:conceptPrefLabel": "Testing"
            },
            "jmd:resourceBrowseGraphic": {
                "jmd:referenceLabel": "text to identify the reference in a UI",
                "jmd:referenceURI": "description",
                "jmd:referenceLink": [{
                    "jmd:link": "uri",
                    "jmd:linkRelation": [{
                        "jmd:referenceLabel": "text to identify the reference in a UI",
                        "jmd:referenceURI": "description"
                        }],
                    "jmd:linkTitle": "text to label this link in a UI"
                    }]
            },

```

## Dublin Core Source:

```[xml]
<dc:contributor>NOAA NESDIS National Oceanographic Data Center</dc:contributor>

<dc:author>NOAA NESDIS National Oceanographic Data Center</dc:author>

<dc:creator>NOAA NESDIS National Oceanographic Data Center</dc:creator>
```


## Iso Source:
- always a gmd:CI_ResponsibleParty element
-- need to evaluate the gmd:role/gmd:CI_ROleCode to determing
- several locations:
-- gmd:MD_metadata/gmd:contact |gmi:MD_metadata/gmd:contact
-- gmd:identificationInfo/gmd:MD_DataIdentification/gmd:pointOfContact/


- - -

### Complete responsible party

```[xml]
 <gmd:CI_ResponsibleParty>
            <gmd:organisationName>
                <gco:CharacterString>NOAA National Oceanographic Data Center</gco:CharacterString>
            </gmd:organisationName>
            <gmd:positionName>
                <gco:CharacterString>Data Officer</gco:CharacterString>
            </gmd:positionName>
            <gmd:contactInfo>
                <gmd:CI_Contact>
                    <gmd:phone>
                        <gmd:CI_Telephone>
                            <gmd:voice>
                                <gco:CharacterString>301-713-3272</gco:CharacterString>
                            </gmd:voice>
                            <gmd:facsimile>
                                <gco:CharacterString>301-713-3302</gco:CharacterString>
                            </gmd:facsimile>
                        </gmd:CI_Telephone>
                    </gmd:phone>
                    <gmd:address>
                        <gmd:CI_Address>
                            <gmd:deliveryPoint>
                                <gco:CharacterString>1315 East-West Highway, SSMC 3, 4th floor</gco:CharacterString>
                            </gmd:deliveryPoint>
                            <gmd:city>
                                <gco:CharacterString>Silver Spring</gco:CharacterString>
                            </gmd:city>
                            <gmd:administrativeArea>
                                <gco:CharacterString>MD</gco:CharacterString>
                            </gmd:administrativeArea>
                            <gmd:postalCode>
                                <gco:CharacterString>20910-3282</gco:CharacterString>
                            </gmd:postalCode>
                            <gmd:country>
                                <gco:CharacterString>U.S.A.</gco:CharacterString>
                            </gmd:country>
                            <gmd:electronicMailAddress>
                                <gco:CharacterString>NODC.DataOfficer@noaa.gov</gco:CharacterString>
                            </gmd:electronicMailAddress>
                        </gmd:CI_Address>
                    </gmd:address>
                    <gmd:onlineResource>
                        <gmd:CI_OnlineResource>
                            <gmd:linkage>
                                <gmd:URL>http://www.nodc.noaa.gov/</gmd:URL>
                            </gmd:linkage>
                            <gmd:protocol>
                                <gco:CharacterString>HTTP</gco:CharacterString>
                            </gmd:protocol>
                            <gmd:name>
                                <gco:CharacterString>NOAA National Oceanographic Data Center website</gco:CharacterString>
                            </gmd:name>
                            <gmd:description>
                                <gco:CharacterString>Main NODC website providing links to the NODC Geoportal and access links to data and data services.</gco:CharacterString>
                            </gmd:description>
                            <gmd:function>
                                <gmd:CI_OnLineFunctionCode codeList="http://www.ngdc.noaa.gov/metadata/published/xsd/schema/resources/Codelist/gmxCodelists.xml#CI_OnLineFunctionCode" codeListValue="information" codeSpace="002">information</gmd:CI_OnLineFunctionCode>
                            </gmd:function>
                        </gmd:CI_OnlineResource>
                    </gmd:onlineResource>
                </gmd:CI_Contact>
            </gmd:contactInfo>
            <gmd:role>
                <gmd:CI_RoleCode codeList="http://www.isotc211.org/2005/resources/Codelist/gmxCodelists.xml#CI_RoleCode" codeListValue="custodian" codeSpace="002">custodian</gmd:CI_RoleCode>
            </gmd:role>
        </gmd:CI_ResponsibleParty>
        ```language
```
