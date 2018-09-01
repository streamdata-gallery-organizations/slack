{
  "info": {
    "name": "Slack Close Conversation",
    "_postman_id": "b66a21c9-c3c0-48c9-ba85-61388a97893f",
    "description": "Closes a direct message or multi-person direct message.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "messaging",
      "item": [
        {
          "id": "3f537ee5-6629-4204-84e7-57558b98485a",
          "name": "conversations_close",
          "request": {
            "url": "http://slack.com/api/conversations.close",
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
                  "description": "Conversation to close"
                }
              ]
            },
            "description": "Closes a direct message or multi-person direct message"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "c1f5c6bb-cff7-4888-9073-5e2558984b68"
            }
          ]
        }
      ]
    }
  ]
}