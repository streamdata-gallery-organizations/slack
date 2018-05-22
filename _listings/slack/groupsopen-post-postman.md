{
  "info": {
    "name": "Slack Open Group",
    "_postman_id": "a8717d1e-2d7e-45f8-9c44-349d2c77f3c7",
    "description": "Opens a private channel.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "messaging",
      "item": [
        {
          "id": "5c853cd6-8e4b-4e91-86e7-6a043703059a",
          "name": "groups_open",
          "request": {
            "url": "http://slack.com/api/groups.open",
            "method": "POST",
            "header": [
              {
                "key": "token",
                "value": "{}",
                "description": "Authentication token",
                "disabled": false
              }
            ],
            "body": {
              "mode": "urlencoded",
              "urlencoded": [
                {
                  "key": "channel",
                  "value": "{}",
                  "disabled": false,
                  "description": "Private channel to open"
                }
              ]
            },
            "description": "Opens a private channel"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "f7f7d93b-6623-4468-a3e2-2feaca274f17"
            }
          ]
        }
      ]
    }
  ]
}