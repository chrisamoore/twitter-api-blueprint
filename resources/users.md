FORMAT: 1A
HOST: http://api.twitter.dev/v1/users

# twitter-API
twitter [API Blueprint](http://apiblueprint.org).

API Mock available @ [mock.twitter.dev/users](http://mock.twitter.dev/users)

# Group Users

## Users [/users]
### Users Collection [GET]
+ Response 200 (application/json)
    + Body

            {
                "data": [
                    {
                        "id": 1,
                        "email": "nickknol@gmail.com",
                        "handle": "nickknol",
                        "profile_photo": "http://lorempixel.com/400/200",
                        "background_photo": "http://lorempixel.com/400/200",
                        "bio": "Blah blah blah, this is a block of text",
                        "website": "http://www.xkcd.com",
                        "active": true,
                        "created_at": "2014-05-23 21:06:05",
                        "updated_at": "2014-05-23 21:06:05",
                        "_links": {
                            "rel": "self",
                            "uri": "http://api.twitter.dev/v1/users/1"
                        }
                    },
                    {
                        "id": 2,
                        "email": "chrisamoore@gmail.com",
                        "handle": "cmoore",
                        "profile_photo": "http://lorempixel.com/400/200",
                        "background_photo": "http://lorempixel.com/400/200",
                        "bio": "Blah blah blah, this is a block of text",
                        "website": "http://www.xkcd.com",
                        "active": true,
                        "created_at": "2014-05-23 21:06:05",
                        "updated_at": "2014-05-23 21:06:05",
                        "_links": {
                            "rel": "self",
                            "uri": "http://api.twitter.dev/v1/users/2"
                        }
                    },
                    {
                        "id": 3,
                        "email": "justinwoodcock@gmail.com",
                        "handle": "thewoodcock",
                        "profile_photo": "http://lorempixel.com/400/200",
                        "background_photo": "http://lorempixel.com/400/200",
                        "bio": "Blah blah blah, this is a block of text",
                        "website": "http://www.xkcd.com",
                        "active": true,
                        "created_at": "2014-05-23 21:06:05",
                        "updated_at": "2014-05-23 21:06:05",
                        "_links": {
                            "rel": "self",
                            "uri": "http://api.twitter.dev/v1/users/3"
                        }
                    }
                ],
                "embeds": [
                    "tweets",
                    "favorites",
                    "messages"
                ]
            }





### Create a User [POST]

+ Request (application/json)
    + Body

            {
                "data": {
                    "id": 7,
                    "email": "newuser@gmail.com",
                    "active": true,
                    "activation_token": "",
                    "created_at": "2014-08-14 00:53:54",
                    "updated_at": "2014-08-14 00:53:54",
                    "_links": {
                        "rel": "self",
                        "uri": "/users/7"
                    }
                }
            }

+ Response 200 (application/json)
    + Body

            {
                "data": {
                    "id": 4,
                    "email": "newuser@gmail.com",
                    "handle": "newuser",
                    "profile_photo": "http://lorempixel.com/400/200",
                    "background_photo": "http://lorempixel.com/400/200",
                    "bio": "Blah blah blah, this is a block of text",
                    "website": "http://www.xkcd.com",
                    "active": true,
                    "created_at": "2014-05-23 21:06:05",
                    "updated_at": "2014-05-23 21:06:05",
                    "_links": {
                        "rel": "self",
                        "uri": "http://api.twitter.dev/v1/users/4"
                    }
                }
            }





## User [/users/{id}]
A single User object with all its details

+ Parameters
    + id (required, number, `4`) ... User ID



### Retrieve a User [GET]
+ Response 200 (application/json)
    + Body

            {
                "data": [
                    {
                        "id": 4,
                        "email": "newuser@gmail.com",
                        "handle": "newuser",
                        "profile_photo": "http://lorempixel.com/400/200",
                        "background_photo": "http://lorempixel.com/400/200",
                        "bio": "Blah blah blah, this is a block of text",
                        "website": "http://www.xkcd.com",
                        "active": true,
                        "created_at": "2014-05-23 21:06:05",
                        "updated_at": "2014-05-23 21:06:05",
                        "_links": {
                            "rel": "self",
                            "uri": "http://api.twitter.dev/v1/users/4"
                        }
                    }
                ],
                "embeds": [
                    "tweets",
                    "favorites"
                    "messages"
                ]
            }
            
            
            
### Remove a User [DELETE]
+ Response 200
    + Body

            {
              "data": "4",
              "message": "User deleted successfully."
            }


## Users [/users/{id}/tweets]
Gets all tweets for one user
+ Parameters
    + id (required, number, `1`) ... User ID
    
### Retrieve a Users tweets [GET]
+ Response 200 (application/json)
    + Body

            {
                data: [
                    {
                        id: 1
                        user_id: 1
                        original_tweet_id: 0
                        message: "Facere a laudantium voluptas minima itaque."
                        created_at: "2014-08-14 00:56:02"
                        _links: {
                            rel: "self"
                            uri: "\/tweets\/1"
                        }
                    },
                    {
                        id: 2
                        user_id: 1
                        original_tweet_id: 0
                        message: "Nisi saepe dolorem eaque alias explicabo fugiat."
                        created_at: "2014-08-14 00:56:02"
                        _links: {
                            rel: "self"
                            uri: "\/tweets\/2"
                        }
                    }
                ]
            }



## Users [/users/{id}/messagesfrom]
Gets all messages from a user
+ Parameters
    + id (required, number, `1`) ... User ID
    
### Retrieve a Users outbox [GET]
+ Response 200 (application/json)
    + Body

            {
                "data": [
                    {
                        "id": 1,
                        "from_user_id": 1,
                        "to_user_id": 3,
                        "message": "Quia iste tenetur nesciunt aut in impedit delectus.",
                        "created_at": "2014-08-14 00:56:02",
                        "_links": {
                            "rel": "self",
                            "uri": "/messages/1"
                        }
                    },
                    {
                        "id": 2,
                        "from_user_id": 1,
                        "to_user_id": 3,
                        "message": "Temporibus quam eum similique nemo.",
                        "created_at": "2014-08-14 00:56:02",
                        "_links": {
                            "rel": "self",
                            "uri": "/messages/2"
                        }
                    },
                    {
                        "id": 3,
                        "from_user_id": 1,
                        "to_user_id": 1,
                        "message": "Molestias non perferendis facilis et.",
                        "created_at": "2014-08-14 00:56:02",
                        "_links": {
                            "rel": "self",
                            "uri": "/messages/3"
                        }
                    }
                ]
            }


## Users [/users/{id}/messagesto]
Gets all messages to a user
+ Parameters
    + id (required, number, `1`) ... User ID
    
### Retrieve a Users inbox [GET]
+ Response 200 (application/json)
    + Body

            {
                "data": [
                    {
                        "id": 1,
                        "from_user_id": 1,
                        "to_user_id": 3,
                        "message": "Quia iste tenetur nesciunt aut in impedit delectus.",
                        "created_at": "2014-08-14 00:56:02",
                        "_links": {
                            "rel": "self",
                            "uri": "/messages/1"
                        }
                    },
                    {
                        "id": 2,
                        "from_user_id": 1,
                        "to_user_id": 3,
                        "message": "Temporibus quam eum similique nemo.",
                        "created_at": "2014-08-14 00:56:02",
                        "_links": {
                            "rel": "self",
                            "uri": "/messages/2"
                        }
                    },
                    {
                        "id": 3,
                        "from_user_id": 1,
                        "to_user_id": 1,
                        "message": "Molestias non perferendis facilis et.",
                        "created_at": "2014-08-14 00:56:02",
                        "_links": {
                            "rel": "self",
                            "uri": "/messages/3"
                        }
                    }
                ]
            }
            
            
## Users [/users/{id}/favorites]
Gets all favorites for a user
+ Parameters
    + id (required, number, `1`) ... User ID
    
### Retrieve a Users favorite tweets [GET]
+ Response 200 (application/json)
    + Body    

            {
                "data": [
                    {
                        "id": 0,
                        "user_id": 1,
                        "original_tweet_id": 0,
                        "message": "Nisi saepe dolorem eaque alias explicabo fugiat.",
                        "created_at": "",
                        "_links": {
                            "rel": "self",
                            "uri": "/tweets/"
                        }
                    },
                    {
                        "id": 0,
                        "user_id": 1,
                        "original_tweet_id": 0,
                        "message": "Porro temporibus aliquam suscipit inventore architecto ut deserunt.",
                        "created_at": "",
                        "_links": {
                            "rel": "self",
                            "uri": "/tweets/"
                        }
                    },
                    {
                        "id": 0,
                        "user_id": 1,
                        "original_tweet_id": 0,
                        "message": "Ratione officiis provident eius aut in quos.",
                        "created_at": "",
                        "_links": {
                            "rel": "self",
                            "uri": "/tweets/"
                        }
                    }
                ]
            }




### Update a User [PUT]
+ Request (application/json)
    + Body

            {
                "website": "http://www.penny-arcade.com"
            }

+ Response 200
    + Body

            {
                "data": {
                        "id": 4,
                        "email": "newuser@gmail.com",
                        "handle": "newuser",
                        "profile_photo": "http://lorempixel.com/400/200",
                        "background_photo": "http://lorempixel.com/400/200",
                        "bio": "Blah blah blah, this is a block of text",
                        "website": "http://www.penny-arcade.com",
                        "active": true,
                        "created_at": "2014-05-23 21:06:05",
                        "updated_at": "2014-05-23 21:06:05",
                        "_links": {
                            "rel": "self",
                            "uri": "http://api.twitter.dev/v1/users/4"
                        }
                },
                "embeds": [
                    "tweets",
                    "favorites",
                    "messages"
                ]
            }


