{
  "info": {
    "name": "Slack Join Channel",
    "_postman_id": "a0f261b2-b4e4-41fd-b0e6-f7784921538f",
    "description": "Joins a channel, creating it if needed.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "messaging",
      "item": [
        {
          "id": "76b4e4dd-a455-4452-b648-21568f2fb864",
          "name": "channels_join",
          "request": {
            "url": "http://slack.com/api/channels.join",
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
                  "key": "name",
                  "value": "{}",
                  "disabled": false,
                  "description": "Name of channel to join"
                },
                {
                  "key": "validate",
                  "value": "{}",
                  "disabled": false,
                  "description": "Whether to return errors on invalid channel name instead of modifying it to meet the specified criteria"
                }
              ]
            },
            "description": "Joins a channel, creating it if needed"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "373d4355-0904-48c7-8929-70b3e88526a7"
            }
          ]
        }
      ]
    }
  ]
}