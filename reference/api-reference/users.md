---
description: The users endpoint and how you can use it
---

# 👥 Users

The users endpoint allows you to make the following queries:

* [creating a new user](users.md#create-a-new-user)
* updating a user's details
* retrieve a user's dashboard
* retrieve a user's profile

{% hint style="info" %}
**Good to know:** All the methods shown below are synced to an example Swagger file URL and are kept up to date automatically with changes to the API.
{% endhint %}

## User actions

{% swagger method="post" path=" " baseUrl="https://www.v2api.digitomize.com /user/signup" summary="Create a new user" %}
{% swagger-description %}
This endpoint allows you to create a new user in the Digitomize platform
{% endswagger-description %}

{% swagger-parameter in="body" %}

{% endswagger-parameter %}
{% endswagger %}

{% swagger src="https://petstore.swagger.io/v2/swagger.json" path="/user/logout" method="get" %}
[https://petstore.swagger.io/v2/swagger.json](https://petstore.swagger.io/v2/swagger.json)
{% endswagger %}

## Creating users

{% swagger src="https://petstore.swagger.io/v2/swagger.json" path="/user/createWithList" method="post" %}
[https://petstore.swagger.io/v2/swagger.json](https://petstore.swagger.io/v2/swagger.json)
{% endswagger %}

{% swagger src="https://petstore.swagger.io/v2/swagger.json" path="/user/createWithArray" method="post" %}
[https://petstore.swagger.io/v2/swagger.json](https://petstore.swagger.io/v2/swagger.json)
{% endswagger %}
