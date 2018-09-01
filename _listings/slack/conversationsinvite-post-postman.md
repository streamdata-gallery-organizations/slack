{
  "info": {
    "name": "Slack Invite User To Conversation",
    "_postman_id": "bf315567-c1d4-42fd-8bde-805e14e6465d",
    "description": "Invites users to a channel.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "messaging",
      "item": [
        {
          "id": "f436c9f7-209e-4f03-b20c-e936f693f48c",
          "name": "conversations_invite",
          "request": {
            "url": "http://slack.com/api/conversations.invite",
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
                  "description": "The ID of the public or private channel to invite user(s) to"
                },
                {
                  "key": "users",
                  "value": "{}",
                  "disabled": false,
                  "description": "A comma separated list of user IDs"
                }
              ]
            },
            "description": "Invites users to a channel"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "e6014810-b3cb-442b-84e0-7b2d910cfadd"
            }
          ]
        }
      ]
    }
  ]
}