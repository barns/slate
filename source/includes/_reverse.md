# Reverse Search

```shell
curl "http://jsongeocode.com/api/v1/reverse?lat=13.3888599&lon=52.5170365"
  -H "Authorization: <Your api key>"
```

```ruby
gem install unirest

require 'unirest'

response = Unirest.get "https://jsongeocode.com/api/v1/reverse",
    headers: { "Accept" => "application/json",
        "Authorization" => "<Your api key>" },
    parameters: { lat: 13.3888599, lon: 52.5170365 }

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

  $response = Unirest\Request::get("https://jsongeocode.com/api/v1/reverse",
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
    "lat": 13.3888599
    "lon": 52.5170365
  });

print response.body
```

```javascript
unirest.get("https://jsongeocode.com/search")
  .headers({ "Accept": "application/json", "Authorization": "<Your api key>" })
  .send({ "lat": 13.3888599, "lon": 52.5170365 })
  .end(function (response) {
    console.log(response.body)
  });
```

```objective_c
NSDictionary* headers = @{@"accept": @"application/json",
    @"authorization": @"<Your api key>"};
NSDictionary* parameters = @{@"lat": @13.3888599, @"lon": @52.5170365};

UNIHTTPJsonResponse *response = [[UNIRest post:^(UNISimpleRequest *request) {
  [request setUrl:@"http://jsongeocode.com/api/v1/search"];
  [request setHeaders:headers];
  [request setParameters:parameters];
}] asJson];
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

You can use this endpoint when you have a latitude and longitude.

<aside class="information">
  JsonGeocode will always return a standard json object, so if it's not possible to determine an attribute, like a house number, it will be returned as an empty string.
</aside>

### HTTP Request

`GET http://jsongeocode.com/ap1/v1/reverse`

### Query Parameters

Parameter | Description
--------- | -----------
lat | Latitude to search
lon | Longitude to search
