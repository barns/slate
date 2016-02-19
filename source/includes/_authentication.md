# Authentication

> To send a request, you must include your api key in the authorization header

```shell
-H "Authorization: <Your api key>"
```

```ruby
headers: { "Authorization" => "<Your api key>" }
```

```php
$headers = array(
  "Accept" => "application/json",
  "Authorization" => "<Your api key>"
);
```

```python
headers = {
  "Authorization": "<Your api key>"
})
```

```javascript
.header('Authorization', '<Your api key>')
```

```objective_c
NSDictionary* headers = @{@"authorization": @"<Your api key>"};
```

```java
.header("authorization", "<Your api key>")
```

> If you don't know your API Key, you can sign in to the JsonGeocode website to find it

JsonGeocode uses API keys to allow access to the API. If you don't have one, you can register for free on our [website]](http://jsongeocode.com/signup).

JsonGeocode expects for the API key to be included in all API requests to the server in a header that looks like the following:

`Authorization: <Your api key>`
