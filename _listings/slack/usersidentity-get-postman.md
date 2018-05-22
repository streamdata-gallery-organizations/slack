{
  "info": {
    "name": "Slack Get User Identity",
    "_postman_id": "25a79544-c9c1-4b38-a68e-ecd8226c645e",
    "description": "Get a user's identity.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "messaging",
      "item": [
        {
          "id": "be7dbbc4-ee94-4306-8c2d-53c5b48b3dee",
          "name": "users_identity",
          "request": {
            "url": "http://slack.com/api/users.identity?token=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Get a user's identity"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "0e5ac2f8-951f-41d8-b69a-36390a4e64a1"
            }
          ]
        }
      ]
    }
  ]
}