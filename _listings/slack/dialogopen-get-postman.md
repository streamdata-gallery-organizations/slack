{
  "info": {
    "name": "Slack Open Dialog",
    "_postman_id": "1b1f68ab-7d86-4fb9-aa53-7889d51d5b44",
    "description": "Open a dialog with a user",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "messaging",
      "item": [
        {
          "id": "2290e4a3-38ae-4b9d-9c5e-d2533998fc0c",
          "name": "dialog_open",
          "request": {
            "url": "http://slack.com/api/dialog.open?dialog=%7B%7D&trigger_id=%7B%7D",
            "method": "GET",
            "header": [
              {
                "key": "token",
                "value": "{}",
                "description": "Authentication token",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Open a dialog with a user"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "bbb54c7b-6c5c-45bb-a387-1a611e6b748b"
            }
          ]
        }
      ]
    }
  ]
}