{
  "info": {
    "name": "Slack Leave Channel",
    "_postman_id": "3a11e165-b3bb-46b2-ad85-ad76141029c2",
    "description": "Leaves a channel.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "messaging",
      "item": [
        {
          "id": "2ff29c19-3c4f-4f77-b062-6d31fe68f4a6",
          "name": "channels_leave",
          "request": {
            "url": "http://slack.com/api/channels.leave",
            "method": "POST",
            "header": [
              {
                "key": "token",
                "value": "{}",
                "description": "Authentication token",
                "disabled": false
              }
            ],
            "body": {
              "mode": "urlencoded",
              "urlencoded": [
                {
                  "key": "channel",
                  "value": "{}",
                  "disabled": false,
                  "description": "Channel to leave"
                }
              ]
            },
            "description": "Leaves a channel"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "2a90a8dc-4825-4e97-8137-935425f22fac"
            }
          ]
        }
      ]
    }
  ]
}