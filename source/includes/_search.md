# Search

```shell
curl "http://jsongeocode.com/api/v1/search?query=berlin&tag=natural"
  -H "Authorization: <Your api key>"
```

```ruby
gem install unirest

require 'unirest'

response = Unirest.get "https://jsongeocode.com/api/v1/search",
    headers: { "Accept" => "application/json",
        "Authorization" => "<Your api key>" },
    parameters: { query: "berlin", tag: "natural" }

p response.body
```

```php
<?php
  git clone git@github.com:Mashape/unirest-php.git // Or install with composer

  require_once "/path/to/Unirest.php";

  $headers = array(
    "Accept" => "application/json",
    "Authorization" => "<Your api key>"
  );

  $body = array("query" => "berlin", "tag" => "natural");

  $response = Unirest\Request::get("https://jsongeocode.com/api/v1/search",
      $headers, $body);

  $response->body
?>
```

```python
pip install unirest

import unirest

response = unirest.get("https://jsongeocode.com/api/v1/search",
  headers = {
    "Accept": "application/json"
    "Authorization": "<Your api key>"
  },
  params = {
    "query": "berlin"
    "tag": "natural"
  });

print response.body
```

```javascript
unirest.get("https://jsongeocode.com/search")
  .headers({ "Accept": "application/json", "Authorization": "<Your api key>" })
  .send({ "query": "berlin", "tag": "natural" })
  .end(function (response) {
    console.log(response.body)
  });
```

```objective_c
NSDictionary* headers = @{@"accept": @"application/json",
    @"authorization": @"<Your api key>"};
NSDictionary* parameters = @{@"query": @"berlin", @"tag": @"natural"};

UNIHTTPJsonResponse *response = [[UNIRest get:^(UNISimpleRequest *request) {
  [request setUrl:@"http://jsongeocode.com/api/v1/search"];
  [request setHeaders:headers];
  [request setParameters:parameters];
}] asJson];
```

```java
HttpResponse<JsonNode> jsonResponse = Unirest
  .get("http://jsongeocode.com/api/v1/search")
  .header("accept", "application/json")
  .header("authorization", "<Your api key")
  .field("query", "berlin")
  .field("tag", "natural")
  .asJson();

System.out.println(jsonResponse.toString)
```

> This will result in the following response:

```json
{
  "results" : [
    {
      "lat": -73.2856639,
      "lon": 42.6917468,
      "location_type": "natural",
      "location_details": "peak",
      "house_number": "",
      "name": "Berlin Mountain",
      "city": "",
      "region": "New York",
      "postcode": "",
      "country": "United States of America"
    },
    {
      "lat": -86.8216671,
      "lon": 35.52285,
      "location_type": "natural",
      "location_details": "peak",
      "house_number": "",
      "name": "Berlin Hill",
      "city": "",
      "region": "Tennessee",
      "postcode": "",
      "country": "United States of America"
    }
  ]
}
```

Use this endpoint to search for an address, city, country etc.

<aside class="information">
  JsonGeocode will always return a standard json object, so if it's not possible to determine an attribute, like a house number, it will be returned as an empty string.
</aside>

### HTTP Request

`GET http://jsongeocode.com/ap1/v1/search`

### Query Parameters

Parameter | Description
--------- | -----------
query | The address/city/country etc. to search
tag | Optional. Specifies the type of result you're looking for. See below for some examples

### Tags

These are some examples of tags you could use in your search

Tag | Description
--- | -----------
natural | Shows you natural landmarks etc.
highway | Specifies that you are looking for roads, etc.
place | Limit your results to just places (i.e. countries, cities not roads)
emergency | Emergency facilities and equipment
military | Specifies that you are looking for military sites
