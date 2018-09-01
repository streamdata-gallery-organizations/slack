{
  "info": {
    "name": "Slack Get Group Thread",
    "_postman_id": "29a995e7-24cd-4dcc-ae04-1a4b6e8af52c",
    "description": "Retrieve a thread of messages posted to a private channel",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "messaging",
      "item": [
        {
          "id": "876d61e5-f1b3-4456-8cf7-b4a5eaa8042c",
          "name": "groups_replies",
          "request": {
            "url": "http://slack.com/api/groups.replies?channel=%7B%7D&thread_ts=%7B%7D&token=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Retrieve a thread of messages posted to a private channel"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "cd68cbc9-62c3-4970-9b0f-e53942125f93"
            }
          ]
        }
      ]
    }
  ]
}