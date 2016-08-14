# API DESCRIPTION

```
HOST: seppiajava-1.fyxfn8ksis.us-east-1.elasticbeanstalk.com
API: /fetch/fetchLocationsByLocation
```

## TYPE OF THIS CONNECT

```
HTTP/GET
```

## DESCRIPTION OF PARAMETER

### PARAMETER OF REQUEST

params  | type   | value        | description
------- | ------ | ------------ | --------------------------
lat     | double | 37.4561922   | latitude
lng     | double | -122.1548878 | longitude
radius  | int    | 5000         | radius of this location ^1
keyword | string | "sports"     | 关键词

### TABLE OF RESPONSE

params  | type          | value                           | description
------- | ------------- | ------------------------------- | --------------------------------------
result  | result.item[] | []                              | result of this this time(http request)
tag     | string        | /fetch/fetchLocationsByLocation | tag of this time(http request)
status  | boolean       | true                            | status of this time(http request)
err_msg | string        | None                            | error message(http request)

#### DESCRIBE ITEM OF RESPONSE

params                 | type         | value                                       | description
---------------------- | ------------ | ------------------------------------------- | --------------------------
address                | string       | 3151 Edison Way, Redwood City               | address of this position
phone                  | string       | 123456789                                   | phone or telephone number
name                   | string       | SportsHouse                                 | name of this sport house
geometry               | geometryInfo | {lat:37.476493,lng:-122.2031432}            | information of location
photo                  | phoneInfo    | {height:1530, width:2048, photoReference:-} | information of photo
rating                 | double       | 4.300000190734863                           | rating of this sport house
openingTimeInSevenDays | string[]     |                                             |

```
[SAMPLES DATA] result.item
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
    "photoReference": "CoQBcwAAANjjBvLAv_QK37UvN1jwtFpC6qBSpHKBd1wgj83EqIsIxMBJw--TRoINFqr0fCiVS17DqO9cZvu632_Q5Mia6E5IwFE8hkRn8GGUXWfOOvm65WS_uc45jl2oWWvEMKKUaLSxsPBHlAekNQ9CqW1s99prtjkQLLK5ce3rqOc7gReuEhDvXqi5qbgrrOX1bjqRGclPGhQ9eoCVcGBpG_C4XaJNvyktn2aRuw"
  },
  "rating": 4.300000190734863,
  "openingTimeInSevenDays": []
}
```

##### PARAMETER OF geometryInfo

params | type   | value        | description
------ | ------ | ------------ | -----------
lat    | double | 37.476493    | latitude
lng    | double | -122.2031432 | longitude

##### DESCRIPTION OF phoneInfo

params         | type | value                         | description
-------------- | ---- | ----------------------------- | ---------------
height         | int  | 1530                          | height of photo
width          | int  | 2048                          | width of photo
photoReference | URL  | <http://xxx.com/fdaffdaf.jpg> | url of photo

```
CoQBcwAAANjjBvLAv_QK37UvN1jwtFpC6qBSpHKBd1wgj83EqIsIxMBJw--TRoINFqr0fCiVS17DqO9cZvu632_Q5Mia6E5IwFE8hkRn8GGUXWfOOvm65WS_uc45jl2oWWvEMKKUaLSxsPBHlAekNQ9CqW1s99prtjkQLLK5ce3rqOc7gReuEhDvXqi5qbgrrOX1bjqRGclPGhQ9eoCVcGBpG_C4XaJNvyktn2aRuw
```

# SAMPLES

## REQUEST

```
/fetch/fetchLocationsByLocation?lat=37.4561922&lng=-122.1548878&radius=5000&keyword=%22sports%22
```

## RESPONSE

