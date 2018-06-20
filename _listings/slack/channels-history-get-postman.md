{
  "info": {
    "name": "Slack Get Channel History",
    "_postman_id": "b86052dc-2966-4abe-8050-ee8a60524d62",
    "description": "Fetches history of messages and events from a channel.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "messaging",
      "item": [
        {
          "id": "815da35d-89e8-4881-a873-dd664ee7ba7d",
          "name": "channels_history",
          "request": {
            "url": "http://slack.com/api/channels.history?channel=%7B%7D&count=%7B%7D&inclusive=%7B%7D&latest=%7B%7D&oldest=%7B%7D&token=%7B%7D&unreads=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Fetches history of messages and events from a channel"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "51717b81-212e-4ba6-9008-430f27ed6543"
            }
          ]
        }
      ]
    }
  ]
}