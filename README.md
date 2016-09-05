# clubdoc


# Authentication

Authenticate user with EMAIL and PASSWORD.
~~~bash
POST http://localhost:3000/api/auth/sign_in
~~~
Access-token and client in response headers

# User's profile
Get current_user info
~~~bash
GET http://localhost:3000/api/cabinet
~~~

# Current User's transports
Get current_user transports. Add parameter "self":"true" 
~~~bash
GET http://localhost:3000/api/transports
~~~
# User's transports
Get another user's transports. Add parameter "user_id":"1", parameter "page" for pagination
~~~bash
GET http://localhost:3000/api/transports
~~~
# All Transports
Get all transports. Add parameter "page":"1" for pagination 
~~~bash
GET http://localhost:3000/api/transports
~~~

Response:
~~~bash
{
  "id":1,
  "user_id":1,
  "user_name":"John",
  "user_surname":"Doe",
  "user_avatar":"/system/avatar/903/image.jpg",
  "avatars":[
              {
                "image":"/system/avatar/900/image.jpg","current":true
              }
            ],
  "backgrounds":[
                  {
                    "image":"/system/avatar/900/image.jpg","current":true
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
  "created_at":"2015-09-08T19:40:32.147+03:00",
  "updated_at":"2015-09-14T17:48:44.340+03:00",
  "model":"Escalate",
  "manufacturer":"Cadillac",
  "engine":"Бензин атмосферный",
  "transmission":"Автомат",
  "state":"declined",
  "specifications":{
                    "about":"",
                    "power":"405",
                    "max_speed":"270",
                    "wheel_drive":"all_permanent",
                    "acceleration":"6,5",
                    "engine_volume":"6,2",
                    "production_year":"2010"
                   },
  "kind":"ground",
  "accepted_at":null,
  "rank":1,
  "top_number":0,
  "purpose":"general"
}
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

# Get Current User's friendly Profiles
Add parameter "page":"1" for pagination.
~~~bash
GET http://localhost:3000/api/profiles
~~~

# Get another User's friendly Profiles
Add parameter User's id for "profile_id""
~~~bash
GET http://localhost:3000/api/profiles

Authentication https://github.com/lynndylanhurley/devise_token_auth#usage-tldr


```
