---
description: >-
  Creatives are the visual elements of your campaign. You can have several
  creative associated to one campaign.
---

# Creative

## Properties description

<table><thead><tr><th width="194">Property</th><th width="107.33333333333331">Type</th><th>Description</th></tr></thead><tbody><tr><td>id</td><td>Integer</td><td>Creative unique identification.</td></tr><tr><td>name</td><td>String</td><td>Creative name defined par user during creation</td></tr><tr><td>created_at</td><td>Datetime</td><td>Creation date of the creative, GMT timezone</td></tr><tr><td>updated_at</td><td>Datetime</td><td>Last update of the creative, GMT timezone</td></tr><tr><td>deleted_at</td><td>Datetime</td><td>Field used for softdeleting the campaign. This property is null for active creative.</td></tr></tbody></table>

## Get creative

{% swagger method="get" path="/creatives/{creative_id}" baseUrl="https://api.smartxsp.io" summary="Get campaign details" expanded="true" %}
{% swagger-description %}
Retrieves campaign details.
{% endswagger-description %}

{% swagger-parameter in="header" name="Authorization" required="true" %}
The Bearer token you get during login process.
{% endswagger-parameter %}

{% swagger-parameter in="path" name="creative_id" required="true" %}
The numeric id of the creative
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="Detail of a creative" %}
{% code overflow="wrap" lineNumbers="true" %}
```json
{
    "success":true,
    "data":{
        "id":1,
        "name":"My first creative",
        "created_at":"2023-04-26T15:24:05.000000Z",
        "updated_at":"2023-05-02T12:37:06.000000Z",
        "deleted_at":null
    },
    "message":"Creative retrieved successfully."
}
```
{% endcode %}
{% endswagger-response %}
{% endswagger %}

## Create creative

{% swagger method="post" path="/creatives/" baseUrl="https://api.smartxsp.io" summary="Create a new creative" expanded="true" %}
{% swagger-description %}
Create a new creative associated to a campaign with template initializationCreate a new creative associated to a campaign based on JSON string
{% endswagger-description %}

{% swagger-parameter in="header" name="Authorization" required="true" %}
The Bearer token you get during login process.
{% endswagger-parameter %}

{% swagger-parameter in="query" name="campaign_id" type="Integer" required="true" %}
The campaign associated to the creative.
{% endswagger-parameter %}

{% swagger-parameter in="query" name="name" required="true" %}
The campaign name
{% endswagger-parameter %}

{% swagger-parameter in="query" name="sub_product_id" type="Integer" required="true" %}
Id of the Sub Product, it's the template used to create the visual. It must be a sub product of the product defined in [the campaign.](campaign.md#create-campaign)
{% endswagger-parameter %}

{% swagger-parameter in="query" name="json_template" type="String" required="false" %}
The JSON stream used to create the visual part of the creative. Please look at [samples below](creative.md#json-templates-samples).
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="Detail of a campaign" %}

{% endswagger-response %}
{% endswagger %}

## Update creative

{% swagger method="patch" path="/creatives/{creative_id}" baseUrl="https://api.smartxsp.io" summary="Update an existing creative" expanded="true" %}
{% swagger-description %}
Generaly used to regenerate the visual part of the creative based on the JSON string.
{% endswagger-description %}

{% swagger-parameter in="path" name="creative_id" type="Integer" %}
The ID of the creative to update
{% endswagger-parameter %}

{% swagger-parameter in="query" name="name" %}
The new name of the creative, no modification if null or empty
{% endswagger-parameter %}

{% swagger-parameter in="query" name="json_template" %}
The new version of the JSON stream used to create the visual part of the creative.
{% endswagger-parameter %}
{% endswagger %}

## JSON Templates samples

### Halfpage Vertical Products

```json
{
    "inputs":{    
        "company":{
            "value":"My super customer"
        },
        "company_sub":{
            "value":"Whatever you want"
        },
        "company_logo":{
            "media_url":"https://cdn.edgequery.io/prd/creatives/7625/5/company_logo_80.jpg"
        },
        "cta_text":{
            "value":"Read more"
        },
        "slides":{
            "elements":{
                "idx1":{
                    "slide_title":{
                        "value":"My first product"
                    },
                    "slide_text":{
                        "value":"Maybe the brand"
                    },
                 "slide_subtext":{
                        "value":"Long description<br/>On many lines."
                    },
                    "slide_price":{
                        "value":349
                    },
                    "slide_price_unit":{
                        "value":"Sub price text"
                    },
                    "slide_image":{
                        "media_url":"https://cdn.edgequery.io/prd/creatives/7625/4/slide_300x300_1.jpg"
                    },
                    "slide_background":{
                        "value":"#FF0000"
                    },
                    "slide_color":{
                        "value":"#FFFFFF"
                    }
                },
                "idx2":{
                    "slide_title":{
                        "value":"My second product"
                    },
                    "slide_text":{
                        "value":"Maybe the brand"
                    },
                    "slide_subtext":{
                        "value":"Long description<br/>On many lines."
                    },
                    "slide_price":{
                        "value":49.95
                    },
                    "slide_price_unit":{
                        "value":"Sub price text"
                    },
                    "slide_image":{
                        "media_url":"https://cdn.edgequery.io/prd/creatives/7625/7/slide_300x300_2.jpg"
                    },
                    "slide_background":{
                        "value":"#FFFF00"
                    },
                    "slide_color":{
                        "value":"#000000"
                    }
                },
                "idx3":{
                    "slide_title":{
                        "value":"My last product"
                    },
                    "slide_text":{
                        "value":"Maybe the brand"
                    },
                    "slide_subtext":{
                        "value":"Long description<br/>On many lines."
                    },
                    "slide_price":{
                        "value":199.99
                    },
                    "slide_price_unit":{
                        "value":"Sub price text"
                    },
                    "slide_image":{
                        "media_url":"https://cdn.edgequery.io/prd/creatives/7625/9/slide_300x300_4.png"
                    },
                    "slide_background":{
                        "value":"#FFFF00"
                    },
                    "slide_color":{
                        "value":"#000000"
                    }
                }
            }
        }
    },
    "url":"https://oursblanc.io",
    "pixel":"https://oursblanc.io/pixel",
    "name":"Custom name of my creative"
}
```
