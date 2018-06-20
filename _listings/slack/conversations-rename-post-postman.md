{
  "info": {
    "name": "Slack Rename Conversation",
    "_postman_id": "de6c40be-920d-4a59-8118-90cde21ce146",
    "description": "Renames a conversation.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "messaging",
      "item": [
        {
          "id": "09880584-f727-4ac9-bd4a-93bdd07efb0b",
          "name": "conversations_rename",
          "request": {
            "url": "http://slack.com/api/conversations.rename",
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
                  "description": "ID of conversation to rename"
                },
                {
                  "key": "name",
                  "value": "{}",
                  "disabled": false,
                  "description": "New name for conversation"
                }
              ]
            },
            "description": "Renames a conversation"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "d4f929c6-aae8-4eed-92ac-33dbae6103ba"
            }
          ]
        }
      ]
    }
  ]
}