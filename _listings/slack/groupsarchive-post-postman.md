{
  "info": {
    "name": "Slack",
    "_postman_id": "bef6e286-247a-4fc9-91aa-f59d098871bb",
    "description": "One way to interact with the Slack platform is its HTTP RPC-based Web API, a collection of methods requiring OAuth 2.0-based user, bot, or workspace tokens blessed with related OAuth scopes.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "messaging",
      "item": [
        {
          "id": "f5ba1583-0049-43d0-b549-140f74828a00",
          "name": "groups_archive",
          "request": {
            "url": "http://slack.com/api/groups.archive",
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
                  "description": "Private channel to archive"
                }
              ]
            },
            "description": "Archives a private channel"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "7ed8b144-4edf-468a-b819-7d5c6e151f35"
            }
          ]
        }
      ]
    }
  ]
}