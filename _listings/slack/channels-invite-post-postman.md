{
  "info": {
    "name": "Slack Invite Channel User",
    "_postman_id": "0e086f0a-d52b-40a4-a4f5-8308748e0c77",
    "description": "Invites a user to a channel.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "messaging",
      "item": [
        {
          "id": "4b0798ec-eab1-43a5-bbbb-b56c49813868",
          "name": "channels_invite",
          "request": {
            "url": "http://slack.com/api/channels.invite",
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
                  "description": "Channel to invite user to"
                },
                {
                  "key": "user",
                  "value": "{}",
                  "disabled": false,
                  "description": "User to invite to channel"
                }
              ]
            },
            "description": "Invites a user to a channel"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "b7779c94-bb09-4de4-acbe-075bfcd02aa2"
            }
          ]
        }
      ]
    }
  ]
}