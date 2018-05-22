{
  "info": {
    "name": "Slack Get Team Logs",
    "_postman_id": "8e9d94d2-09f0-4dc3-acc1-37d6123e34c9",
    "description": "Gets the integration logs for the current team.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "messaging",
      "item": [
        {
          "id": "14e02af1-06a9-42cc-9793-aee2a2539c90",
          "name": "team_integrationLogs",
          "request": {
            "url": "http://slack.com/api/team.integrationLogs?app_id=%7B%7D&change_type=%7B%7D&count=%7B%7D&page=%7B%7D&service_id=%7B%7D&token=%7B%7D&user=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Gets the integration logs for the current team"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "e3c7ca0b-e619-4643-8340-37b6a3cd5cff"
            }
          ]
        }
      ]
    }
  ]
}