---
description: The contests endpoint and how you can use it
---

# Contests

The Digitomize API allows users to get details about programming contests. This endpoint allows you to:

* [get all the contests available](contests.md#all-contests)
* [get all contests hosted by a specific host](contests.md#specific-host)
* [get all contests hosted by multiple hosts](contests.md#multiple-hosts)
* [get a specific contest](contests.md#specific-contest)

{% swagger method="get" path=" " baseUrl="https://www.v2api.digitomize.com/contests " summary="All Contests" fullWidth="false" expanded="true" %}
{% swagger-description %}
This endpoint allows you to get all the programming contests available in  Digitomize
{% endswagger-description %}

{% swagger-response status="200: OK" description="Successful Request" %}
This is the response you will get when your request is successful.


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

The response body has a total property and a results property which is an array of objects containing the contests. It will have the following format:

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

{% swagger method="get" path=" " baseUrl="https://www.v2api.digitomize.com/contests" summary="Specific host" expanded="true" %}
{% swagger-description %}
This API route allows you to get all the programming contests available in  Digitomize by a specific host
{% endswagger-description %}

{% swagger-parameter in="query" name="host" type="String" %}
One of the available event hosts
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

{% hint style="info" %}
The available event hosts in Digitomize include:&#x20;

* geeksforgeeks
* codechef
* codeforces
* atcoder
* codingninjas
* leetcode
{% endhint %}

In this example, we will get programming contests by GeeksForGeeks.

The request URL is [https://www.v2api.digitomize.com/contests?host=geeksforgeeks](https://www.v2api.digitomize.com/contests?host=geeksforgeeks)

You will get the following JSON object as a response.

```json
{
    "total": 6,
    "results": [
        {
            "host": "geeksforgeeks",
            "name": "Bi-Wizard School Coding Tournament 22.0",
            "vanity": "bi-wizard-school-coding-tournament-220",
            "url": "https://practice.geeksforgeeks.org/contest/bi-wizard-school-coding-tournament-220",
            "startTimeUnix": 1703593800,
            "duration": 90
        },
        {
            "host": "geeksforgeeks",
            "name": "GFG Weekly Coding Contest - 135",
            "vanity": "gfg-weekly-coding-contest-135",
            "url": "https://practice.geeksforgeeks.org/contest/gfg-weekly-coding-contest-135",
            "startTimeUnix": 1704029400,
            "duration": 90
        },
        {
            "host": "geeksforgeeks",
            "name": "GFG Weekly Coding Contest - 136",
            "vanity": "gfg-weekly-coding-contest-136",
            "url": "https://practice.geeksforgeeks.org/contest/gfg-weekly-coding-contest-136",
            "startTimeUnix": 1704634200,
            "duration": 90
        },
        {
            "host": "geeksforgeeks",
            "name": "GATE CS 2024 - All India Mock 2",
            "vanity": "all-india-mock-gate-csit-ii",
            "url": "https://practice.geeksforgeeks.org/contest/all-india-mock-gate-csit-ii",
            "startTimeUnix": 1705775400,
            "duration": 1440
        },
        {
            "host": "geeksforgeeks",
            "name": "Job-A-Thon 29 Hiring Challenge",
            "vanity": "job-a-thon-29-hiring-challenge",
            "url": "https://practice.geeksforgeeks.org/contest/job-a-thon-29-hiring-challenge",
            "startTimeUnix": 1705847400,
            "duration": 150
        },
        {
            "host": "geeksforgeeks",
            "name": "GATE Data Science and Artificial Intelligence 2 - All India Mock 2024",
            "vanity": "all-india-mock-gate-mlai-ii",
            "url": "https://practice.geeksforgeeks.org/contest/all-india-mock-gate-mlai-ii",
            "startTimeUnix": 1706380200,
            "duration": 2880
        }
    ]
}
```

You can test this endpoint using any of the [available event hosts](contests.md#event-hosts-in-digitomize).

{% swagger method="get" path=" " baseUrl="https://www.v2api.digitomize.com/contests" summary="Multiple hosts" expanded="true" %}
{% swagger-description %}
This API route allows you to get all the programming contests available in  Digitomize by multiple event hosts
{% endswagger-description %}

{% swagger-parameter in="query" name="host" type="String" %}
Two or more of the available event hosts
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

{% hint style="info" %}
The available event hosts in Digitomize include:&#x20;

* geeksforgeeks
* codechef
* codeforces
* atcoder
* codingninjas
* leetcode
{% endhint %}

In this example, you will get all the programming contests hosted by GeeksForGeeks and CodeChef.

The request URL will be [https://www.v2api.digitomize.com/contests?host=geeksforgeeks,codechef](https://www.v2api.digitomize.com/contests?host=geeksforgeeks,codechef)

You will get the following JSON object as the response:&#x20;

```json
{
    "total": 12,
    "results": [
        {
            "host": "geeksforgeeks",
            "name": "Bi-Wizard School Coding Tournament 22.0",
            "vanity": "bi-wizard-school-coding-tournament-220",
            "url": "https://practice.geeksforgeeks.org/contest/bi-wizard-school-coding-tournament-220",
            "startTimeUnix": 1703593800,
            "duration": 90
        },
        {
            "host": "codechef",
            "name": "Starters 114",
            "vanity": "start114",
            "url": "https://www.codechef.com/START114",
            "startTimeUnix": 1703687400,
            "duration": 120
        },
        {
            "host": "geeksforgeeks",
            "name": "GFG Weekly Coding Contest - 135",
            "vanity": "gfg-weekly-coding-contest-135",
            "url": "https://practice.geeksforgeeks.org/contest/gfg-weekly-coding-contest-135",
            "startTimeUnix": 1704029400,
            "duration": 90
        },
        {
            "host": "codechef",
            "name": "Starters 115",
            "vanity": "start115",
            "url": "https://www.codechef.com/START115",
            "startTimeUnix": 1704292200,
            "duration": 120
        },
        {
            "host": "geeksforgeeks",
            "name": "GFG Weekly Coding Contest - 136",
            "vanity": "gfg-weekly-coding-contest-136",
            "url": "https://practice.geeksforgeeks.org/contest/gfg-weekly-coding-contest-136",
            "startTimeUnix": 1704634200,
            "duration": 90
        },
        {
            "host": "codechef",
            "name": "Starters 116",
            "vanity": "start116",
            "url": "https://www.codechef.com/START116",
            "startTimeUnix": 1704897000,
            "duration": 120
        },
        {
            "host": "codechef",
            "name": "Starters 117",
            "vanity": "start117",
            "url": "https://www.codechef.com/START117",
            "startTimeUnix": 1705501800,
            "duration": 120
        },
        {
            "host": "geeksforgeeks",
            "name": "GATE CS 2024 - All India Mock 2",
            "vanity": "all-india-mock-gate-csit-ii",
            "url": "https://practice.geeksforgeeks.org/contest/all-india-mock-gate-csit-ii",
            "startTimeUnix": 1705775400,
            "duration": 1440
        },
        {
            "host": "geeksforgeeks",
            "name": "Job-A-Thon 29 Hiring Challenge",
            "vanity": "job-a-thon-29-hiring-challenge",
            "url": "https://practice.geeksforgeeks.org/contest/job-a-thon-29-hiring-challenge",
            "startTimeUnix": 1705847400,
            "duration": 150
        },
        {
            "host": "codechef",
            "name": "Starters 118",
            "vanity": "start118",
            "url": "https://www.codechef.com/START118",
            "startTimeUnix": 1706106600,
            "duration": 120
        },
        {
            "host": "geeksforgeeks",
            "name": "GATE Data Science and Artificial Intelligence 2 - All India Mock 2024",
            "vanity": "all-india-mock-gate-mlai-ii",
            "url": "https://practice.geeksforgeeks.org/contest/all-india-mock-gate-mlai-ii",
            "startTimeUnix": 1706380200,
            "duration": 2880
        },
        {
            "host": "codechef",
            "name": "Starters 119",
            "vanity": "start119",
            "url": "https://www.codechef.com/START119",
            "startTimeUnix": 1706711400,
            "duration": 120
        }
    ]
}
```

You can add more event hosts from the [list of available hosts](contests.md#event-hosts-in-digitomize).

{% swagger method="get" baseUrl="https://www.v2api.digitomize.com/contests" summary="Specific contest" expanded="true" path=" " %}
{% swagger-description %}
This API route allows you to get a specific programming contest based on the vanity string
{% endswagger-description %}

{% swagger-parameter in="query" name="vanity" type="String" %}
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

In this example, you will get details about a weekend contest on GeeksForGeeks.

The request URL will be [https://www.v2api.digitomize.com/contests?vanity=weekend-contest-106](https://www.v2api.digitomize.com/contests?vanity=weekend-contest-106)

You will get the following JSON object as a response:

```json
{
    "total": 1,
    "results": [
        {
            "host": "codingninjas",
            "name": "Weekend Contest 106",
            "vanity": "weekend-contest-106",
            "url": "https://codingninjas.com/studio/contests/weekend-contest-106",
            "startTimeUnix": 1703941200,
            "duration": 90
        }
    ]
}
```
