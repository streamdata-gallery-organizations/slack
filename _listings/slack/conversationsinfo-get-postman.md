{
  "info": {
    "name": "Slack Get Conversation",
    "_postman_id": "9e1a92c3-57b4-47b3-9af4-c082c52d10ad",
    "description": "Retrieve information about a conversation.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "messaging",
      "item": [
        {
          "id": "13186300-2a26-4ed8-8281-9b8497f9c786",
          "name": "conversations_info",
          "request": {
            "url": "http://slack.com/api/conversations.info?channel=%7B%7D&include_locale=%7B%7D&token=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Retrieve information about a conversation"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "bbaaf7e1-654b-4bfd-bb99-5a3fc8f1ad9f"
            }
          ]
        }
      ]
    }
  ]
}