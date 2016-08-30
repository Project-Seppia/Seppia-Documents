# API FORMAT

all of api use JSON(`Content-Type: application/json`)

# API DESCRIPTION

```
HOST: seppiajava-1.fyxfn8ksis.us-east-1.elasticbeanstalk.com
```

**ATTENTION**

> when Http Code is 100, Response format is: `{"code":100,"message":"Sucessed.","tag":"/fetch/fetchLocationsByLocation","data":{}}`

## 1\. fetch Locations by location

**Url**<br>
`http://host.url/fetch/fetchLocationsByLocation`

**Method**<br>
`GET`

**Request**<br>

`{ "lat":37.4561922, "lng":-122.1548878, "radius":5000, "keyword":"sports" }`

**Response**

```
{
  "result": {
    "locations": [
      {
        "address": "3151 Edison Way, Redwood City",
        "phone": "123456789",
        "name": "SportsHouse",
        "geometry": {
          "lat": 37.476493,
          "lng": -122.2031432
        },
        "photo": {
          "height": 1530,
          "width": 2048,
          "photoReference": "http://t.cn/image01.jpg"
        },
        "rating": 4.300000190734863,
        "openingTimeInSevenDays": []
      }
    ]
  },
  "code": 200,
  "tag": "/fetch/fetchLocationsByLocation",
  "status": true,
  "err_msg": "None"
}
```

## TYPE DEFINE

[ ^1]: DESCRIPTION OF PARAMETER IN REQUEST

> params  | type   | value        | description
> ------- | ------ | ------------ | -----------------------
> lat     | double | 37.4561922   | latitude
> lng     | double | -122.1548878 | longitude
> radius  | int    | 5000         | radius of this location
> keyword | string | "sports"     | Keyword

[ ^2]: DESCRIPTION OF RESPONSE

> params  | type    | value                           | description
> ------- | ------- | ------------------------------- | --------------------------------------
> result  | result  | Locations                       | result of this this time(http request)
> tag     | string  | /fetch/fetchLocationsByLocation | tag of this time(http request)
> status  | boolean | true                            | status of this time(http request)
> code    | int     | from a to b                     | action return code
> err_msg | string  | None                            | error message(http request)

[ ^3]: DESCRIPTION OF _Locations_

> params                 | type      | value                                       | description
> ---------------------- | --------- | ------------------------------------------- | --------------------------
> address                | string    | 3151 Edison Way, Redwood City               | address of this position
> phone                  | string    | 123456789                                   | phone or telephone number
> name                   | string    | SportsHouse                                 | name of this sport house
> geometry               | Geometry  | {lat:37.476493,lng:-122.2031432}            | information of location
> photo                  | phoneInfo | {height:1530, width:2048, photoReference:-} | information of photo
> rating                 | double    | 4.300000190734863                           | rating of this sport house
> openingTimeInSevenDays | string[]  |                                             |

[ ^4]: DESCRIPTION OF _Geometry_

> params | type   | value        | description
> ------ | ------ | ------------ | -----------
> lat    | double | 37.476493    | latitude
> lng    | double | -122.2031432 | longitude

[ ^5]: DESCRIPTION OF _phoneInfo_

> params         | type | value                         | description
> -------------- | ---- | ----------------------------- | ---------------
> height         | int  | 1530                          | height of photo
> width          | int  | 2048                          | width of photo
> photoReference | URL  | <http://xxx.com/fdaffdaf.jpg> | url of photo
