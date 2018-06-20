{
  "info": {
    "name": "Slack Create Channel",
    "_postman_id": "4fc182d2-e5ae-4ed0-8941-ca019463cfc7",
    "description": "Creates a channel.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "messaging",
      "item": [
        {
          "id": "5eabe16e-d119-49b6-90ba-e219cee92fc6",
          "name": "channels_create",
          "request": {
            "url": "http://slack.com/api/channels.create",
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
                  "key": "name",
                  "value": "{}",
                  "disabled": false,
                  "description": "Name of channel to create"
                },
                {
                  "key": "validate",
                  "value": "{}",
                  "disabled": false,
                  "description": "Whether to return errors on invalid channel name instead of modifying it to meet the specified criteria"
                }
              ]
            },
            "description": "Creates a channel"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "a248b044-148e-418d-b64f-c23fac4fbb25"
            }
          ]
        }
      ]
    }
  ]
}