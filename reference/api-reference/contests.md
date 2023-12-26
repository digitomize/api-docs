---
description: >-
  In this page, you will learn how to use the Digitomize API to get all
  programming contests
---

# Contests

The following queries are covered in this page:

* GET all contests
* GET all contests by a specific host
* GET a specific contest based on the vanity string

Let's get started.

{% swagger method="get" path="" baseUrl="https://www.v2api.digitomize.com/contests" summary="Get All The Contests" %}
{% swagger-description %}
This API route allows you to get all the programming contests available in  Digitomize
{% endswagger-description %}

{% swagger-response status="200: OK" description="Successful Request" %}
This is the response you will get when your request is successful.

The response body will have the following format:

```json
{
    "total" : integer,
    "results": [
        {
            "host": string,
            "name": string,
            "vanity": string,
            "url": string,
            "startTimeUnix": timestamp,
            "duration": integer
        }
    ]
}
```


{% endswagger-response %}

{% swagger-response status="500: Internal Server Error" description="Server Error" %}
```json
// Response Body
{
    "error": string,
    "message": string
}
```
{% endswagger-response %}
{% endswagger %}

{% swagger method="get" path="" baseUrl="https://www.v2api.digitomize.com/contests" summary="Get all the contests by a specific host" %}
{% swagger-description %}
This API route allows you to get all the programming contests available in  Digitomize by a specific host
{% endswagger-description %}

{% swagger-parameter in="query" name="host" %}
Specify an event host
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="Successful Request" %}
This is the response you will get when your request is successful.

The response body will have the following format:

```json
{
    "total" : integer,
    "results": [
        {
            "host": string,
            "name": string,
            "vanity": string,
            "url": string,
            "startTimeUnix": timestamp,
            "duration": integer
        }
    ]
}
```


{% endswagger-response %}

{% swagger-response status="500: Internal Server Error" description="Server Error" %}
```json
// Response Body
{
    "error": string,
    "message": string
}
```
{% endswagger-response %}
{% endswagger %}

{% swagger method="get" path="" baseUrl="https://www.v2api.digitomize.com/contests" summary="Get a specific contest" %}
{% swagger-description %}
This API route allows you to get all the programming contests available in  Digitomize
{% endswagger-description %}

{% swagger-parameter in="query" name="vanity" %}
A unique string for an event
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="Successful Request" %}
This is the response you will get when your request is successful.

The response body will have the following format:

```json
{
    "total" : integer,
    "results": [
        {
            "host": string,
            "name": string,
            "vanity": string,
            "url": string,
            "startTimeUnix": timestamp,
            "duration": integer
        }
    ]
}
```


{% endswagger-response %}

{% swagger-response status="500: Internal Server Error" description="Server Error" %}
```json
// Response Body
{
    "error": string,
    "message": string
}
```
{% endswagger-response %}
{% endswagger %}
