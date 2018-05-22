{
  "info": {
    "name": "Slack Get User Info",
    "_postman_id": "690f987e-4d60-484c-a7a3-f8d8dc192a20",
    "description": "Gets information about a user.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "messaging",
      "item": [
        {
          "id": "75a55cb3-4b74-4986-aa20-e345065b4752",
          "name": "users_info",
          "request": {
            "url": "http://slack.com/api/users.info?include_locale=%7B%7D&token=%7B%7D&user=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Gets information about a user"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "7ae0ff21-2f1b-4468-93e5-a91ba84eb8f6"
            }
          ]
        }
      ]
    }
  ]
}