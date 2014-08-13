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
                "email": "newuser@gmail.com",
                "handle": "newuser",
                "profile_photo": "http://lorempixel.com/400/200",
                "background_photo": "http://lorempixel.com/400/200",
                "bio": "Blah blah blah, this is a block of text",
                "website": "http://www.xkcd.com",
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


### Remove a User [DELETE]
+ Response 200
    + Body

            {
              "data": "4",
              "message": "User deleted successfully."
            }


## User Tweets [/users/{id}/tweets]
### Tweets Collection [GET]
+ Response 200 (application/json)
    + Body

            {
                "data": [
                    {
                        "id": 187,
                        "user_id": 24,
                        "message": "free cialis",
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
                        "message": "free cialis",
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
                        "message": "free cialis",
                        "original_tweet_id": 101,
                        "created_at": "2014-05-23 21:06:05",
                        "_links": {
                            "rel": "self",
                            "uri": "http://api.twitter.dev/v1/tweets/187"
                        }
                    }
                ],
                "embeds": [
                    "user"
                ]
            }
