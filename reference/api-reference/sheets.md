# Sheets

## Get All Contests

{% swagger baseUrl="https://v2api.digitomize.com" method="post" path="/sheets" summary="Get all sheets" %}
{% swagger-description %}
This endpoint allows you to retrieve information about various programming contests. You can filter contests based on the `host` and `vanity` query parameters.
{% endswagger-description %}

{% swagger-response status="200" description="OK" %}
```json
{
    "count": 1,
    "sheets": [
        {
            "_id": "656cd731ef98a08ce82edbb3",
            "name": "New Sheet",
            "s_id": "S_NEW",
            "desc": "This is a new sheet for testing.",
            "questions": [
                {
                    "_id": "657348abd09c5305512955f4",
                    "q_id": "101",
                    "name": "Sum of Two Numbers",
                    "difficulty": "easy",
                    "topics": [
                        "Math",
                        "Addition"
                    ],
                    "__v": 0
                },
                {
                    "_id": "657348abd09c5305512955f5",
                    "q_id": "102",
                    "name": "Palindrome Check",
                    "difficulty": "medium",
                    "topics": [
                        "String",
                        "Palindrome"
                    ],
                    "__v": 0
                },
                {
                    "_id": "657348abd09c5305512955f6",
                    "q_id": "123",
                    "name": "Factorial Calculation",
                    "difficulty": "hard",
                    "topics": [
                        "Math",
                        "Factorial"
                    ],
                    "__v": 0
                },
                {
                    "_id": "657348abd09c5305512955f7",
                    "q_id": "456",
                    "name": "Sorting an Array",
                    "difficulty": "medium",
                    "topics": [
                        "Array",
                        "Sorting"
                    ],
                    "__v": 0
                },
                {
                    "_id": "657348abd09c5305512955f8",
                    "q_id": "789",
                    "name": "Graph Traversal",
                    "difficulty": "hard",
                    "topics": [
                        "Graph",
                        "Traversal"
                    ],
                    "__v": 0
                }
            ],
            "__v": 1
        }
    ]
}
```
{% endswagger-response %}

{% swagger-response status="500: Internal Server Error" description="Internal Server Error" %}
```json
{
  "error": "string",
  "message": "string"
}
```
{% endswagger-response %}
{% endswagger %}

{% hint style="info" %}
**Good to know:** This API method was created using the API Method block, it's how you can build out an API method documentation from scratch. Have a play with the block and you'll see you can do some nifty things like add and reorder parameters, document responses, and give your methods detailed descriptions.
{% endhint %}

## Updating a sheet

{% swagger method="get" path="/sheets" baseUrl="https:/v2api.digitomize.com" summary="" %}
{% swagger-description %}

{% endswagger-description %}
{% endswagger %}

{% hint style="info" %}
**Good to know:** This API method was auto-generated from an example Swagger file. You'll see that it's not editable – that's because the contents are synced to a URL! Any time the linked file changes, the documentation will change too.
{% endhint %}
