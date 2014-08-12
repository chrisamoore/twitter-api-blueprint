FORMAT: 1A
HOST: http://api.twitter.dev

# twitter-API
twitter [API Blueprint](http://apiblueprint.org).

API Mock available @ [mock.twitter.](http://mock.twitter.dev)

# Group Users

## Users [/users]
### Users Collection [GET]
+ Response 200 (application/json)
    + Body

            {
                "data": [
                    {
                        "id": 1,
                        "email": "admin@twitter.com",
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
                        "email": "supervisor@twitter.com",
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
                        "email": "manager@twitter.com",
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
                    "retweets",
                    "replies"
                ]
            }

### Create a User [POST]

+ Request (application/json)
    + Body

            {
                "handle" : "@camdesigns",
                "email": "cmoore@twitter.com",
                "password": "1l1k3pupp135"
            }

+ Response 200 (application/json)
    + Body

            {
                "data": {
                    "id": 11,
                    "email": "cmoore@twitter.com",
                    "handle" : "@camdesigns",
                    "active": false,
                    "created_at": "2014-05-23 21:06:05",
                    "updated_at": "2014-05-23 21:06:05",
                    "_links": {
                        "rel": "self",
                        "uri": "http://api.twitter.dev/v1/users/1"
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
                        "email": "admin@twitter.com",
                        "active": true,
                        "created_at": "2014-05-23 21:06:05",
                        "updated_at": "2014-05-23 21:06:05",
                        "_links": {
                            "rel": "self",
                            "uri": "http://api.twitter.dev/v1/users/1"
                        }
                    }
                ],
                "embeds": [
                    "tweets",
                    "favorites",
                    "retweets",
                    "replies"
                ]
            }

### Remove a User [DELETE]
+ Response 200
    + Body

            {
              "data": "4",
              "message": "User deleted successfully."
            }

## User's Followers [/users/{id}/followers]
### User's Followers Collection [GET]
+ Response 200 (application/json)
    + Body

            {
                "data": [
                    {
                        "id": 1,
                        "email": "admin@twitter.com",
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
                        "email": "supervisor@twitter.com",
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
                        "email": "manager@twitter.com",
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
                    "retweets",
                    "replies"
                ]
            }

## User's Mentions [/users/{id}/mentions]
### User's Mentions Collection [GET]
+ Response 200 (application/json)
    + Body

            {
                "data": [
                    {
                        "id": 187,
                        "message": "free cialis",
                        "type": "retweet",
                        "tweet_id": 1,
                        "created_at": "2014-05-23 21:06:05",
                        "updated_at": "2014-05-23 21:06:05",
                        "_links": {
                            "rel": "self",
                            "uri": "http://api.twitter.dev/v1/tweets/187"
                        }
                    },
                    {
                        "id": 18,
                        "message": "free cialis",
                        "type": "reply",
                        "tweet_id": 1,
                        "created_at": "2014-05-23 21:06:05",
                        "updated_at": "2014-05-23 21:06:05",
                        "_links": {
                            "rel": "self",
                            "uri": "http://api.twitter.dev/v1/tweets/18"
                        }
                    },
                    {
                        "id": 1001,
                        "message": "free cialis",
                        "type": "tweet",
                        "tweet_id": 1,
                        "created_at": "2014-05-23 21:06:05",
                        "updated_at": "2014-05-23 21:06:05",
                        "_links": {
                            "rel": "self",
                            "uri": "http://api.twitter.dev/v1/tweets/1001"
                        }
                    },
                    {
                        "id": 324,
                        "message": "free cialis",
                        "type": "favorite",
                        "tweet_id": 1,
                        "created_at": "2014-05-23 21:06:05",
                        "updated_at": "2014-05-23 21:06:05",
                        "_links": {
                            "rel": "self",
                            "uri": "http://api.twitter.dev/v1/tweets/324"
                        }
                    },
                ],
                "embeds": [
                    "user",
                    "favorites",
                    "retweets",
                    "replies"
                ]
            }

## User's tweets [/users/{id}/tweets]
### User's tweets Collection [GET]
+ Response 200 (application/json)
    + Body

            {
                "data": [
                    {
                        "id": 187,
                        "message": "free cialis",
                        "type": "retweet",
                        "tweet_id": 1,
                        "created_at": "2014-05-23 21:06:05",
                        "updated_at": "2014-05-23 21:06:05",
                        "_links": {
                            "rel": "self",
                            "uri": "http://api.twitter.dev/v1/tweets/187"
                        }
                    },
                    {
                        "id": 18,
                        "message": "free cialis",
                        "type": "reply",
                        "tweet_id": 1,
                        "created_at": "2014-05-23 21:06:05",
                        "updated_at": "2014-05-23 21:06:05",
                        "_links": {
                            "rel": "self",
                            "uri": "http://api.twitter.dev/v1/tweets/18"
                        }
                    },
                    {
                        "id": 1001,
                        "message": "free cialis",
                        "type": "tweet",
                        "tweet_id": 1,
                        "created_at": "2014-05-23 21:06:05",
                        "updated_at": "2014-05-23 21:06:05",
                        "_links": {
                            "rel": "self",
                            "uri": "http://api.twitter.dev/v1/tweets/1001"
                        }
                    },
                    {
                        "id": 324,
                        "message": "free cialis",
                        "type": "favorite",
                        "tweet_id": 1,
                        "created_at": "2014-05-23 21:06:05",
                        "updated_at": "2014-05-23 21:06:05",
                        "_links": {
                            "rel": "self",
                            "uri": "http://api.twitter.dev/v1/tweets/324"
                        }
                    },
                ],
                "embeds": [
                    "user",
                    "favorites",
                    "retweets",
                    "replies"
                ]
            }

# Group Tweets

## Tweets [/tweets]
### Tweets Collection [GET]
+ Response 200 (application/json)
    + Body

            {
                "data": [
                    {
                        "id": 187,
                        "message": "free cialis",
                        "type": "retweet",
                        "tweet_id": 1,
                        "created_at": "2014-05-23 21:06:05",
                        "updated_at": "2014-05-23 21:06:05",
                        "_links": {
                            "rel": "self",
                            "uri": "http://api.twitter.dev/v1/tweets/187"
                        }
                    },
                    {
                        "id": 18,
                        "message": "free cialis",
                        "type": "reply",
                        "tweet_id": 1,
                        "created_at": "2014-05-23 21:06:05",
                        "updated_at": "2014-05-23 21:06:05",
                        "_links": {
                            "rel": "self",
                            "uri": "http://api.twitter.dev/v1/tweets/18"
                        }
                    },
                    {
                        "id": 1001,
                        "message": "free cialis",
                        "type": "tweet",
                        "tweet_id": 1,
                        "created_at": "2014-05-23 21:06:05",
                        "updated_at": "2014-05-23 21:06:05",
                        "_links": {
                            "rel": "self",
                            "uri": "http://api.twitter.dev/v1/tweets/1001"
                        }
                    },
                    {
                        "id": 324,
                        "message": "free cialis",
                        "type": "favorite",
                        "tweet_id": 1,
                        "created_at": "2014-05-23 21:06:05",
                        "updated_at": "2014-05-23 21:06:05",
                        "_links": {
                            "rel": "self",
                            "uri": "http://api.twitter.dev/v1/tweets/324"
                        }
                    },
                ],
                "embeds": [
                    "user",
                    "favorites",
                    "retweets",
                    "replies"
                ]
            }

### Create a Tweet [POST]

+ Request (application/json)
    + Body

            {
                "message" : "Quick get your free trial.",
                "image_url" : "http://google.com/image/1",
                "type" : "reply",
                "tweet_id" : 1
            }

+ Response 200 (application/json)
    + Body

           {
                "id": 1890,
                "message": "Quick get your free trial.",
                "type": "reply",
                "tweet_id": 1,
                "created_at": "2014-05-23 21:06:05",
                "updated_at": "2014-05-23 21:06:05",
                "_links": {
                    "rel": "self",
                    "uri": "http://api.twitter.dev/v1/tweets/1890"
                }
            }

## Tweet [/tweets/{id}]
A single Tweet object with all its details

+ Parameters
    + id (required, number, `1890`) ... Tweet ID

### Retrieve a Tweet [GET]
+ Response 200 (application/json)
    + Body

            {
                "data": [{
                            "id": 1890,
                            "message": "Quick get your free trial.",
                            "type": "reply",
                            "tweet_id": 1,
                            "created_at": "2014-05-23 21:06:05",
                            "updated_at": "2014-05-23 21:06:05",
                            "_links": {
                                "rel": "self",
                                "uri": "http://api.twitter.dev/v1/tweets/1890"
                            }
                }],
                "embeds": [
                    "tweets",
                    "favorites",
                    "retweets",
                    "replies"
                ]
            }

### Update a Tweet [PUT]
+ Request (application/json)
    + Body

            {
                "message" : "Quick get your paid trial.",
            }

+ Response 200 (application/json)
    + Body

            {
                "data": [{
                            "id": 1890,
                            "message": "Quick get your paid trial.",
                            "type": "reply",
                            "tweet_id": 1,,
                            "created_at": "2014-05-23 21:06:05",
                            "updated_at": "2014-05-23 21:06:05",
                            "_links": {
                                "rel": "self",
                                "uri": "http://api.twitter.dev/v1/tweets/1890"
                            }
                }],
                "embeds": [
                    "tweets",
                    "favorites",
                    "retweets",
                    "replies"
                ]
            }

### Remove a Tweet [DELETE]
+ Response 200
    + Body

            {
              "data": "4",
              "message": "Tweet deleted successfully."
            }

## Tweet's favorites [/tweets/{id}/favorites]
### Tweet's favorites Collection [GET]
+ Response 200 (application/json)
    + Body

            {
                "data": [
                    {
                        "id": 187,
                        "message": "free cialis",
                        "type": "retweet",
                        "tweet_id": 1,
                        "created_at": "2014-05-23 21:06:05",
                        "updated_at": "2014-05-23 21:06:05",
                        "_links": {
                            "rel": "self",
                            "uri": "http://api.twitter.dev/v1/tweets/187"
                        }
                    },
                    {
                        "id": 18,
                        "message": "free cialis",
                        "type": "reply",
                        "tweet_id": 1,
                        "created_at": "2014-05-23 21:06:05",
                        "updated_at": "2014-05-23 21:06:05",
                        "_links": {
                            "rel": "self",
                            "uri": "http://api.twitter.dev/v1/tweets/18"
                        }
                    },
                    {
                        "id": 1001,
                        "message": "free cialis",
                        "type": "tweet",
                        "tweet_id": 1,
                        "created_at": "2014-05-23 21:06:05",
                        "updated_at": "2014-05-23 21:06:05",
                        "_links": {
                            "rel": "self",
                            "uri": "http://api.twitter.dev/v1/tweets/1001"
                        }
                    },
                    {
                        "id": 324,
                        "message": "free cialis",
                        "type": "favorite",
                        "tweet_id": 1,
                        "created_at": "2014-05-23 21:06:05",
                        "updated_at": "2014-05-23 21:06:05",
                        "_links": {
                            "rel": "self",
                            "uri": "http://api.twitter.dev/v1/tweets/324"
                        }
                    },
                ],
                "embeds": [
                    "user",
                    "favorites",
                    "retweets",
                    "replies"
                ]
            }

## Tweet's retweets [/tweets/{id}/retweets]
### Tweet's retweets Collection [GET]
+ Response 200 (application/json)
    + Body

            {
                "data": [
                    {
                        "id": 187,
                        "message": "free cialis",
                        "type": "retweet",
                        "tweet_id": 1,
                        "created_at": "2014-05-23 21:06:05",
                        "updated_at": "2014-05-23 21:06:05",
                        "_links": {
                            "rel": "self",
                            "uri": "http://api.twitter.dev/v1/tweets/187"
                        }
                    },
                    {
                        "id": 18,
                        "message": "free cialis",
                        "type": "reply",
                        "tweet_id": 1,
                        "created_at": "2014-05-23 21:06:05",
                        "updated_at": "2014-05-23 21:06:05",
                        "_links": {
                            "rel": "self",
                            "uri": "http://api.twitter.dev/v1/tweets/18"
                        }
                    },
                    {
                        "id": 1001,
                        "message": "free cialis",
                        "type": "tweet",
                        "tweet_id": 1,
                        "created_at": "2014-05-23 21:06:05",
                        "updated_at": "2014-05-23 21:06:05",
                        "_links": {
                            "rel": "self",
                            "uri": "http://api.twitter.dev/v1/tweets/1001"
                        }
                    },
                    {
                        "id": 324,
                        "message": "free cialis",
                        "type": "favorite",
                        "tweet_id": 1,
                        "created_at": "2014-05-23 21:06:05",
                        "updated_at": "2014-05-23 21:06:05",
                        "_links": {
                            "rel": "self",
                            "uri": "http://api.twitter.dev/v1/tweets/324"
                        }
                    },
                ],
                "embeds": [
                    "user",
                    "favorites",
                    "retweets",
                    "replies"
                ]
            }

## Tweet's replies [/tweets/{id}/replies]
### Tweet's replies Collection [GET]
+ Response 200 (application/json)
    + Body

            {
                "data": [
                    {
                        "id": 187,
                        "message": "free cialis",
                        "type": "retweet",
                        "tweet_id": 1,
                        "created_at": "2014-05-23 21:06:05",
                        "updated_at": "2014-05-23 21:06:05",
                        "_links": {
                            "rel": "self",
                            "uri": "http://api.twitter.dev/v1/tweets/187"
                        }
                    },
                    {
                        "id": 18,
                        "message": "free cialis",
                        "type": "reply",
                        "tweet_id": 1,
                        "created_at": "2014-05-23 21:06:05",
                        "updated_at": "2014-05-23 21:06:05",
                        "_links": {
                            "rel": "self",
                            "uri": "http://api.twitter.dev/v1/tweets/18"
                        }
                    },
                    {
                        "id": 1001,
                        "message": "free cialis",
                        "type": "tweet",
                        "tweet_id": 1,
                        "created_at": "2014-05-23 21:06:05",
                        "updated_at": "2014-05-23 21:06:05",
                        "_links": {
                            "rel": "self",
                            "uri": "http://api.twitter.dev/v1/tweets/1001"
                        }
                    },
                    {
                        "id": 324,
                        "message": "free cialis",
                        "type": "favorite",
                        "tweet_id": 1,
                        "created_at": "2014-05-23 21:06:05",
                        "updated_at": "2014-05-23 21:06:05",
                        "_links": {
                            "rel": "self",
                            "uri": "http://api.twitter.dev/v1/tweets/324"
                        }
                    },
                ],
                "embeds": [
                    "user",
                    "favorites",
                    "retweets",
                    "replies"
                ]
            }

## Tweets by hashtag Collection [/tweets/{hashtag}]
### Tweets by hashtag Collection [GET]
+ Response 200 (application/json)
    + Body

            {
                "data": [
                    {
                        "id": 187,
                        "message": "free cialis",
                        "type": "retweet",
                        "tweet_id": 1,
                        "created_at": "2014-05-23 21:06:05",
                        "updated_at": "2014-05-23 21:06:05",
                        "_links": {
                            "rel": "self",
                            "uri": "http://api.twitter.dev/v1/tweets/187"
                        }
                    },
                    {
                        "id": 18,
                        "message": "free cialis",
                        "type": "reply",
                        "tweet_id": 1,
                        "created_at": "2014-05-23 21:06:05",
                        "updated_at": "2014-05-23 21:06:05",
                        "_links": {
                            "rel": "self",
                            "uri": "http://api.twitter.dev/v1/tweets/18"
                        }
                    },
                    {
                        "id": 1001,
                        "message": "free cialis",
                        "type": "tweet",
                        "tweet_id": 1,
                        "created_at": "2014-05-23 21:06:05",
                        "updated_at": "2014-05-23 21:06:05",
                        "_links": {
                            "rel": "self",
                            "uri": "http://api.twitter.dev/v1/tweets/1001"
                        }
                    },
                    {
                        "id": 324,
                        "message": "free cialis",
                        "type": "favorite",
                        "tweet_id": 1,
                        "created_at": "2014-05-23 21:06:05",
                        "updated_at": "2014-05-23 21:06:05",
                        "_links": {
                            "rel": "self",
                            "uri": "http://api.twitter.dev/v1/tweets/324"
                        }
                    },
                ],
                "embeds": [
                    "user",
                    "favorites",
                    "retweets",
                    "replies"
                ]
            }

