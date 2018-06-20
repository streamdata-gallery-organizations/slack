{
  "info": {
    "name": "Slack Group History",
    "_postman_id": "a5172002-b06c-44c7-a3cf-7a3b79357db4",
    "description": "Fetches history of messages and events from a private channel.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "messaging",
      "item": [
        {
          "id": "3513fe89-a5b6-4d2f-89de-5a8fa0bf9724",
          "name": "groups_history",
          "request": {
            "url": "http://slack.com/api/groups.history?channel=%7B%7D&count=%7B%7D&inclusive=%7B%7D&latest=%7B%7D&oldest=%7B%7D&token=%7B%7D&unreads=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Fetches history of messages and events from a private channel"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "3126f89b-f534-48e5-999f-cb1751668bf4"
            }
          ]
        }
      ]
    }
  ]
}