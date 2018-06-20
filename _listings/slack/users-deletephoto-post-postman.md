{
  "info": {
    "name": "Slack Delete Photo",
    "_postman_id": "32f2bf15-b285-411e-a299-489eb8f07b57",
    "description": "Delete the user profile photo",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "messaging",
      "item": [
        {
          "id": "83c961fd-b9ec-4cf4-bf55-e5057232659c",
          "name": "users_deletePhoto",
          "request": {
            "url": "http://slack.com/api/users.deletePhoto",
            "method": "POST",
            "body": {
              "mode": "urlencoded",
              "urlencoded": [
                {
                  "key": "token",
                  "value": "{}",
                  "disabled": false,
                  "description": "Authentication token"
                }
              ]
            },
            "description": "Delete the user profile photo"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "0ddf1be5-b89d-45cc-bde1-edf1fd6f6cd7"
            }
          ]
        }
      ]
    }
  ]
}