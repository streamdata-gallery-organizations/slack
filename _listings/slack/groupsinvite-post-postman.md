{
  "info": {
    "name": "Slack Invite User To Group",
    "_postman_id": "724e199e-8503-4e7d-af89-a6c676e9c225",
    "description": "Invites a user to a private channel.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "messaging",
      "item": [
        {
          "id": "059c79be-1071-466a-941c-8836064bbf3f",
          "name": "groups_invite",
          "request": {
            "url": "http://slack.com/api/groups.invite",
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
                  "description": "Private channel to invite user to"
                },
                {
                  "key": "user",
                  "value": "{}",
                  "disabled": false,
                  "description": "User to invite"
                }
              ]
            },
            "description": "Invites a user to a private channel"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "26c64be1-eeb4-4b2a-9de8-bf5781d5f096"
            }
          ]
        }
      ]
    }
  ]
}