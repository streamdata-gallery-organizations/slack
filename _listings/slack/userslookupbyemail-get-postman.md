{
  "info": {
    "name": "Slack Find User",
    "_postman_id": "716f377a-5262-4b5d-8ed6-8fb960f449ce",
    "description": "Find a user with an email address.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "messaging",
      "item": [
        {
          "id": "6cfbabe9-91ad-4fc4-a7f7-bf7a517e7bf2",
          "name": "users_lookupByEmail",
          "request": {
            "url": "http://slack.com/api/users.lookupByEmail?email=%7B%7D&token=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Find a user with an email address"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "ad86b9f9-afe9-4c38-a535-2aee5f6e6707"
            }
          ]
        }
      ]
    }
  ]
}