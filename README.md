# theclub_doc
docs

```
#!ruby

// DB //
rake db:remake (:drop, :create, :migrate)
rake db:reseed (:drop, :create, :migrate, :seed)

// GET   Article //
GET /api/posts/4

// GET  Articles //
GET /api/posts

// GET   Widget //
GET /api/widget/1

// GET  Widgets //
GET /api/widgets

// GET  Genres //
GET /api/genres

// GET  Topics //
GET /api/topics

// Create Article //
POST /api/posts
{
  "title":"AAAAAGGAGAGAGAG",
  "status":"pending",
  "body": "Hello world!",
  "title_type": "typical",
  "lead_status": true,
  "lead_text": "ololo trulala",
  "media_type": "keep_up",
  "caption": "Yeahhhh baby!",
  "copyright": "this is mf copyright!",
  "link_to_picture": "images/image.png",
  "template": "videos",
  "publish": 1454343135000,
  "badge": "badge badge trulalala",
  "important": false,
  "main_page": "auto_feed",
  "culture": false,
  "icon": "live_stream",
  "icon_type": "updated",
  "tizer_style": "outside",
  "status": "progress",
  "body": "There are many flowers and trees. Aston Martin, JAck Daniels, Chicken macNuggets!",
  "program_id": 1,
  "blog": true,
  "genres":[ {"id": 1},
             {"id": 3},
             {"id": 4}],
  "topics":[ {"id": 1},
             {"id": 2},
             {"id": 3}]
}


// Update Article //
PUT /api/posts/4
{
  "title":"7777777777777",
  "status":"ready",
  "body": "Hello!",
  "genres": [ {"id": 1},
              {"id": 3},
              {"id": 4}],
  "topics":[  {"id": 1},
              {"id": 2},
              {"id": 3}]
}

Authentication https://github.com/lynndylanhurley/devise_token_auth#usage-tldr


```
