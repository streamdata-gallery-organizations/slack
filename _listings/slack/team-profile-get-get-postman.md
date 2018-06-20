{
  "info": {
    "name": "Slack Get Team Profile",
    "_postman_id": "4c31b154-6021-4495-a129-72ea96d6171f",
    "description": "Retrieve a team's profile.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "messaging",
      "item": [
        {
          "id": "f25db4c5-c81b-4c16-9a19-7a3331f2931b",
          "name": "team_profile_get",
          "request": {
            "url": "http://slack.com/api/team.profile.get?token=%7B%7D&visibility=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Retrieve a team's profile"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "24c3c64b-b239-45eb-aa2c-6c1f0f059b42"
            }
          ]
        }
      ]
    }
  ]
}