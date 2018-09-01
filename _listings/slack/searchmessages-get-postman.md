{
  "info": {
    "name": "Slack Search Real Time Messaging",
    "_postman_id": "f51e728a-7da5-4993-9ddd-180dd5eb6e12",
    "description": "Searches for messages matching a query.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "messaging",
      "item": [
        {
          "id": "f3e29339-b848-4ad3-85c4-cb6baab9e1d7",
          "name": "search_messages",
          "request": {
            "url": "http://slack.com/api/search.messages?count=%7B%7D&highlight=%7B%7D&page=%7B%7D&query=%7B%7D&sort=%7B%7D&sort_dir=%7B%7D&token=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Searches for messages matching a query"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "1e7e04ab-bbdb-4d88-b8c0-52473ccfc430"
            }
          ]
        }
      ]
    }
  ]
}