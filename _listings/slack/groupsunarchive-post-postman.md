{
  "info": {
    "name": "Slack",
    "_postman_id": "9608a29a-fbdf-46b8-8359-6a87ed4061eb",
    "description": "One way to interact with the Slack platform is its HTTP RPC-based Web API, a collection of methods requiring OAuth 2.0-based user, bot, or workspace tokens blessed with related OAuth scopes.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "messaging",
      "item": [
        {
          "id": "d4ceab91-b0f0-411b-8c58-a8010c5ab28e",
          "name": "groups_unarchive",
          "request": {
            "url": "http://slack.com/api/groups.unarchive",
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
                  "description": "Private channel to unarchive"
                }
              ]
            },
            "description": "Unarchives a private channel"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "94cad6b8-4ff4-455d-98c0-c9852f0ccf8b"
            }
          ]
        }
      ]
    }
  ]
}