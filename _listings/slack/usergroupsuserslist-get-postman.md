{
  "info": {
    "name": "Slack List Group Users",
    "_postman_id": "c6ae2a10-2ad0-4b40-9ff0-a1fe2daa5faf",
    "description": "List all users in a User Group",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "messaging",
      "item": [
        {
          "id": "a6183d4b-bd6b-44a1-84ba-fb827081b62e",
          "name": "usergroups_users_list",
          "request": {
            "url": "http://slack.com/api/usergroups.users.list?include_disabled=%7B%7D&token=%7B%7D&usergroup=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "List all users in a User Group"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "dddaaa45-814f-4da1-ba18-2214f95f35fe"
            }
          ]
        }
      ]
    }
  ]
}