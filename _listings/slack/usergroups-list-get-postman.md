{
  "info": {
    "name": "Slack List Groups",
    "_postman_id": "56305ad7-a681-4fd3-98d1-8a682189cfc0",
    "description": "List all User Groups for a team",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "messaging",
      "item": [
        {
          "id": "d6cfc7ae-f38e-424f-993c-cb15cc82e150",
          "name": "usergroups_list",
          "request": {
            "url": "http://slack.com/api/usergroups.list?include_count=%7B%7D&include_disabled=%7B%7D&include_users=%7B%7D&token=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "List all User Groups for a team"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "b3e0b6f3-31b6-4467-8603-b6b2b147e295"
            }
          ]
        }
      ]
    }
  ]
}