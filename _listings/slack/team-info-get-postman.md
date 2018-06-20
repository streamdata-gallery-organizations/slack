{
  "info": {
    "name": "Slack Get Team",
    "_postman_id": "ce1323a7-6659-46ce-9cc7-2bd4b3f86652",
    "description": "Gets information about the current team.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "messaging",
      "item": [
        {
          "id": "1eb9198d-227f-4252-8f2d-fb4cc5f21d05",
          "name": "team_info",
          "request": {
            "url": "http://slack.com/api/team.info?token=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Gets information about the current team"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "168fa22d-2f93-4aa3-8283-be5a14ca8b97"
            }
          ]
        }
      ]
    }
  ]
}