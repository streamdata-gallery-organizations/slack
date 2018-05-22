{
  "info": {
    "name": "Slack Get Conversation History",
    "_postman_id": "cc7bb8d5-fc02-4c6f-bd52-82bd99b99833",
    "description": "Fetches a conversation's history of messages and events.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "messaging",
      "item": [
        {
          "id": "ead318a5-7097-4c4e-af48-49f1d1120612",
          "name": "conversations_history",
          "request": {
            "url": "http://slack.com/api/conversations.history?channel=%7B%7D&cursor=%7B%7D&inclusive=%7B%7D&latest=%7B%7D&limit=%7B%7D&oldest=%7B%7D&token=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Fetches a conversation's history of messages and events"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "249575d0-3017-4d0c-b641-b98fe42aced7"
            }
          ]
        }
      ]
    }
  ]
}