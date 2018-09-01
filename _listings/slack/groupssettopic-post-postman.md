{
  "info": {
    "name": "Slack Set Group Topic",
    "_postman_id": "eeefc9cb-2437-4312-96de-d4b9b5f89770",
    "description": "Sets the topic for a private channel.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "messaging",
      "item": [
        {
          "id": "56d6c165-732c-46ce-953a-376deedf7143",
          "name": "groups_setTopic",
          "request": {
            "url": "http://slack.com/api/groups.setTopic",
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
                  "description": "Private channel to set the topic of"
                },
                {
                  "key": "topic",
                  "value": "{}",
                  "disabled": false,
                  "description": "The new topic"
                }
              ]
            },
            "description": "Sets the topic for a private channel"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "081375cf-01e5-438b-a15d-4ffe578a2e93"
            }
          ]
        }
      ]
    }
  ]
}