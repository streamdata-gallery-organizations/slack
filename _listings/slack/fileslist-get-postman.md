{
  "info": {
    "name": "Slack List Files",
    "_postman_id": "3732aeb1-ef6c-4dff-973e-bd6f61a4ca44",
    "description": "Lists & filters team files.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "messaging",
      "item": [
        {
          "id": "bd3bb064-7335-4e43-96d3-7e8842feb85f",
          "name": "files_list",
          "request": {
            "url": "http://slack.com/api/files.list?channel=%7B%7D&count=%7B%7D&page=%7B%7D&token=%7B%7D&ts_from=%7B%7D&ts_to=%7B%7D&types=%7B%7D&user=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Lists & filters team files"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "c1bc181d-7497-4bf6-94b6-b096f6eb86e3"
            }
          ]
        }
      ]
    }
  ]
}