# Account

## Properties description

<table><thead><tr><th width="194">Property</th><th width="107.33333333333331">Type</th><th>Description</th></tr></thead><tbody><tr><td>id</td><td>Integer</td><td>Account unique identification.</td></tr><tr><td>name</td><td>String</td><td>Account name defined by user during creation</td></tr><tr><td>owner_account_id</td><td>Integer</td><td>Id of the owner account or parent account generally used for agency customer campaigns.</td></tr><tr><td>created_at</td><td>Datetime</td><td>Creation date of the account, GMT timezone</td></tr><tr><td>updated_at</td><td>Datetime</td><td>Last update of the account, GMT timezone</td></tr><tr><td>deleted_at</td><td>Datetime</td><td>Field used for softdeleting the account. This property is null for active account.</td></tr></tbody></table>

## Search accounts

{% swagger method="get" path="/accounts" baseUrl="https://api.smartxsp.io" summary="Search accounts" expanded="true" %}
{% swagger-description %}
Allows you to retrieve the list of accounts associated to the connected user. :warning: Please note that the list is limited to the last 1000 accounts.
{% endswagger-description %}

{% swagger-parameter in="header" name="Authorization" required="true" %}
The Bearer token you get during login process.
{% endswagger-parameter %}

{% swagger-parameter in="query" name="search" %}
Search string filtering on account name.
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="List of accounts" %}
{% code overflow="wrap" lineNumbers="true" %}
```json
{
    "success":true,
    "data":{
        "user":{
            "id":1,
            "name":"John Doe",
            "email":"johndoe@smartxsp.io",
            "account_id":1,
            "account":{
                "id":1,
                "name":"Account Name",
                "account_type":"agency"
            }
        },
        "accounts":[
            {
                "id":1,
                "name":"First account"
            },
            {
                "id":2,
                "name":"Second account"
            }
        ]
    },
    "message":"Accounts retrieved successfully."
}
```
{% endcode %}
{% endswagger-response %}
{% endswagger %}

## Get account

{% swagger method="get" path="/accounts/{account_id}" baseUrl="https://api.smartxsp.io" summary="Get account details" expanded="true" %}
{% swagger-description %}
Retrieves account details.
{% endswagger-description %}

{% swagger-parameter in="header" name="Authorization" required="true" %}
The Bearer token you get during login process.
{% endswagger-parameter %}

{% swagger-parameter in="path" name="account_id" required="true" %}
The numeric id of the campaign
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="Detail of a account" %}
{% code overflow="wrap" lineNumbers="true" %}
```json
{
    "success":true,
    "data":{
        "id":1,
        "name":"My first account",
        "owner_account_id":21,
        "created_at":"2023-04-26T15:24:05.000000Z",
        "updated_at":"2023-05-02T12:37:06.000000Z",
        "deleted_at":null
    },
    "message":"Account retrieved successfully."
}
```
{% endcode %}
{% endswagger-response %}
{% endswagger %}

## Create account

{% swagger method="post" path="/accounts" baseUrl="https://api.smartxsp.io" summary="Create a new account" expanded="true" %}
{% swagger-description %}
Create a new account.
{% endswagger-description %}

{% swagger-parameter in="header" name="Authorization" required="true" %}
The Bearer token you get during login process.
{% endswagger-parameter %}

{% swagger-parameter in="query" name="name" required="true" %}
The account name
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="Detail of a campaign" %}
{% code overflow="wrap" lineNumbers="true" %}
```json
{
    "success":true,
    "data":{
        "id":1,
        "name":"My first campagn",
        "state":"running",
        "account_id":2216,
        "owner_account_id":21,
        "product_id":1,
        "start_at":"2023-04-25T22:00:00.000000Z",
        "stop_at":"2023-05-12T21:59:00.000000Z",
        "budget":24000,
        "sell_price":"20.00000",
        "buy_price":"12.00000",
        "impressions":11397,
        "visible_impressions":7938,
        "clicks":57,
        "exposure_time":140122,
        "created_at":"2023-04-26T15:24:05.000000Z",
        "updated_at":"2023-05-02T12:37:06.000000Z",
        "deleted_at":null
    },
    "message":"Campaign retrieved successfully."
}
```
{% endcode %}
{% endswagger-response %}
{% endswagger %}

