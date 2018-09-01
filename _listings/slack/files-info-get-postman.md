{
  "info": {
    "name": "Slack Get File",
    "_postman_id": "1b15bb12-62b4-4cc8-ab0f-b80d2c71d977",
    "description": "Gets information about a team file.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "messaging",
      "item": [
        {
          "id": "5ee506f1-3f28-4093-ab2b-49fb693980e8",
          "name": "files_info",
          "request": {
            "url": "http://slack.com/api/files.info?count=%7B%7D&file=%7B%7D&page=%7B%7D&token=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Gets information about a team file"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "57cad1f1-7c6f-41bf-8ba1-584250363cc0"
            }
          ]
        }
      ]
    }
  ]
}