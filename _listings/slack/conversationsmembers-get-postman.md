{
  "info": {
    "name": "Slack Get Conversation Members",
    "_postman_id": "83b1cfed-29c5-41a5-afda-b6d4374a2501",
    "description": "Retrieve members of a conversation.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "messaging",
      "item": [
        {
          "id": "b1ce7897-b658-4529-8fcf-e76568a460fa",
          "name": "conversations_members",
          "request": {
            "url": "http://slack.com/api/conversations.members?channel=%7B%7D&cursor=%7B%7D&limit=%7B%7D&token=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Retrieve members of a conversation"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "8706db8a-a32b-4674-9af9-6f3491265ec6"
            }
          ]
        }
      ]
    }
  ]
}