{
  "info": {
    "name": "Slack Add Reaction",
    "_postman_id": "da06d73a-5ef7-4297-926a-a076320a0a5f",
    "description": "Adds a reaction to an item.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Messaging",
      "item": [
        {
          "id": "1e93727e-9759-4aae-8bd2-aa60da434028",
          "name": "reactions_list",
          "request": {
            "url": "http://slack.com/api/reactions.list?count=%7B%7D&full=%7B%7D&page=%7B%7D&token=%7B%7D&user=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Lists reactions made by a user."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "3fcea3d2-9cd7-4973-b7d5-084bea583448"
            }
          ]
        },
        {
          "id": "21462c3a-3952-48e0-8f6b-b24ccb96953b",
          "name": "reactions_add",
          "request": {
            "url": "http://slack.com/api/reactions.add",
            "method": "POST",
            "header": [
              {
                "key": "token",
                "value": "{}",
                "description": "Authentication token",
                "disabled": false
              }
            ],
            "body": {
              "mode": "urlencoded",
              "urlencoded": [
                {
                  "key": "channel",
                  "value": "{}",
                  "disabled": false,
                  "description": "Channel where the message to add reaction to was posted"
                },
                {
                  "key": "file",
                  "value": "{}",
                  "disabled": false,
                  "description": "File to add reaction to"
                },
                {
                  "key": "file_comment",
                  "value": "{}",
                  "disabled": false,
                  "description": "File comment to add reaction to"
                },
                {
                  "key": "name",
                  "value": "{}",
                  "disabled": false,
                  "description": "Reaction (emoji) name"
                },
                {
                  "key": "timestamp",
                  "value": "{}",
                  "disabled": false,
                  "description": "Timestamp of the message to add reaction to"
                }
              ]
            },
            "description": "Adds a reaction to an item."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "95affee8-3401-424e-a10b-ab9b37f899c2"
            }
          ]
        }
      ]
    }
  ]
}