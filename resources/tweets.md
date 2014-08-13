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
                        "user_id": 24,
                        "message": "This weeks SDPHP MeetUp: @camdesigns "API's: You're doing it wrong" hosted at Variable Action Office RSVP today http://ow.ly/A5Gtf ",
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
                        "message": "Love APIs and our product? We're looking for a dev evangelist. Full time SF. jobs@apiary.io",
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
                        "message": "Using Dredd, our testing tool? We'd love to talk to you! Send us what your experience is.",
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





### Create a Tweet [POST]

+ Request (application/json)
    + Body

            {
                "message" : "Using Dredd, our testing tool? We'd love to talk to you! Send us what your experience is.",
                "original_tweet_id": null 
            }

+ Response 200 (application/json)
    + Body

           {
                "id": 1890,
                "user_id": 24,
                "message": "Using Dredd, our testing tool? We'd love to talk to you! Send us what your experience is.",
                "original_tweet_id": 1,
                "created_at": "2014-05-23 21:06:05"
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
                "data": [
                    {
                        "id": 1890,
                        "user_id": 24,
                        "message": "Using Dredd, our testing tool? We'd love to talk to you! Send us what your experience is.",
                        "original_tweet_id": 1,
                        "created_at": "2014-05-23 21:06:05"
                        "_links": {
                            "rel": "self",
                            "uri": "http://api.twitter.dev/v1/tweets/1890"
                        }
                    }
                ],
                "embeds": [
                    "user"
                ]
            }





### Remove a Tweet [DELETE]
+ Response 200
    + Body

            {
              "data": "1890",
              "message": "Tweet deleted successfully."
            }
