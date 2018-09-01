{
  "info": {
    "name": "Slack List Reactions",
    "_postman_id": "e137e417-3bc0-4c16-abc8-4177d7d4bafb",
    "description": "Lists reactions made by a user.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Messaging",
      "item": [
        {
          "id": "f0eefae9-42fe-4299-94c0-3528154eae2a",
          "name": "reactions_list",
          "request": {
            "url": "http://slack.com/api/reactions.list?count=%7B%7D&full=%7B%7D&page=%7B%7D&token=%7B%7D&user=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Lists reactions made by a user."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "4cb6156d-9e89-4d92-a2b2-954fc9eadbb4"
            }
          ]
        }
      ]
    }
  ]
}