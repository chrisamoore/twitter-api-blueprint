FORMAT: 1A
HOST: http://api.twitter.dev/v1/tweets

# twitter-API
twitter [API Blueprint](http://apiblueprint.org).

API Mock available @ [mock.twitter.dev/tweets](http://mock.twitter.dev/tweets)

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
                "type" : "reply"
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





### Remove a Tweet [DELETE]
+ Response 200
    + Body

            {
              "data": "4",
              "message": "Tweet deleted successfully."
            }
