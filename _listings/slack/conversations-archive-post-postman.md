{
  "info": {
    "name": "Slack",
    "_postman_id": "31b745e7-1975-4d69-a0fd-a9f2cc7fcecc",
    "description": "One way to interact with the Slack platform is its HTTP RPC-based Web API, a collection of methods requiring OAuth 2.0-based user, bot, or workspace tokens blessed with related OAuth scopes.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "messaging",
      "item": [
        {
          "id": "1cb0b3ae-eb3f-4e95-85e0-ee22dffcb9eb",
          "name": "conversations_archive",
          "request": {
            "url": "http://slack.com/api/conversations.archive",
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
                  "description": "ID of conversation to archive"
                }
              ]
            },
            "description": "Archives a conversation"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "d0c9c408-8157-4879-bdfa-3610a958ac9b"
            }
          ]
        }
      ]
    }
  ]
}