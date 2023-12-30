---
description: The user profile endpoint
---

# 👥 Users

This users endpoint allows you to retrieve data about Digitomize's users.&#x20;

You can get the following data about a Digitomize user:

* personal details
* social links
* ratings
* github

{% swagger method="get" path="" baseUrl="https://www.v2api.digitomize.com /user/signup" summary="Retrieve user data" expanded="true" %}
{% swagger-description %}
This endpoint allows you to create a new user in the Digitomize platform
{% endswagger-description %}

{% swagger-parameter in="path" name="username" type="String" required="true" %}
Digitomize username
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="User found" %}

{% endswagger-response %}

{% swagger-response status="404: Not Found" description="User not found" %}
```json
{
    "message":"User not found",
    "error":"User not found"
}
```
{% endswagger-response %}

{% swagger-response status="500: Internal Server Error" description="Server Error" %}

{% endswagger-response %}
{% endswagger %}

For example,

The request URL is [https://www.v2api.digitomize.com/user/profile/priyanshutrivedi818](https://www.v2api.digitomize.com/user/profile/priyanshutrivedi818)

The response will be:

```json
{
    "personal_data": {
        "username": "priyanshutrivedi818",
        "name": "Priyanshu Trivedi",
        "picture": "https://lh3.googleusercontent.com/a/ACg8ocKHINLEGHdSrFO_D1TqPMqX3UhLKuYfYKNCN5QCiU-3=s96-c",
        "email_verified": true,
        "email": "priyanshutrivedi818@gmail.com",
        "bio": null,
        "dateOfBirth": null,
        "phoneNumber": null,
        "role": 1,
        "skills": []
    },
    "github": {
        "data": null
    },
    "social": {
        "linkedin": null,
        "instagram": null,
        "twitter": null
    },
    "ratings": {
        "digitomize_rating": 1667,
        "codechef": {
            "username": "priyanshu_triv",
            "rating": 2005,
            "attendedContestsCount": 53,
            "badge": "5 star",
            "fetchTime": 1703946843104
        },
        "leetcode": {
            "username": "priyanshu_triv",
            "rating": 2060,
            "attendedContestsCount": 28,
            "badge": "Knight",
            "fetchTime": 1703946843104
        },
        "codeforces": {
            "username": null,
            "rating": 1667,
            "attendedContestsCount": null,
            "badge": null,
            "fetchTime": 1703946843104
        }
    }
}
```

Feel free to use this API. If you have any issues, you can raise it in [our Discord channel](https://discord.com/invite/bsbBytBqBc).
