{
  "info": {
    "name": "Slack Set Channel Topic",
    "_postman_id": "ef3da998-6394-44a4-81f3-a7a5126ad3d8",
    "description": "Sets the topic for a channel.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "messaging",
      "item": [
        {
          "id": "7cd3c1fd-590f-46bb-921b-0531d04e13c6",
          "name": "channels_setTopic",
          "request": {
            "url": "http://slack.com/api/channels.setTopic",
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
                  "description": "Channel to set the topic of"
                },
                {
                  "key": "topic",
                  "value": "{}",
                  "disabled": false,
                  "description": "The new topic"
                }
              ]
            },
            "description": "Sets the topic for a channel"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "7eb99ac7-84f3-43cf-99a5-26cdb67aaadf"
            }
          ]
        }
      ]
    }
  ]
}