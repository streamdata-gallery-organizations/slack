{
  "info": {
    "name": "Slack",
    "_postman_id": "59959e35-7b99-4568-a983-1a6d380828f9",
    "description": "One way to interact with the Slack platform is its HTTP RPC-based Web API, a collection of methods requiring OAuth 2.0-based user, bot, or workspace tokens blessed with related OAuth scopes.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "messaging",
      "item": [
        {
          "id": "2d1496a1-94c1-457d-9d9c-626d63ff5e9d",
          "name": "groups_createChild",
          "request": {
            "url": "http://slack.com/api/groups.createChild",
            "method": "POST",
            "body": {
              "mode": "urlencoded",
              "urlencoded": [
                {
                  "key": "channel",
                  "value": "{}",
                  "disabled": false,
                  "description": "Private channel to clone and archive"
                },
                {
                  "key": "token",
                  "value": "{}",
                  "disabled": false,
                  "description": "Authentication token"
                }
              ]
            },
            "description": "Clones and archives a private channel"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "e9ea06ac-d9c7-401a-8502-ced07c0fef91"
            }
          ]
        }
      ]
    }
  ]
}