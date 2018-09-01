{
  "info": {
    "name": "Slack Get Bot Info",
    "_postman_id": "b149793e-e5c2-4d1c-96c0-de9209b64e00",
    "description": "Gets information about a bot user.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "messaging",
      "item": [
        {
          "id": "d7a3edd4-5737-465a-8605-58e51d4ad003",
          "name": "bots_info",
          "request": {
            "url": "http://slack.com/api/bots.info?bot=%7B%7D&token=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Gets information about a bot user"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "e61ddf9e-c46c-4579-99db-fafb5979cfa6"
            }
          ]
        }
      ]
    }
  ]
}