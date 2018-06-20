{
  "info": {
    "name": "Slack Get Channel",
    "_postman_id": "803a181a-d4b3-4f38-a210-87165ca02d90",
    "description": "Gets information about a channel.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "messaging",
      "item": [
        {
          "id": "e834a96d-3909-4226-ac14-eafb06d4fc95",
          "name": "channels_info",
          "request": {
            "url": "http://slack.com/api/channels.info?channel=%7B%7D&include_locale=%7B%7D&token=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Gets information about a channel"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "ff3cb5ab-054f-493b-8911-6aaa0a98177c"
            }
          ]
        }
      ]
    }
  ]
}