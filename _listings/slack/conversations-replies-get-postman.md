{
  "info": {
    "name": "Slack Reply Conversation",
    "_postman_id": "97d3a838-10a0-4c0d-8118-c418a23f7f7b",
    "description": "Retrieve a thread of messages posted to a conversation",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "messaging",
      "item": [
        {
          "id": "41deeb0b-dcac-43ca-a976-f5d9d5a58ca8",
          "name": "conversations_replies",
          "request": {
            "url": "http://slack.com/api/conversations.replies?channel=%7B%7D&cursor=%7B%7D&inclusive=%7B%7D&latest=%7B%7D&limit=%7B%7D&oldest=%7B%7D&token=%7B%7D&ts=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Retrieve a thread of messages posted to a conversation"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "b23aa58f-d256-4cd0-9c7c-014110a042c5"
            }
          ]
        }
      ]
    }
  ]
}