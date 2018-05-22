{
  "info": {
    "name": "Slack Remove User From Conversation",
    "_postman_id": "9f9c6731-f312-411c-b4f7-e1f1cc5aae73",
    "description": "Removes a user from a conversation.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "messaging",
      "item": [
        {
          "id": "9191ef22-339c-4745-b9d8-c636a2f48d7f",
          "name": "conversations_kick",
          "request": {
            "url": "http://slack.com/api/conversations.kick",
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
                  "description": "ID of conversation to remove user from"
                },
                {
                  "key": "user",
                  "value": "{}",
                  "disabled": false,
                  "description": "User ID to be removed"
                }
              ]
            },
            "description": "Removes a user from a conversation"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "7ad02be4-d313-41b3-af69-460ea71f1fb8"
            }
          ]
        }
      ]
    }
  ]
}