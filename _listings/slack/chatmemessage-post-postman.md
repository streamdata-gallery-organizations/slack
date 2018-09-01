{
  "info": {
    "name": "Slack Share Message",
    "_postman_id": "2100f2e2-b941-483e-a7af-a074a61b6656",
    "description": "Share a me message into a channel.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "messages",
      "item": [
        {
          "id": "684b8520-8ac5-40a0-a2e0-11cc6f2b75fa",
          "name": "chat_meMessage",
          "request": {
            "url": "http://slack.com/api/chat.meMessage",
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
                  "description": "Channel to send message to"
                },
                {
                  "key": "text",
                  "value": "{}",
                  "disabled": false,
                  "description": "Text of the message to send"
                }
              ]
            },
            "description": "Share a me message into a channel"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "3b823de4-a495-4f6e-87f8-87231d5e7ea8"
            }
          ]
        }
      ]
    }
  ]
}