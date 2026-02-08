---
title: "yahoo weather api has changed and now needs auth oauth oauth2"
date: 2019-05-12
categories: 
  - "fsse"
tags: 
  - "api"
  - "auth"
  - "ibm"
  - "oauth"
  - "weather"
  - "yahoo"
---

the yahoo weather api has changed and now needs auth oauth oauth2

old retired urls

- https://query.yahooapis.com
- https://weather.yahooapis.com

new url that requires auth

- https://weather-ydn-yql.media.yahoo.com/forecastrss

yahoo api docs

- https://developer.yahoo.com/api/
- https://developer.yahoo.com/oauth/
- https://developer.yahoo.com/oauth2/guide/
- https://developer.yahoo.com/oauth2/guide/apirequests/

so now _to make API requests, include the access token in the `Authorization` header. Note that API requests must be made securely over HTTPS. The header content comprises of the word `Bearer` followed by the access token._

also  _note that the "Yahoo-App-Id" header will be deprecated soon and after that request without the "X-Yahoo-App-Id" will be rejected._

yahoo api weather docs

- https://developer.yahoo.com/weather/
- https://developer.yahoo.com/weather/documentation.html

yahoo api oauth headers

```
GET /forecastrss?location=sunnyvale,ca HTTP/1.1
Host: weather-ydn-yql.media.yahoo.com
X-Yahoo-App-Id: YOUR_APP_ID
Authorization: OAuth
oauth_consumer_key="YOUR_CONSUMER_KEY",oauth_signature_method="HMAC-SHA1",oauth_timestamp="YOUR_TIMESTAMP",oauth_nonce="YOUR_NONCE",oauth_version="1.0",oauth_signature="YOUR_GENERATED_SIGNATURE"
cache-control: no-cache
```

yahoo api oauth node js example

- https://gist.github.com/osde8info/caee283fe3c78b09d5542299bda4bfbd

if you dont authenticate you will get the error(s)

```
Please provide valid credentials. 
OAuth oauth_problem="OST_OAUTH_PARAMETER_ABSENT_ERROR", realm="yahooapis.com"
Please provide valid credentials. 
OAuth oauth_problem="OST_OAUTH_PARAMETER_ABSENT_ERROR", realm="yahooapis.com"
```

 

you could also try the IBM bluemix weather or OpenWeatherMap apis which also requires auth or a key

- https://twcservice.mybluemix.net/api/weather/v1/geocode/33.40/-83.42/forecast/daily/3day.json
- https://openweathermap.org/api
