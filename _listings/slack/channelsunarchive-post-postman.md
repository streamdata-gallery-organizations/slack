{
  "info": {
    "name": "Slack",
    "_postman_id": "7b348ccf-8a57-4692-9c8c-8a3ff0f679fd",
    "description": "One way to interact with the Slack platform is its HTTP RPC-based Web API, a collection of methods requiring OAuth 2.0-based user, bot, or workspace tokens blessed with related OAuth scopes.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "messaging",
      "item": [
        {
          "id": "81a3636d-9225-4c85-8e3c-e2ff40cf072f",
          "name": "channels_unarchive",
          "request": {
            "url": "http://slack.com/api/channels.unarchive",
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
                  "description": "Channel to unarchive"
                }
              ]
            },
            "description": "Unarchives a channel"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "b50e7b1b-a347-429e-8c62-f516464dda23"
            }
          ]
        }
      ]
    }
  ]
}