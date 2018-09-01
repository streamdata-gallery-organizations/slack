{
  "info": {
    "name": "Slack Join Conversation",
    "_postman_id": "09020386-4724-47a1-8e37-a2e4ba4a553e",
    "description": "Joins an existing conversation.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "messaging",
      "item": [
        {
          "id": "86b3c50f-7b9f-47ec-8b85-677368d20a12",
          "name": "conversations_join",
          "request": {
            "url": "http://slack.com/api/conversations.join",
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
                  "description": "ID of conversation to join"
                }
              ]
            },
            "description": "Joins an existing conversation"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "b9292344-ae7a-4d30-8159-63f0e996758a"
            }
          ]
        }
      ]
    }
  ]
}