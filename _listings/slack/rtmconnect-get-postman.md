{
  "info": {
    "name": "Slack Connect Real Time Messaging",
    "_postman_id": "e71e4bdd-8567-48ed-b488-86e83b4af06f",
    "description": "Starts a Real Time Messaging session.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "messaging",
      "item": [
        {
          "id": "850fee56-cccf-495e-bc79-ee9500da09a7",
          "name": "rtm_connect",
          "request": {
            "url": "http://slack.com/api/rtm.connect?batch_presence_aware=%7B%7D&token=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Starts a Real Time Messaging session"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "0f0d4d3c-92c0-49bd-8efd-247840629f16"
            }
          ]
        }
      ]
    }
  ]
}