{
  "info": {
    "name": "Slack Rename Channel",
    "_postman_id": "fe185f26-34cc-476d-b2d6-00a7faa53523",
    "description": "Renames a channel.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "messaging",
      "item": [
        {
          "id": "3bf7a6c3-772f-406a-a569-b1dd0b3f6a8a",
          "name": "channels_rename",
          "request": {
            "url": "http://slack.com/api/channels.rename",
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
                  "description": "Channel to rename"
                },
                {
                  "key": "name",
                  "value": "{}",
                  "disabled": false,
                  "description": "New name for channel"
                },
                {
                  "key": "validate",
                  "value": "{}",
                  "disabled": false,
                  "description": "Whether to return errors on invalid channel name instead of modifying it to meet the specified criteria"
                }
              ]
            },
            "description": "Renames a channel"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "531249e8-46e7-401b-af5c-10532a82805f"
            }
          ]
        }
      ]
    }
  ]
}