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
