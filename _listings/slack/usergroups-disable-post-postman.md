{
  "info": {
    "name": "Slack Disable Group",
    "_postman_id": "0b6f467b-09a5-46c2-adae-9ebbaca7ac1f",
    "description": "Disable an existing User Group",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "messaging",
      "item": [
        {
          "id": "e981d98c-d9d2-4b15-a445-5de81b834aa2",
          "name": "usergroups_disable",
          "request": {
            "url": "http://slack.com/api/usergroups.disable",
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
                  "key": "include_count",
                  "value": "{}",
                  "disabled": false,
                  "description": "Include the number of users in the User Group"
                },
                {
                  "key": "usergroup",
                  "value": "{}",
                  "disabled": false,
                  "description": "The encoded ID of the User Group to disable"
                }
              ]
            },
            "description": "Disable an existing User Group"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "4bcc8152-aa51-4699-95b7-d6fda3bff762"
            }
          ]
        }
      ]
    }
  ]
}