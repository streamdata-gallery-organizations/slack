{
  "info": {
    "name": "Slack Leave Conversation",
    "_postman_id": "74932445-6697-4bbe-95db-b91e59cc49cc",
    "description": "Leaves a conversation.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "messaging",
      "item": [
        {
          "id": "d30c3916-1588-496f-b0bf-13c4f3b3b586",
          "name": "conversations_leave",
          "request": {
            "url": "http://slack.com/api/conversations.leave",
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
                  "description": "Conversation to leave"
                }
              ]
            },
            "description": "Leaves a conversation"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "8d8e6042-4a12-4091-a8d6-708d2e96ca4a"
            }
          ]
        }
      ]
    }
  ]
}