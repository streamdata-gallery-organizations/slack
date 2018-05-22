{
  "info": {
    "name": "Slack Set Channel Purpose",
    "_postman_id": "749c1a98-bec7-4bc3-8a39-6d295f38be0d",
    "description": "Sets the purpose for a channel.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "messaging",
      "item": [
        {
          "id": "1e790151-0933-4e6d-8181-6352bbb85863",
          "name": "channels_setPurpose",
          "request": {
            "url": "http://slack.com/api/channels.setPurpose",
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
                  "description": "Channel to set the purpose of"
                },
                {
                  "key": "purpose",
                  "value": "{}",
                  "disabled": false,
                  "description": "The new purpose"
                }
              ]
            },
            "description": "Sets the purpose for a channel"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "26da6a5f-26cb-44b2-ab43-27c44c791bdf"
            }
          ]
        }
      ]
    }
  ]
}