```
{
  "result": [
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
        "photoReference": "CoQBcwAAANjjBvLAv_QK37UvN1jwtFpC6qBSpHKBd1wgj83EqIsIxMBJw--TRoINFqr0fCiVS17DqO9cZvu632_Q5Mia6E5IwFE8hkRn8GGUXWfOOvm65WS_uc45jl2oWWvEMKKUaLSxsPBHlAekNQ9CqW1s99prtjkQLLK5ce3rqOc7gReuEhDvXqi5qbgrrOX1bjqRGclPGhQ9eoCVcGBpG_C4XaJNvyktn2aRuw"
      },
      "rating": 4.300000190734863,
      "openingTimeInSevenDays": []
    },
    {
      "address": "450 Broadway, Redwood City",
      "phone": "123456789",
      "name": "Stanford Sports Medicine Clinic",
      "geometry": {
        "lat": 37.4857142,
        "lng": -122.2030561
      },
      "photo": {
        "height": 252,
        "width": 252,
        "photoReference": "CoQBcwAAAMBrft7_csGrZi_JW8Cvhv_hMxSskjAPemeq0dukyzpJAQ8p5VXdgT8aSptkYaY9xgx49Uo5cCcv_RoCzILqpWeeDbo2ikK2cxZGZyOfdZ_bBP02IluXQlS7VtelG-IOBKdV03-XQ_Stqe6Fyfh-WX2VMzHvdI-jfmZkBlUXIn4pEhA1Y4GKPjzuw2zzdn3xiXNyGhQdqA1S_vlQ3HcklEUqJDTej_FzZg"
      },
      "rating": 4.5,
      "openingTimeInSevenDays": []
    },
    {
      "address": "3705 Haven Avenue, Menlo Park",
      "phone": "123456789",
      "name": "Hi Five Sports",
      "geometry": {
        "lat": 37.485557,
        "lng": -122.18225
      },
      "photo": {
        "height": 156,
        "width": 324,
        "photoReference": "http://images.locanto.in/1124850122/Regent-Club-One-of-the-top-clubs-in-Bangalore-sports-club-in_3.jpg"
      },
      "rating": 0.0,
      "openingTimeInSevenDays": []
    },
    {
      "address": "795 El Camino Real, 3rd Floor, Palo Alto",
      "phone": "123456789",
      "name": "Sports Medicine: Palo Alto Center: Palo Alto Medical Foundation",
      "geometry": {
        "lat": 37.439262,
        "lng": -122.162161
      },
      "photo": {
        "height": 156,
        "width": 324,
        "photoReference": "http://images.locanto.in/1124850122/Regent-Club-One-of-the-top-clubs-in-Bangalore-sports-club-in_3.jpg"
      },
      "rating": 2.799999952316284,
      "openingTimeInSevenDays": []
    },
    {
      "address": "162 University Avenue, Palo Alto",
      "phone": "123456789",
      "name": "Black Diamond Sports",
      "geometry": {
        "lat": 37.444224,
        "lng": -122.16305
      },
      "photo": {
        "height": 600,
        "width": 960,
        "photoReference": "CoQBcwAAAH5LKe7tGQi6vZ8F-i0OxhxSkuGxZmDOx20COnOg-mkmC84YeAM8zIv-kEA-f5pFMDFHD7HEkLx06N4oNpanz-rJWtb2EK6r2YXYhyOVBGDfKoTWqWL3hxpl0YRiGWh9CkDzBkSSU0DZ1GScD91wGQvXjm7-Dnk8tm7q_KUxjZJSEhCiYV9NqR3QSlBdJLlR46vMGhSWR9n8UM52F6-h734IJyVk1HVx-w"
      },
      "rating": 4.699999809265137,
      "openingTimeInSevenDays": []
    },
    {
      "address": "260 Sheridan Avenue, Palo Alto",
      "phone": "123456789",
      "name": "Sports Medicine Institute",
      "geometry": {
        "lat": 37.4263825,
        "lng": -122.1410112
      },
      "photo": {
        "height": 156,
        "width": 324,
        "photoReference": "http://images.locanto.in/1124850122/Regent-Club-One-of-the-top-clubs-in-Bangalore-sports-club-in_3.jpg"
      },
      "rating": 0.0,
      "openingTimeInSevenDays": [
        "",
        "",
        "",
        "",
        "",
        "",
        ""
      ]
    },
    {
      "address": "341 Galvez Street, Stanford",
      "phone": "123456789",
      "name": "Stanford ACSR",
      "geometry": {
        "lat": 37.430006,
        "lng": -122.163805
      },
      "photo": {
        "height": 533,
        "width": 535,
        "photoReference": "CoQBcwAAAN3sBjjKx5-ChSDwRzBBLnen3TMqEZ0c0UNETGU2CBq6T-Gcd6yFUxXqMwe1pyArfFWIj6MQ4sdYxF3hWtSuKCDi2gZX3-9K7qjYImMaIYVclwyPIFJpSANr75QSs_Qs_ZlZrkx3HIQBfs1fz5Tzb8GX_sRf2vKn1xpasvkOWDwtEhA1J1KFVtH1h-pV4jCzaO09GhS4sOLHlFQPz75nX8Ee49RndiqB0g"
      },
      "rating": 0.0,
      "openingTimeInSevenDays": []
    },
    {
      "address": "208 Hamilton Avenue, Palo Alto",
      "phone": "123456789",
      "name": "Title Nine",
      "geometry": {
        "lat": 37.4439661,
        "lng": -122.1612265
      },
      "photo": {
        "height": 156,
        "width": 324,
        "photoReference": "http://images.locanto.in/1124850122/Regent-Club-One-of-the-top-clubs-in-Bangalore-sports-club-in_3.jpg"
      },
      "rating": 0.0,
      "openingTimeInSevenDays": []
    },
    {
      "address": "341 Galvez Street, Stanford",
      "phone": "123456789",
      "name": "Stanford Sports Medicine",
      "geometry": {
        "lat": 37.4297643,
        "lng": -122.1638611
      },
      "photo": {
        "height": 156,
        "width": 324,
        "photoReference": "http://images.locanto.in/1124850122/Regent-Club-One-of-the-top-clubs-in-Bangalore-sports-club-in_3.jpg"
      },
      "rating": 0.0,
      "openingTimeInSevenDays": [
        "",
        "",
        "",
        "",
        "",
        "",
        ""
      ]
    },
    {
      "address": "1610A El Camino Real, Menlo Park",
      "phone": "123456789",
      "name": "Bulldogs Sports \u0026 Fitness",
      "geometry": {
        "lat": 37.4582497,
        "lng": -122.1915069
      },
      "photo": {
        "height": 2048,
        "width": 2048,
        "photoReference": "CoQBcwAAAEJ7xYHN5HubqiduxbXNrqb8OiNLuXgqZurMsdsbX6LEzOtfvnGqLJX5sGTdR0p-DXAA51iIRKLM0rSdeJGr1U7I3wRM-VNGoOlb9k4g_VrMjsgP3994B-T_PHml1NQrorevbC65GFnJqlwB6xsT_Gpvw2V-K_xkjmV2PmJIOn18EhA8cpgLEL5Ejyp1Gobtxy1GGhSiux88ZiWpfKsLpFXVzJQH9FLiZw"
      },
      "rating": 0.0,
      "openingTimeInSevenDays": []
    },
    {
      "address": "Stanford",
      "phone": "123456789",
      "name": "Arrillaga Family Sports Center",
      "geometry": {
        "lat": 37.4301563,
        "lng": -122.161616
      },
      "photo": {
        "height": 156,
        "width": 324,
        "photoReference": "http://images.locanto.in/1124850122/Regent-Club-One-of-the-top-clubs-in-Bangalore-sports-club-in_3.jpg"
      },
      "rating": 4.199999809265137,
      "openingTimeInSevenDays": [
        "",
        "",
        "",
        "",
        "",
        "",
        ""
      ]
    },
    {
      "address": "368 California Avenue, Palo Alto",
      "phone": "123456789",
      "name": "Massage Therapy Center",
      "geometry": {
        "lat": 37.4268854,
        "lng": -122.1447246
      },
      "photo": {
        "height": 1363,
        "width": 2048,
        "photoReference": "CoQBcwAAAH5p8Th43gvK58x0Gc2u9T0nMx2ximGTLJ7tKhrfFaMJWg_-QbtPZ45NCMLxmQEkwVC1AWBDAUVM1K6kaPjyxjPLen83InwkFhc2oBY2lEistVkaTsvCot-8TXiuoqNVRr6WxvwY5TAIoNM-FNdh9NehEbkMqhDOaa9bT6SG-qk1EhD2ediUiTNStKNQFKFP_vTWGhQ-u9BY2NyB4-0UgNEY6cQOltD6SA"
      },
      "rating": 4.800000190734863,
      "openingTimeInSevenDays": []
    },
    {
      "address": "859 Santa Cruz Avenue, Menlo Park",
      "phone": "123456789",
      "name": "Fleet Feet Menlo Park",
      "geometry": {
        "lat": 37.4503001,
        "lng": -122.1853929
      },
      "photo": {
        "height": 3024,
        "width": 4032,
        "photoReference": "CoQBdwAAAGqXPrLrtakpdPTZ2Y1uarmiWAMPTPgCcBThC0h46l-Voxw0_w30t5XPxyJTR8cx_rwDyhDCm0-n-g3GoXQNhS5GWXqshDdgQScAqfkl5bIB-iWAt8gRjqBajVdiVLQxIRAyRqnsSmDtskSbQqzeCxlUB7NHpuCMqG3VGpBVBl_WEhAqeMYoB7JReW-w99rlRsqYGhTe748VPXHHdnu14GeM25Nwre3nCg"
      },
      "rating": 4.800000190734863,
      "openingTimeInSevenDays": []
    },
    {
      "address": "209 El Camino Real, Menlo Park",
      "phone": "123456789",
      "name": "Sarti Sports Medicine",
      "geometry": {
        "lat": 37.44833669999999,
        "lng": -122.174493
      },
      "photo": {
        "height": 156,
        "width": 324,
        "photoReference": "http://images.locanto.in/1124850122/Regent-Club-One-of-the-top-clubs-in-Bangalore-sports-club-in_3.jpg"
      },
      "rating": 0.0,
      "openingTimeInSevenDays": [
        "",
        "",
        "",
        "",
        "",
        "",
        ""
      ]
    },
    {
      "address": "700 El Camino Real, Menlo Park",
      "phone": "123456789",
      "name": "Big 5 Sporting Goods",
      "geometry": {
        "lat": 37.451287,
        "lng": -122.177902
      },
      "photo": {
        "height": 695,
        "width": 1200,
        "photoReference": "CoQBcwAAAAdBUKPfAstrPdO-dKAdorhHDkAVODP8GM12dXFc0RXiPg-K-L6-3ubnwmnGjdaoIFRkKm-w61S8u3YPFmWQzS0-yurC0BqWIrePfi2ltiscdbWi8TBo91dkP_qWTPiGsZ_03WYwzlosrt27txiefV2BoLILXgnsfJ4JRZymmY8gEhBACJ8KX5At0XdmpbHdyjwAGhS5_jDQmWvOWqQRMty6uNAPIcacTg"
      },
      "rating": 3.799999952316284,
      "openingTimeInSevenDays": []
    },
    {
      "address": "429 California Avenue, Palo Alto",
      "phone": "123456789",
      "name": "ZombieRunner",
      "geometry": {
        "lat": 37.4259759,
        "lng": -122.1447369
      },
      "photo": {
        "height": 600,
        "width": 600,
        "photoReference": "CoQBcwAAAKzo2JQwy4_K3PhDWsvEVMwzJGDlmjOdvXhza18oxWs0Xayxo7lSg3OBa2VEpzL_wPufpHDfx6UZM2w9HEpVzaRZWwndRgJstlE8FtLrVi84ms-5v3EZzaxqBSlccN0mQrhhrt_HTewB_C7_beivazgw-8J6lUfjBEfDFc_vzphbEhDz-nQMB4Hk2WDs3YxJY1dfGhTT0bOtL3Ir-DttDE2eUmvYx1AhTw"
      },
      "rating": 4.800000190734863,
      "openingTimeInSevenDays": []
    },
    {
      "address": "250 Hamilton Avenue, Palo Alto",
      "phone": "123456789",
      "name": "Decathlon Sports Club-Summer Camps/Sports Camps",
      "geometry": {
        "lat": 37.4442545,
        "lng": -122.1599094
      },
      "photo": {
        "height": 800,
        "width": 672,
        "photoReference": "CoQBcwAAAPkGSLyEcl5CgLXMBv3Btv6GFpRKcHrStvBDfU57efGW-7wJnKe45NFci0Yv0wj-vI38spt-R4wYWbc9Jyzp95-p--qcxq8OL0Cqaz76typIcXRZNtZ0PLxnmRcqohnF--jkmrnwrjdwLVIIR2DF1PKu-wHpJOChK3AlmiQGGJBwEhD6NvioHfV_dDAeXwqnquvpGhSmIo-FlyUJCGSpcNfufGH0wHR9zQ"
      },
      "rating": 0.0,
      "openingTimeInSevenDays": [
        "",
        "",
        "",
        "",
        "",
        "",
        ""
      ]
    },
    {
      "address": "Street Pavilion B31, 3rd Floor, 450 Broadway, Redwood City",
      "phone": "123456789",
      "name": "Stanford Orthopaedic and Sports Medicine Physical Therapy Clinic",
      "geometry": {
        "lat": 37.4857417,
        "lng": -122.2029766
      },
      "photo": {
        "height": 252,
        "width": 252,
        "photoReference": "CoQBcwAAADbM3WpL157k3o5gsFDOJQ_3Wv7653-k6tUoXB0X1hGWqoKUB3-s_IvJ_-3IUme4D1IQDxHMG0aS_u0dMSVxYxQF0DUUwyftSfLZCH_fQDTLNr_ouQFQAb7Ro5_r-Zm8JLatjngq_YOldJ3bKK3fUs1skin9gcqjbkIjlm52Zh-vEhCjent2hbP30LNBUupYGT1qGhRyJVXGa_BZ_c1Tf0mLkpZmVqkCqg"
      },
      "rating": 0.0,
      "openingTimeInSevenDays": []
    },
    {
      "address": "412 Emerson Street, Palo Alto",
      "phone": "123456789",
      "name": "The Patio",
      "geometry": {
        "lat": 37.4451663,
        "lng": -122.1639157
      },
      "photo": {
        "height": 1365,
        "width": 2048,
        "photoReference": "CoQBcwAAAHnqztlsSKcs2d4M-mQvdvRqjPQVmSf10HHlnFuy7o1PmYkILYNGTt3T9QpUFM8Df8PtRaGKj1wFgRSzW0uaAGdGozdbEpyISheI2t1HBWJxv1csf5bdtTGOlyG5OrE-eq1OcRGDphWwX136ax24mPMy-sW1GD9keO29ovIt4YjuEhAbC_yIxxe5DalVvv8JL_2tGhTI1qwv8p6f-Orb772NZt5RSiAWlw"
      },
      "rating": 3.299999952316284,
      "openingTimeInSevenDays": []
    },
    {
      "address": "2450 Charleston Road, Mountain View",
      "phone": "123456789",
      "name": "REI",
      "geometry": {
        "lat": 37.4231682,
        "lng": -122.0966487
      },
      "photo": {
        "height": 432,
        "width": 432,
        "photoReference": "CoQBcwAAAO-wngp7Omm-AiBCCYdu6zQnTV5uYYg9BSr8A5uuFXC9p_NDwG6u74Lkgs5WCfDG6hRPmcXbwGt75XNetUuWpupqXIlGjDXVABxcApdP12k_ntTwUWEI-_q0Lt3M-g88hvY6cykpx70REQHj3omQX-RgW9R2Nw26n9_yRSOenb3KEhDmgKmVMFqVY5raggX4sykYGhRnswUk2-0M08p1i6E_1KTV2tEAmw"
      },
      "rating": 4.199999809265137,
      "openingTimeInSevenDays": []
    }
  ],
  "tag": "/fetch/fetchLocationsByLocation",
  "status": true,
  "err_msg": "None"
}
```
