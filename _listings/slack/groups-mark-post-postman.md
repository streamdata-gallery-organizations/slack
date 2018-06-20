{
  "info": {
    "name": "Slack Mark Group",
    "_postman_id": "c496d806-ece3-4fd9-bb43-bcbd0fa4387b",
    "description": "Sets the read cursor in a private channel.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "messaging",
      "item": [
        {
          "id": "6e986bd4-3a39-4b49-8b29-175f3a78b2ab",
          "name": "groups_mark",
          "request": {
            "url": "http://slack.com/api/groups.mark",
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
                  "description": "Private channel to set reading cursor in"
                },
                {
                  "key": "ts",
                  "value": "{}",
                  "disabled": false,
                  "description": "Timestamp of the most recently seen message"
                }
              ]
            },
            "description": "Sets the read cursor in a private channel"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "5f5ef821-ee16-4d63-aebc-1c31d71f839f"
            }
          ]
        }
      ]
    }
  ]
}