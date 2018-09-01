{
  "info": {
    "name": "Slack Leave Group",
    "_postman_id": "499c6643-f1af-45a2-b824-f402ebd8558a",
    "description": "Leaves a private channel.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "messaging",
      "item": [
        {
          "id": "91e8c161-e723-483e-8658-28c6eb309ff9",
          "name": "groups_leave",
          "request": {
            "url": "http://slack.com/api/groups.leave",
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
                  "description": "Private channel to leave"
                }
              ]
            },
            "description": "Leaves a private channel"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "ec28fac0-ee95-4430-bda1-3c8415ed7f0b"
            }
          ]
        }
      ]
    }
  ]
}