---
description: >-
  Creatives are the visual elements of your campaign. You can have several
  creative associated to one campaign.
---

# Creative

## Properties description

<table><thead><tr><th width="194">Property</th><th width="107.33333333333331">Type</th><th>Description</th></tr></thead><tbody><tr><td>id</td><td>Integer</td><td>Creative unique identification.</td></tr><tr><td>name</td><td>String</td><td>Creative name defined par user during creation</td></tr><tr><td>created_at</td><td>Datetime</td><td>Creation date of the creative, GMT timezone</td></tr><tr><td>updated_at</td><td>Datetime</td><td>Last update of the creative, GMT timezone</td></tr><tr><td>deleted_at</td><td>Datetime</td><td>Field used for softdeleting the campaign. This property is null for active creative.</td></tr></tbody></table>

## Get creative

## Get campaign details

<mark style="color:blue;">`GET`</mark> `https://my.smartxsp.io/api/creatives/{creative_id}`

Retrieves campaign details.

#### Path Parameters

| Name                                           | Type   | Description                    |
| ---------------------------------------------- | ------ | ------------------------------ |
| creative\_id<mark style="color:red;">\*</mark> | String | The numeric id of the creative |

#### Headers

| Name                                            | Type   | Description                                    |
| ----------------------------------------------- | ------ | ---------------------------------------------- |
| Authorization<mark style="color:red;">\*</mark> | String | The Bearer token you get during login process. |

{% tabs %}
{% tab title="200: OK Detail of a creative" %}
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
{% endtab %}
{% endtabs %}

## Create creative

## Create a new creative

<mark style="color:green;">`POST`</mark> `https://my.smartxsp.io/api/creatives/`

Create a new creative associated to a campaign with template initializationCreate a new creative associated to a campaign based on JSON string

#### Query Parameters

| Name                                               | Type    | Description                                                                                                                                                         |
| -------------------------------------------------- | ------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| campaign\_id<mark style="color:red;">\*</mark>     | Integer | The campaign associated to the creative.                                                                                                                            |
| name<mark style="color:red;">\*</mark>             | String  | The campaign name                                                                                                                                                   |
| json\_template                                     | String  | The JSON stream used to create the visual part of the creative. Please look at [samples below](creative.md#json-templates-samples).                                 |
| sub\_product\_id<mark style="color:red;">\*</mark> | Integer | Id of the Sub Product, it's the template used to create the visual. It must be a sub product of the product defined in [the campaign.](campaign.md#create-campaign) |

#### Headers

| Name                                            | Type   | Description                                    |
| ----------------------------------------------- | ------ | ---------------------------------------------- |
| Authorization<mark style="color:red;">\*</mark> | String | The Bearer token you get during login process. |

{% tabs %}
{% tab title="200: OK Detail of a campaign" %}

{% endtab %}
{% endtabs %}

## Update creative

## Update an existing creative

<mark style="color:purple;">`PATCH`</mark> `https://my.smartxsp.io/api/creatives/{creative_id}`

Generaly used to regenerate the visual part of the creative based on the JSON string.

#### Path Parameters

| Name         | Type    | Description                      |
| ------------ | ------- | -------------------------------- |
| creative\_id | Integer | The ID of the creative to update |

#### Query Parameters

| Name           | Type   | Description                                                                        |
| -------------- | ------ | ---------------------------------------------------------------------------------- |
| name           | String | The new name of the creative, no modification if null or empty                     |
| json\_template | String | The new version of the JSON stream used to create the visual part of the creative. |

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
