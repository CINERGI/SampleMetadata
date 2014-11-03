# Keyword:



## Goal:

 Enchance searching by subject keyword  by

- Associating Keywords with a known thesaurus.

- Discovering new Thesaurii and terms

- Extracting additional keywords from document title, purpose and absctracts



## Steps:



## Validations:

- Keywords are known

- kewords are in vocabularies



## Enhancements:



- Created Linked data references for elements without them. 

- Identify new vocabularies

- Add keywords from other elements (title abstract)





## Cinergi Object Example:
```
"cmd:resourceIndexTerms": {
        "cmd:keywordType": {
            "cmd:keywordTypeLabel":"",
            "cmd:keywordTypeURI":"",
            "cmd:keywordTypeVocabularyURI":""
        },
        "cmd:keywords": 
          ["",""  ]
        ,
        "cmd:keywordSourceReference":{
            "cmd:keywordSourceLabel":"",
            "cmd:keywordSourceURI":""
        }
        
        
    }
```


## Dublin Core Source:

`<dc:subject>Hydrology</dc:subject>`

```

"cmd:resourceIndexTerms": {
        "cmd:keywordType": {
            "cmd:keywordTypeLabel":"dc_subject",
             "cmd:keywordTypeURI":"htrp://prul.org/dc/subject",
            "cmd:keywordTypeVocabularyURI":"undefined"
        },
        "cmd:keywords": 
          ["Hydrology" ]
        ,
        "cmd:keywordSourceReference":{
            "cmd:keywordSourceLabel":"undefined",
        }


    }
```

```

"cmd:resourceIndexTerms": {
        "cmd:keywordType": {
            "cmd:keywordTypeLabel":"dc_dubject",
           "cmd:keywordTypeURI":"htrp://prul.org/dc/subject",
            "cmd:keywordTypeVocabularyURI":"undefined"
        },
        "cmd:keywords": 
          ["",""  ]
        ,
        "cmd:keywordSourceReference":{
            "cmd:keywordSourceLabel":"ODM",
            "cmd:keywordSourceURI":"http://www.example.com/cuahsi"
        }


    }
```



## Iso Source:

Iso xml examples have several variants. 



Xpath for keywords:



`/gmi:MI_Metadata/gmd:identificationInfo[1]/gmd:MD_DataIdentification[1]/gmd:descriptiveKeywords[3]/gmd:MD_Keywords`



`/gmi:MI_Metadata/gmd:identificationInfo[1]/gmd:MD_DataIdentification[1]/gmd:topicCategory[1]/gmd:MD_TopicCategoryCode[1]`



- - -



### basic

-





- - -

### Iso type specified

 /gmi:MI_Metadata/gmd:identificationInfo[1]/gmd:MD_DataIdentification[1]/gmd:descriptiveKeywords[3]/gmd:MD_Keywords[1]/gmd:type



## ISO Types:



-  Type specified, not an iso reference

-- but is really an iso term

- Not an iso term



## Thesaurus Name Specified:

### Object: 

`

- gmi:MI_Metadata/gmd:identificationInfo[1]/gmd:MD_DataIdentification[1]/gmd:descriptiveKeywords[9]/gmd:MD_Keywords[1]/gmd:thesaurusName[1]`





### Title xpath: 



```

/gmi:MI_Metadata/gmd:identificationInfo[1]/gmd:MD_DataIdentification[1]/gmd:descriptiveKeywords[9]/gmd:MD_Keywords[1]/gmd:thesaurusName[1]/gmd:CI_Citation[1]/gmd:title[1]/gco:CharacterString[1]

```



### Keywords xpath

```

/gmi:MI_Metadata/gmd:identificationInfo[1]/gmd:MD_DataIdentification[1]/gmd:topicCategory[1]/gmd:MD_TopicCategoryCode[1]

```



```

/gmi:MI_Metadata/gmd:identificationInfo[1]/gmd:MD_DataIdentification[1]/gmd:descriptiveKeywords[1]

```











## Examples:

IDEAL SOURCE: Thesaurus Name, anchor



```[xml]

<gmd:descriptiveKeywords>

    <gmd:MD_Keywords>

        <gmd:keyword xmlns:gmx="http://www.isotc211.org/2005/gmx"

            xmlns:xlink="http://www.w3.org/1999/xlink">

            <gmx:Anchor xlink:href="http://accession.nodc.noaa.gov/9500089" xlink:actuate="onRequest">9500089</gmx:Anchor>

        </gmd:keyword>

        <gmd:thesaurusName>

            <gmd:CI_Citation>

                <gmd:title>

                    <gco:CharacterString>NODC ACCESSION NUMBER</gco:CharacterString>

                </gmd:title>

                <gmd:date>

                    <gmd:CI_Date>

                        <gmd:date>

                            <gco:Date>2013-03-19</gco:Date>

                        </gmd:date>

                        <gmd:dateType>

                            <gmd:CI_DateTypeCode codeList="http://www.isotc211.org/2005/resources/Codelist/gmxCodelists.xml#CI_DateTypeCode" codeListValue="publication" codeSpace="002">publication</gmd:CI_DateTypeCode>

                        </gmd:dateType>

                    </gmd:CI_Date>

                </gmd:date>

            </gmd:CI_Citation>

        </gmd:thesaurusName>

    </gmd:MD_Keywords>

</gmd:descriptiveKeywords>

```



### ANCHOR:

```[XML]

<gmd:keyword xmlns:gmx="http://www.isotc211.org/2005/gmx"

    xmlns:xlink="http://www.w3.org/1999/xlink">

    <gmx:Anchor xlink:href="http://accession.nodc.noaa.gov/9500089" xlink:actuate="onRequest">9500089</gmx:Anchor>

</gmd:keyword>



```





					



