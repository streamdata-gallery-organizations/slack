{
  "info": {
    "name": "Slack Set Conversation Purpose",
    "_postman_id": "2346b404-5596-4140-a58f-473bc16f0f2c",
    "description": "Sets the purpose for a conversation.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "messaging",
      "item": [
        {
          "id": "d4c7b37b-9715-473c-86af-69b415014044",
          "name": "conversations_setPurpose",
          "request": {
            "url": "http://slack.com/api/conversations.setPurpose",
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
                  "description": "Conversation to set the purpose of"
                },
                {
                  "key": "purpose",
                  "value": "{}",
                  "disabled": false,
                  "description": "A new, specialer purpose"
                }
              ]
            },
            "description": "Sets the purpose for a conversation"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "df4bae27-a72e-45a0-8aa5-840e5582ecdd"
            }
          ]
        }
      ]
    }
  ]
}