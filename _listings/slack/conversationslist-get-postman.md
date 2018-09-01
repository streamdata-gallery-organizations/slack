{
  "info": {
    "name": "Slack List Conversations",
    "_postman_id": "c7e80f6a-7b9f-4676-9d45-287d8a44ee46",
    "description": "Lists all channels in a Slack team.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "messaging",
      "item": [
        {
          "id": "6630009d-ef08-49b5-b4dd-f94fc1d68526",
          "name": "conversations_list",
          "request": {
            "url": "http://slack.com/api/conversations.list?cursor=%7B%7D&exclude_archived=%7B%7D&limit=%7B%7D&token=%7B%7D&types=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Lists all channels in a Slack team"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "3be0f807-0de0-4d78-bb77-ca6dda73d26f"
            }
          ]
        }
      ]
    }
  ]
}