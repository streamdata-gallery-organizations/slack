{
  "info": {
    "name": "Slack Start Real Time Messaging",
    "_postman_id": "8b3693c2-cfc8-4313-969f-681cf0a2f6b3",
    "description": "Starts a Real Time Messaging session.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "messaging",
      "item": [
        {
          "id": "74866461-92f6-4fbc-b76d-0a056950bc4d",
          "name": "rtm_start",
          "request": {
            "url": "http://slack.com/api/rtm.start?batch_presence_aware=%7B%7D&include_locale=%7B%7D&mpim_aware=%7B%7D&no_latest=%7B%7D&no_unreads=%7B%7D&simple_latest=%7B%7D&token=%7B%7D",
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
              "id": "b1ca3cb8-b307-4d43-81e2-36ad015e7fad"
            }
          ]
        }
      ]
    }
  ]
}