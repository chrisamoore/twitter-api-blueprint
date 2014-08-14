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
                        "name": "Nick Knol",
                        "email": "nickknol@gmail.com",
                        "handle": "nickknol",
                        "profile_photo": "http://lorempixel.com/200/200",
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
                        "name": "Chris Moore",
                        "email": "chrisamoore@gmail.com",
                        "handle": "cmoore",
                        "profile_photo": "http://lorempixel.com/200/200",
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
                        "name": "Justin Woodcock",
                        "email": "justinwoodcock@gmail.com",
                        "handle": "thewoodcock",
                        "profile_photo": "http://lorempixel.com/200/200",
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
                }
            }


### Remove a User [DELETE]
+ Response 200
    + Body

            {
              "data": "4",
              "message": "User deleted successfully."
            }


## User Tweets [/users/{id}/tweets]
+ Parameters
    + id (required, number, `1`) ... User ID
    
### Tweets Collection [GET]
+ Response 200 (application/json)
    + Body

            {
                "data": [
                    {
                        "id": 187,
                        "user_id": 24,
                        "message": "Using Dredd, our testing tool? We'd love to talk to you! Send us what your experience is.",
                        "original_tweet_id": 101,
                        "created_at": "2014-05-23 21:06:05",
                        "_links": {
                            "rel": "self",
                            "uri": "http://api.twitter.dev/v1/tweets/187"
                        }
                    },
                    {
                        "id": 188,
                        "user_id": 24,
                        "message": "This weeks SDPHP MeetUp: @camdesigns \"API's: You're doing it wrong\" hosted at Variable Action Office RSVP today http://ow.ly/A5Gtf ",
                        "original_tweet_id": 101,
                        "created_at": "2014-05-23 21:06:05",
                        "_links": {
                            "rel": "self",
                            "uri": "http://api.twitter.dev/v1/tweets/187"
                        }
                    },
                    {
                        "id": 189,
                        "user_id": 24,
                        "message": "Love APIs and our product? We're looking for a dev evangelist. Full time SF. jobs@apiary.io",
                        "original_tweet_id": 101,
                        "created_at": "2014-05-23 21:06:05",
                        "_links": {
                            "rel": "self",
                            "uri": "http://api.twitter.dev/v1/tweets/187"
                        }
                    }
                ]
            }
