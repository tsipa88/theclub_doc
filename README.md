# clubdoc


# Authentication

Authentication user with EMAIL and PASSWORD.
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
GET http://localhost:3000/api/posts
~~~
# Current User's Posts
Get current_user posts. Add parameter "self":"true", parameter "page" for pagination
~~~bash
GET http://localhost:3000/api/posts
~~~
# User's Posts
Get another user's post. Add parameter "user_id":"1", parameter "page" for pagination
~~~bash
GET http://localhost:3000/api/posts
~~~
Response
~~~bash
{
  "id":1,
  "user_id":1,
  "user_name":"John",
  "user_surname":"Doe",
  "user_avatar":"/system/avatar/781/4675.jpg",
  "photos":[
            {
              "image":"/system/posts/photo/image/279/image.jpg"
            },{
              "image":"/system/posts/photo/image/282/image.jpg"
            }
           ],
  "likes":[
            {
              "id":1,
              "user_id":1,
              "user_name":"John",
              "user_surname":"Doe",
              "user_avatar":"/system/avatar/1/image.jpg",
              "created_at":"2015-04-23T17:09:09.394+03:00",
              "updated_at":"2015-04-23T17:09:09.394+03:00"
            }
          ],
  "comments":[
              {
                "id":1,
                "user_id":1,
                "commentable_id":1,
                "commentable_type":"Post",
                "text":"lorem ipsum dolor sit amet consectetur adipiscing elit",
                "created_at":"2015-02-27T05:54:41.465+03:00",
                "updated_at":"2015-02-27T05:54:41.465+03:00"
              }
             ],
  "text":"lorem ipsum dolor sit amet consectetur adipiscing elit ...",
  "created_at":"2015-02-06T02:05:21.903+03:00",
  "updated_at":"2016-01-25T13:40:33.790+03:00",
  "latitude":null,
  "longitude":null,
  "address":"",
  "map_zoom":null,
  "postable_type":"Member",
  "postable_id":1,
  "pop_club":1,
  "pop_garage":null,
  "pop_company":null,
  "pop_community":null,
  "status":"none",
  "pop_featured":null,
  "popular_at":"2015-02-06T02:05:21.903+03:00" 
}
~~~


Authentication https://github.com/lynndylanhurley/devise_token_auth#usage-tldr


```
