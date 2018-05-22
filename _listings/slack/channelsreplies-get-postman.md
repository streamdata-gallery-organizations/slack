{
  "info": {
    "name": "Slack Get Channel Thread",
    "_postman_id": "9c3d6716-ea3c-4964-bcdb-3f7780b47518",
    "description": "Retrieve a thread of messages posted to a channel",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "messaging",
      "item": [
        {
          "id": "70a3681e-3597-4687-b17c-4feb89ca26ac",
          "name": "channels_replies",
          "request": {
            "url": "http://slack.com/api/channels.replies?channel=%7B%7D&thread_ts=%7B%7D&token=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Retrieve a thread of messages posted to a channel"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "bd110447-dc3d-4d51-986e-0a68d49d15b0"
            }
          ]
        }
      ]
    }
  ]
}