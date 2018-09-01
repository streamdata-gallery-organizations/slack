{
  "info": {
    "name": "Slack List Channels",
    "_postman_id": "a88c9bcf-9c0c-4739-aef0-e8b62df68fc2",
    "description": "Lists all channels in a Slack team.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "messaging",
      "item": [
        {
          "id": "7c7a73c2-278c-4d78-8351-e0178c48b130",
          "name": "channels_list",
          "request": {
            "url": "http://slack.com/api/channels.list?cursor=%7B%7D&exclude_archived=%7B%7D&exclude_members=%7B%7D&limit=%7B%7D&token=%7B%7D",
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
              "id": "a44c8a15-c8d2-46fb-a07e-92e4048e9b9d"
            }
          ]
        }
      ]
    }
  ]
}