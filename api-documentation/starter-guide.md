# Starter Guide

## Authentification

## Identification on the SmartXSP platform

<mark style="color:green;">`POST`</mark> `https://my.smartxsp.io/api/login`

This method will allow you to identify yourself on the SmartXSP platform. A dedicated service account / user account is generally used to perform these operations. If you do not have such an account, contact your sales contact at OursBlanc or contact@oursblanc.io directly.

At the end of this operation, you will obtain a token allowing you to execute all the following requests.

#### Query Parameters

| Name                                       | Type   | Description                               |
| ------------------------------------------ | ------ | ----------------------------------------- |
| email<mark style="color:red;">\*</mark>    | String | The email address of your service account |
| password<mark style="color:red;">\*</mark> | String | The password of your service account      |

{% tabs %}
{% tab title="200: OK Identification accepted" %}
{% code overflow="wrap" lineNumbers="true" %}
```json
{
    "success":true,
    "data":{
        "token":"your_token",
        "name":"user_name"
    },
    "message":"User login successfully."
}
```
{% endcode %}
{% endtab %}
{% endtabs %}
