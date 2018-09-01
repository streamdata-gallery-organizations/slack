{
  "info": {
    "name": "Slack Make User Inactive",
    "_postman_id": "f1e51c3d-570c-48a3-8eca-e3b6b185e05f",
    "description": "Marks a user as active.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "messaging",
      "item": [
        {
          "id": "93fdaba9-e55f-45be-a29b-808c7d02ac02",
          "name": "users_setActive",
          "request": {
            "url": "http://slack.com/api/users.setActive",
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
              "mode": "raw"
            },
            "description": "Marks a user as active"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "c27f5557-2f3a-4e53-9472-56a634560c72"
            }
          ]
        }
      ]
    }
  ]
}