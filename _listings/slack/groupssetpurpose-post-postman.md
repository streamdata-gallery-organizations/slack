{
  "info": {
    "name": "Slack Set Group Purpose",
    "_postman_id": "9a8d1155-b8af-4a2c-9e89-5b6e415b313f",
    "description": "Sets the purpose for a private channel.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "messaging",
      "item": [
        {
          "id": "4f420131-53ef-4a77-a502-e01d8703c9bc",
          "name": "groups_setPurpose",
          "request": {
            "url": "http://slack.com/api/groups.setPurpose",
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
                  "description": "Private channel to set the purpose of"
                },
                {
                  "key": "purpose",
                  "value": "{}",
                  "disabled": false,
                  "description": "The new purpose"
                }
              ]
            },
            "description": "Sets the purpose for a private channel"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "b76696c1-2acf-4133-891c-5b89a57eac5a"
            }
          ]
        }
      ]
    }
  ]
}