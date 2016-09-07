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
  "avatars_attributes":[
                        {
                          "image":"/system/avatar/900/image.jpg","current":true
                        }
                       ],
  "backgrounds_attributes":[
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
  "photos_attributes":[
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

# Current User's friendly Profiles
Get Current User's friendly Profiles. Add parameter "page":"1" for pagination.
~~~bash
GET http://localhost:3000/api/profiles
~~~

# User's friendly Profiles
Get another User's friendly Profiles. Add parameter User's id for "profile_id""
~~~bash
GET http://localhost:3000/api/profiles
~~~

~~~bash

Response
[
  {
    "id":1,
    "user_name":"John",
    "user_surname":"Doe",
    "user_avatar":"/system/avatar/1175.jpg",
    "user_nickname":"john77",
    "gender":"female",
    "birthdate":"1988-05-04",
    "status":"Hello world!",
    "rank":1,
    "top_number":0,
    "kind":"simple"
  },{
    "id":2,
    "user_name":"John",
    "user_surname":"Doe",
    "user_avatar":"/system/avatar/image.jpg",
    "user_nickname":"john88",
    "gender":"male",
    "birthdate":"1997-02-25",
    "status":"Hello world!",
    "rank":1,
    "top_number":0,
    "kind":"simple"
  }
]
~~~

# Current User's Communities list
Get Current User's Communities list. Add parameter "self":"true", parameter "page":"1" for pagination. 
~~~bash
GET http://localhost:3000/api/communities
~~~

# User's friendly Communities list
Get another User's Communitites list. Add parameter "user_id", parameter "page":"1" for pagination. 
~~~bash
GET http://localhost:3000/api/communities
~~~

# All Communities list
Get all Communities. Add parameter "page":"1" for pagination. 
~~~bash
GET http://localhost:3000/api/communities
~~~

Response
~~~bash
[
  {
    "id":1,
    "name":"Porsche Club",
    "nickname":"pclb",
    "site":"http://porsche-club.com",
    "description":"Grand Porsche Club",
    "category_id":2,
    "category":"Автомобили",
    "rank":1,
    "created_at":"2015-02-16T14:29:21.534+03:00",
    "updated_at":"2015-02-25T12:28:30.719+03:00"
  },{
    "id":2,
    "name":"Mersedes-Benz Club",
    "nickname":"mb_clb",
    "site":"http://m-b.club",
    "description":"MB clubbb",
    "category_id":6,
    "category":"Автомобили",
    "rank":1,
    "created_at":"2015-02-24T12:44:11.757+03:00",
    "updated_at":"2015-02-25T12:34:29.958+03:00"
  }
]
~~~

# All Advertisements
Get all Advertisements. Add parameter "page":"1" for pagination 
~~~bash
GET http://localhost:3000/api/advertisements
~~~
# Current User's Advertisements
Get current_user Advertisements. Add parameter "self":"true", parameter "page" for pagination
~~~bash
GET http://localhost:3000/api/advertisements
~~~
# User's Advertisements
Get another user's Advertisements. Add parameter "user_id":"1", parameter "page" for pagination
~~~bash
GET http://localhost:3000/api/advertisements
~~~
Response
~~~bash
[
  {
    "id":1,
    "user_id":1,
    "category_id":1,
    "name":"Pranck Miller Square 6010 K SC",
    "avatars_attributes":[
                          {
                            "image":"/system/avatar/198/IMG_1621.JPG",
                            "current":true
                          },{
                            "image":"/system/avatar/197/IMG_1620.JPG",
                            "current":false
                          }
                        ],
    "price_on_demand":false,
    "about":"Lorem ipsum dolor ...",
    "city":"Москва",
    "country":"Россия",
    "email":"",
    "phone":"+79099780222",
    "state":"active",
    "created_at":"2015-03-11T13:08:17.132+03:00",
    "updated_at":"2015-03-11T13:17:32.463+03:00"
  }
]
~~~

# All Companies
Get all Companies. Add parameter "page":"1" for pagination 
~~~bash
GET http://localhost:3000/api/companies
~~~

Response
~~~bash
[
  {
    "id":1,
    "name":"Avalon LoreM",
    "nickname":"avalor",
    "site":"http://avalor.ru",
    "email":"info@avalor.ru",
    "phone":"+7777787777",
    "address":"Волгоградский пр.003 к5",
    "description":"Avalor - все авто!",
    "created_at":"2015-02-20T16:59:11.473+03:00",
    "updated_at":"201502-25T12:28:31.952+03:00",
    "category_id":1,
    "rank":1,
    "meta_description":null,
    "meta_keywords":null
  }
]
~~~

# All Manufacturers
Get all Manufacturers. 
~~~bash
GET http://localhost:3000/api/manufacturers
~~~

Response
~~~bash
[
  {
    "id":48,
    "name":"Audi",
    "only_rare_models":false
  },{
    "id":6,
    "name":"BMW",
    "only_rare_models":false
  }
]
~~~

# All Engines
Get all Engines. 
~~~bash
GET http://localhost:3000/api/engines
~~~

Response
~~~bash
[
  {
    "id":4,
    "name_ru":"Бензин атмосферный",
    "name_en":"Petrol",
    "transport_kind":"ground"
  },{
    "id":5,
    "name_ru":"Бензин турбо",
    "name_en":"Petrol Turbo",
    "transport_kind":"ground"
  }
]
~~~

# All Transmissions
Get all Transmissions. 
~~~bash
GET http://localhost:3000/api/transmissions
~~~

Response
~~~bash
[
  {
    "id":5,
    "name_ru":"Механическая",
    "name_en":"Manual"
  },{
    "id":3,
    "name_ru":"Автомат",
    "name_en":"Automatic"
  }
]
~~~

# Update Current_user
Update Current_user's attributes
~~~bash
PUT http://localhost:3000/api/cabinet
~~~

Request params
~~~bash
{
  name: "John",
  surname: "Doe",
  avatars_attributes: image.jpg,
  status: "Hello world!",
  backgrounds_attributes: image.jpg
}
~~~

# Create Transport
Create new Current_user's Transport
~~~bash
POST http://localhost:3000/api/transports
~~~

Request params
~~~bash
{
  manufacturer_id: 1,
  model: "Continental GT",
  engine_id: 5,
  transmission_id: 3,
  about: "Самая полная,салон Mulliner,сосояние идеал",
  power: "560",
  max_speed: "340",
  wheel_drive: "all_permanent",
  acceleration: "4",
  engine_volume: "6.0",
  production_year: "2007",
  kind: "ground"
}
~~~

Authentication https://github.com/lynndylanhurley/devise_token_auth#usage-tldr


```
