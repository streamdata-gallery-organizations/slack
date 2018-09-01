{
  "info": {
    "name": "Slack Start Real Time Messaging Files",
    "_postman_id": "67c26f46-3196-46f4-8af7-5a6938b780db",
    "description": "Searches for files matching a query.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "messaging",
      "item": [
        {
          "id": "0c517bf2-1c2e-4732-afae-bb8083020f6a",
          "name": "search_files",
          "request": {
            "url": "http://slack.com/api/search.files?count=%7B%7D&highlight=%7B%7D&page=%7B%7D&query=%7B%7D&sort=%7B%7D&sort_dir=%7B%7D&token=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Searches for files matching a query"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "f4357945-5a1b-4927-a734-b0668c3f59a7"
            }
          ]
        }
      ]
    }
  ]
}