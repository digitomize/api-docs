# Contests

## Get All Contests

{% swagger baseUrl="https://v2api.digitomize.com" method="post" path="/contests" summary="Get all contests" %}
{% swagger-description %}
This endpoint allows you to retrieve information about various programming contests. You can filter contests based on the `host` and `vanity` query parameters.
{% endswagger-description %}

{% swagger-parameter in="body" name="host" required="false" type="string" %}
Enter one or more hosting platforms to filter contests. Separate multiple platforms with commas.
{% endswagger-parameter %}

{% swagger-parameter in="body" name="vanity" required="false" type="string" %}
Enter the unique vanity string associated with a specific contest to retrieve details about that contest.
{% endswagger-parameter %}

{% swagger-response status="200" description="OK" %}
```json
{
  "total": 0,
  "results": [
    {
      "url": "string",
      "host": "string",
      "name": "string",
      "vanity": "string",
      "duration": 0,
      "startTimeUnix": 0
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

## Updating a pet

{% swagger src="https://petstore.swagger.io/v2/swagger.json" path="/pet" method="put" %}
[https://petstore.swagger.io/v2/swagger.json](https://petstore.swagger.io/v2/swagger.json)
{% endswagger %}

{% hint style="info" %}
**Good to know:** This API method was auto-generated from an example Swagger file. You'll see that it's not editable – that's because the contents are synced to a URL! Any time the linked file changes, the documentation will change too.
{% endhint %}
