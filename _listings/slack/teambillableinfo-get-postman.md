{
  "info": {
    "name": "Slack Get Billable Info",
    "_postman_id": "4e96fef8-47e1-43f9-936a-dce15ea76052",
    "description": "Gets billable users information for the current team.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "messaging",
      "item": [
        {
          "id": "e1c3bf99-446f-4b37-90ce-a5fccca44626",
          "name": "team_billableInfo",
          "request": {
            "url": "http://slack.com/api/team.billableInfo?token=%7B%7D&user=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Gets billable users information for the current team"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "ed2282e7-4c6e-4664-afeb-75d6d0d3ebd6"
            }
          ]
        }
      ]
    }
  ]
}