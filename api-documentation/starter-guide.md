# Starter Guide

## Authentification

{% swagger method="post" path="/login" baseUrl="https://api.smartxsp.io" summary="Identification on the SmartXSP platform" expanded="true" %}
{% swagger-description %}
This method will allow you to identify yourself on the SmartXSP platform. A dedicated service account / user account is generally used to perform these operations. If you do not have such an account, contact your sales contact at OursBlanc or contact@oursblanc.io directly.

At the end of this operation, you will obtain a token allowing you to execute all the following requests.
{% endswagger-description %}

{% swagger-parameter in="query" name="email" required="true" %}
The email address of your service account
{% endswagger-parameter %}

{% swagger-parameter in="query" name="password" required="true" %}
The password of your service account
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="Identification accepted" %}
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
{% endswagger-response %}
{% endswagger %}
