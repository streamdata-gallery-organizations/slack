{
  "info": {
    "name": "Slack List Team Users",
    "_postman_id": "d177e60f-1a9f-46f0-b02a-973a2aa4b228",
    "description": "Lists all users in a Slack team.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "messaging",
      "item": [
        {
          "id": "2c67fc7b-a181-42f1-979f-856f6c417df5",
          "name": "users_list",
          "request": {
            "url": "http://slack.com/api/users.list?cursor=%7B%7D&include_locale=%7B%7D&limit=%7B%7D&presence=%7B%7D&token=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Lists all users in a Slack team"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "6ae5009d-481d-4263-b912-e3b8dc2df170"
            }
          ]
        }
      ]
    }
  ]
}