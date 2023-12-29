---
description: This endpoint allows you to access Digitomize's leaderboard
---

# 🏆 Leaderboard

You can use the endpoint to perform the following queries:

* [Retrieve the leaderboard](leaderboard.md#the-leaderboard)
* [Filter the leaderboard by platform](leaderboard.md#filter-by-platform)
* [Filter the leaderboard by username](leaderboard.md#filter-by-username)

This endpoint gives you all the details on the leaderboard including,

* total number of users
* top 3 users&#x20;
* number of users per page
* current page
* total number of pages
* &#x20;leaderboard

{% swagger method="get" path=" " baseUrl="https://www.v2api.digitomize.com/user/leaderboard" summary="The leaderboard" expanded="true" %}
{% swagger-description %}
This endpoint retrieves the whole leaderboard
{% endswagger-description %}

{% swagger-response status="200: OK" description="Successful data retrieval" %}

{% endswagger-response %}

{% swagger-response status="500: Internal Server Error" description="Server Error" %}

{% endswagger-response %}
{% endswagger %}

An example of the response is:

```json
{
    "total_users": 70,
    "top3": [
        {
            "username": "coderdhanraj",
            "picture": "https://res.cloudinary.com/dsazw0r59/image/upload/ar_1.0,c_fill,g_face/f_auto/r_max/v1701666794/users/bqvYU117aieXrUN8tYS4mky8act1.jpg",
            "name": "Dhanraj Chaurasia",
            "codechef": 2035,
            "leetcode": 2478,
            "codeforces": 1905,
            "digitomize_rating": 1905,
            "platform_rating": null
        },
        ...
    ],
    "users_in_page": 5,
    "total_pages": 14,
    "current_page": 1,
    "leaderboard": [
        {
            "username": "priyanshutrivedi818",
            "picture": "https://lh3.googleusercontent.com/a/ACg8ocKHINLEGHdSrFO_D1TqPMqX3UhLKuYfYKNCN5QCiU-3=s96-c",
            "name": "Priyanshu Trivedi",
            "codechef": 2005,
            "leetcode": 2060,
            "codeforces": 1667,
            "digitomize_rating": 1667,
            "platform_rating": null
        },
        ...
    ]
}
```

{% swagger method="get" path=" " baseUrl="https://www.v2api.digitomize.com/user/leaderboard" summary="Filter by platform" expanded="true" %}
{% swagger-description %}
This endpoint retrieves the leaderboard sorted based on a specified platform
{% endswagger-description %}

{% swagger-parameter in="query" name="platform" type="String" %}
One of the supported platforms
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="Successful data retrieval" %}

{% endswagger-response %}

{% swagger-response status="500: Internal Server Error" description="Server Error" %}

{% endswagger-response %}
{% endswagger %}

The response will only include the leaderboard sorted by ratings based on the platform.&#x20;

{% hint style="info" %}
The available platforms in Digitomize include:&#x20;

* geeksforgeeks
* codechef
* codeforces
* atcoder
* codingninjas
* leetcode
{% endhint %}

Here is an example of the response:

The leaderboard is filtered by the leetcode platform

```json
{
    "total_users": 56,
    "top3": [
        {
            "username": "Mukul_Rawat",
            "picture": "https://res.cloudinary.com/dsazw0r59/image/upload/ar_1.0,c_fill,g_face/f_auto/r_max/v1702761621/users/rA3v7v5sZ8QmkzI3UNprZlx9e1r1.png",
            "name": "Mukul Rawat",
            "codechef": 2052,
            "leetcode": 2481,
            "codeforces": 1709,
            "digitomize_rating": 1724.2949999999998,
            "platform_rating": 2481
        },
        ...
    ],
    "users_in_page": 5,
    "total_pages": 11,
    "current_page": 1,
    "leaderboard": [
        {
            "username": "rahul1995",
            "picture": "https://lh3.googleusercontent.com/a/ACg8ocJV0_ycmW98qj9MUhSEbMZUtDv1buXrn4qkjN1THVyyu50=s96-c",
            "name": "Rahul JAIN",
            "codechef": 1768,
            "leetcode": 2326,
            "codeforces": 1186,
            "digitomize_rating": 1616.57,
            "platform_rating": 2326
        },
        ...
    ]
}
```

{% swagger method="get" path=" " baseUrl="https://www.v2api.digitomize.com/user/leaderboard" summary="Filter by username" expanded="true" %}
{% swagger-description %}
This endpoint retrieves an individual user's data on the leaderboard
{% endswagger-description %}

{% swagger-parameter in="query" name="username" type="String" %}
The username
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="Successful data retrieval" %}

{% endswagger-response %}

{% swagger-response status="500: Internal Server Error" description="Server Error" %}

{% endswagger-response %}
{% endswagger %}

Here is an example where we search for Priyanshu's details in the leaderboard.

```json
{
    "user_position": 4,
    "ratings": {
        "codechef": 2005,
        "leetcode": 2060,
        "codeforces": 1667,
        "digitomize_rating": 1667,
        "platform_rating": null
    }
}
```

Feel free to use this API. If you have any issues, you can raise it in [our Discord channel](https://discord.com/invite/bsbBytBqBc).
