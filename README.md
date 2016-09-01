# theclub_doc
docs

# Authentication

Authorize user with EMAIL and PASSWORD.
~~~bash
POST http://localhost:3000/api/auth/sign_in
~~~
Access-token and client in response headers

# User's profile
Get current_user info
~~~bash
GET http://localhost:3000/api/cabinet
~~~

# User's transports
Get current_user transport. Add parameter "self":"true" 
~~~bash
GET http://localhost:3000/api/transports
~~~

Response:
~~~bash
[
  {
    "id":165,
    "user_id":10,
    "model":"11",
    "created_at":"2015-06-28T20:41:57.829+03:00",
    "updated_at":"2015-09-07T12:59:37.604+03:00",
    "manufacturer_id":6,
    "engine_id":5,
    "transmission_id":null,
    "state":"declined",
    "specifications":
    {
      "about":"",
      "power":"1",
      "max_speed":"",
      "wheel_drive":"rear",
      "acceleration":"",
      "engine_volume":"1",
      "production_year":"2015"
    },
    "kind":"ground",
    "accepted_at":null,
    "rank":1,
    "top_number":0,
    "purpose":"general"
  },

  {
    "id":6,
    "user_id":10,
    "model":"SLS AMG",
    "created_at":"2015-01-27T15:25:59.039+03:00",
    "updated_at":"2015-10-09T17:00:57.551+03:00",
    "manufacturer_id":29,
    "engine_id":4,
    "transmission_id":3,
    "state":"accepted",
    "specifications":
    {
      "about":"Wow!)",
      "power":"583",
      "max_speed":"317",
      "wheel_drive":"rear",
      "acceleration":"3.8",
      "engine_volume":"6.2",
      "production_year":"2015"
    },
    "kind":"ground",
    "accepted_at":"2015-01-27T15:27:19.954+03:00",
    "rank":1,
    "top_number":0,
    "purpose":
    "target"
  }
]
~~~

# All Transports
Get all transports. Add parameter "page":"1" for pagination 
~~~bash
GET http://localhost:3000/api/transports
~~~

# All Posts
Get all posts. Add parameter "page":"1" for pagination 
~~~bash
GET http://localhost:3000/api/transports
~~~

Response
~~~bash
[
  {
    "id":51,
    "user_id":10,
    "text":"http://vimeo.com/109141765",
    "created_at":"2015-02-06T02:05:21.903+03:00",
    "updated_at":"2016-01-25T13:40:33.790+03:00",
    "latitude":null,
    "longitude":null,
    "address":"",
    "map_zoom":null,
    "postable_type":"Member",
    "postable_id":12,
    "pop_club":75,
    "pop_garage":null,
    "pop_company":null,
    "pop_community":null,
    "status":"none",
    "pop_featured":null,
    "popular_at":"2015-02-06T02:05:21.903+03:00"
  },
  {
    "id":313,
    "user_id":10,
    "text":"See the incredible cars of Pebble Beach's multimillion-dollar ......",
    "created_at":"2015-08-23T03:03:55.690+03:00",
    "updated_at":"2016-01-25T13:40:34.518+03:00",
    "latitude":null,
    "longitude":null,
    "address":"",
    "map_zoom":null,
    "postable_type":"Member",
    "postable_id":12,
    "pop_club":18,
    "pop_garage":null,
    "pop_company":null,
    "pop_community":null,
    "status":"none",
    "pop_featured":null,
    "popular_at":"2015-08-23T03:03:55.690+03:00"
  }
]
~~~

# User's Posts
Get current_user transport. Add parameter "self":"true" 
~~~bash
GET http://localhost:3000/api/transports
~~~

Authentication https://github.com/lynndylanhurley/devise_token_auth#usage-tldr


```
