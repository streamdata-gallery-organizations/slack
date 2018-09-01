{
  "info": {
    "name": "Slack Get Permalink",
    "_postman_id": "ca09d6ec-2a39-4046-9237-243f6a59917f",
    "description": "Retrieve a permalink URL for a specific extant message",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "messages",
      "item": [
        {
          "id": "4c024fe2-ada0-4335-ae44-b34ea7247156",
          "name": "chat_getPermalink",
          "request": {
            "url": "http://slack.com/api/chat.getPermalink?channel=%7B%7D&message_ts=%7B%7D&token=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Retrieve a permalink URL for a specific extant message"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "1f29b2a0-6719-4194-9884-2e839be19366"
            }
          ]
        }
      ]
    }
  ]
}