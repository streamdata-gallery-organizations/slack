{
  "info": {
    "name": "Slack Revoke Auth",
    "_postman_id": "e92b28fd-c18c-4028-b1d2-1e41a5cbd754",
    "description": "Revokes a token.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "messaging",
      "item": [
        {
          "id": "bc90c170-8686-428c-aad4-03babc9a9639",
          "name": "auth_revoke",
          "request": {
            "url": "http://slack.com/api/auth.revoke?test=%7B%7D&token=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Revokes a token"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "02467a29-fac9-4235-aa0c-a282c28a9636"
            }
          ]
        }
      ]
    }
  ]
}