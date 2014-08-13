FORMAT: 1A
HOST: http://api.twitter.dev/v1/messages

# twitter-API
twitter [API Blueprint](http://apiblueprint.org).

API Mock available @ [mock.twitter.dev/users](http://mock.twitter.dev/messages)

# Group Messages

## Users [/messages]
### Users Collection [GET]
+ Response 200 (application/json)
    + Body

            {
                "data": [
                    {
                        "id": 1,
                        "from_user_id": 1,
                        "to_user_id": 2,
                        "message": "Blah blah blah, this is a new message",
                        "created_at": "2014-05-23 21:06:05",
                        "_links": {
                            "rel": "self",
                            "uri": "http://api.twitter.dev/v1/messages/1"
                        }
                    },
                    {
                        "id": 2,
                        "from_user_id": 2,
                        "to_user_id": 3,
                        "message": "Blah blah blah, this is a new message",
                        "created_at": "2014-05-23 21:06:05",
                        "_links": {
                            "rel": "self",
                            "uri": "http://api.twitter.dev/v1/messages/2"
                        }
                    },
                    {
                        "id": 3,
                        "from_user_id": 1,
                        "to_user_id": 3,
                        "message": "Blah blah blah, this is a new message",
                        "created_at": "2014-05-23 21:06:05",
                        "_links": {
                            "rel": "self",
                            "uri": "http://api.twitter.dev/v1/messages/3"
                        }
                    }
                ],
                "embeds": [
                    "from_user",
                    "to_user"
                ]
            }





### Create a Message [POST]

+ Request (application/json)
    + Body

            {
                "to_user_id": 3,
                "from_user_id": 2,
                "message": "This is a new message to user three."
            }

+ Response 200 (application/json)
    + Body

            {
                "data": {
                    "id": 4,
                    "from_user_id": 1,
                    "to_user_id": 3,
                    "message": "This is a new message to user three.",
                    "created_at": "2014-05-23 21:06:05",
                    "_links": {
                        "rel": "self",
                        "uri": "http://api.twitter.dev/v1/messages/4"
                    }
                }
            }





## User [/users/{id}]
A single Message object with all its details

+ Parameters
    + id (required, number, `4`) ... Message ID



### Retrieve a Message [GET]
+ Response 200 (application/json)
    + Body

            {
                "data": [
                    {
                        "id": 4,
                        "from_user_id": 1,
                        "to_user_id": 3,
                        "message": "This is a new message to user three.",
                        "created_at": "2014-05-23 21:06:05",
                        "_links": {
                            "rel": "self",
                            "uri": "http://api.twitter.dev/v1/messages/4"
                        }
                    }
                ],
                "embeds": [
                    "from_user",
                    "to_user"
                ]
            }





### Remove a Message [DELETE]
+ Response 200
    + Body

            {
              "data": "4",
              "message": "Message deleted successfully."
            }
