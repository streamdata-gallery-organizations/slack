{
  "info": {
    "name": "Slack Create Group",
    "_postman_id": "58e0e620-3118-4462-987e-2b71d07b28d6",
    "description": "Creates a private channel.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "messaging",
      "item": [
        {
          "id": "c43a9474-b275-44d9-8d0b-789d689a1b75",
          "name": "groups_create",
          "request": {
            "url": "http://slack.com/api/groups.create",
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
                  "description": "Name of private channel to create"
                },
                {
                  "key": "validate",
                  "value": "{}",
                  "disabled": false,
                  "description": "Whether to return errors on invalid channel name instead of modifying it to meet the specified criteria"
                }
              ]
            },
            "description": "Creates a private channel"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "c9dae1d8-9fc4-43a4-89bd-7893e1637cb4"
            }
          ]
        }
      ]
    }
  ]
}