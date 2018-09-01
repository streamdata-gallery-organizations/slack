{
  "info": {
    "name": "Slack Search Real Time Messaging",
    "_postman_id": "a07632ec-f18b-40db-95a1-8db8bc10e36b",
    "description": "Searches for messages and files matching a query.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "messaging",
      "item": [
        {
          "id": "664489c8-6dc6-41d6-83e2-74543528acdf",
          "name": "search_all",
          "request": {
            "url": "http://slack.com/api/search.all?count=%7B%7D&highlight=%7B%7D&page=%7B%7D&query=%7B%7D&sort=%7B%7D&sort_dir=%7B%7D&token=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Searches for messages and files matching a query"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "737b3f8b-e6e0-4486-bbad-7cb45144714f"
            }
          ]
        }
      ]
    }
  ]
}