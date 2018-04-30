---
title: /weather
position: 1.6
type: get
description: Gets the full weather data details, including temperature, wind, astronomy, and more.
right_code: |
  ~~~ json
  return: |
   {
    "coord": {
      "lon": -121.96,
      "lat": 37.35
    },
    "weather": [
      {
        "id": 500,
        "main": "Rain",
        "description": "light rain",
        "icon": "10d"
      },
      {
        "id": 701,
        "main": "Mist",
        "description": "mist",
        "icon": "50d"
      }
    ],
    "base": "stations",
    "main": {
      "temp": 57.74,
      "pressure": 1015,
      "humidity": 93,
      "temp_min": 57.2,
      "temp_max": 59
    },
    "visibility": 14484,
    "wind": {
      "speed": 14.99,
      "deg": 130
    },
    "clouds": {
      "all": 90
    },
    "dt": 1523030940,
    "sys": {
      "type": 1,
      "id": 479,
      "message": 0.0088,
      "country": "US",
      "sunrise": 1523022288,
      "sunset": 1523068543
    },
    "id": 420006397,
    "name": "Santa Clara",
    "cod": 200
    }
  ~~~
  {: title="Response" }

  ~~~ json
  {
    "error": true,
    "message": "Not supported."
  }
  ~~~
  {: title="Error" }
---
q
: **City name**. *Example: London*. You can call by city name, or by city name and country code. The API responds with a list of results that match a searching word. For the query value, type the city name and optionally the country code divided by comma; use ISO 3166 country codes.

id
: "**City ID**. *Example: `2172797`*. You can call by city ID. API responds with exact result. The List of city IDs can be downloaded [here](http://bulk.openweathermap.org/sample/). You can include multiple cities in parameter &mdash; just separate them by commas. The limit of locations is 20. *Note: A single ID counts as a one API call. So, if you have city IDs. it's treated as 3 API calls.*

lat
: **Latitude**. *Example: 35*. The latitude cordinate of the location of your interest. Must use with `lon`.

lon
: **Longitude**. *Example: 139*. Longitude cordinate of the location of your interest. Must use with `lat`.

zip
: **Zip code**. Search by zip code. *Example: 95050,us*. Please note if country is not specified then the search works for USA as a default.

units
: **Units**. *Example: imperial*. Possible values: `metric`, `imperial`. When you do not use units parameter, format is `standard` by default.

lang
: **Language**. *Example: en*. You can use lang parameter to get the output in your language. We support the following languages that you can use with the corresponded lang values: Arabic - `ar`, Bulgarian - `bg`, Catalan - `ca`, Czech - `cz`, German - `de`, Greek - `el`, English - `en`, Persian (Farsi) - `fa`, Finnish - `fi`, French - `fr`, Galician - `gl`, Croatian - `hr`, Hungarian - `hu`, Italian - `it`, Japanese - `ja`, Korean - `kr`, Latvian - `la`, Lithuanian - `lt`, Macedonian - `mk`, Dutch - `nl`, Polish - `pl`, Portuguese - `pt`, Romanian - `ro`, Russian - `ru`, Swedish - `se`, Slovak - `sk`, Slovenian - `sl`, Spanish - `es`, Turkish - `tr`, Ukrainian - `ua`, Vietnamese - `vi`, Chinese Simplified - `zh_cn`, Chinese Traditional - `zh_tw`.

mode
: "**Mode**. *Example: html*. Determines format of response. Possible values are `xml` and `html`. If mode parameter is empty the format is `json` by default.

These values will be added as query parameters.
{: .success }

The following code sample shows how to make a request using jQuery AJAX:

~~~ javascript
var settings = {
  "async": true,
  "crossDomain": true,
  "url": "http://api.openweathermap.org/data/2.5/weather?zip=95050%2Cus&appid=fd4698c940c6d1da602a70ac34f0b147&units=imperial",
  "method": "GET"
}

$.ajax(settings).done(function (response) {
  console.log(response);
});
~~~
{: title="jQuery" }
