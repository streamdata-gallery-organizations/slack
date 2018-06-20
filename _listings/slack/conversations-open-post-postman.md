{
  "info": {
    "name": "Slack Open Conversation",
    "_postman_id": "6dd6e03b-0aa9-447e-bc8e-00f1f570be53",
    "description": "Opens or resumes a direct message or multi-person direct message.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "messaging",
      "item": [
        {
          "id": "e3ca0909-c342-469f-9922-431504b63d4e",
          "name": "conversations_open",
          "request": {
            "url": "http://slack.com/api/conversations.open",
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
                  "description": "Resume a conversation by supplying an `im` or `mpim`'s ID"
                },
                {
                  "key": "return_im",
                  "value": "{}",
                  "disabled": false,
                  "description": "Boolean, indicates you want the full IM channel definition in the response"
                },
                {
                  "key": "users",
                  "value": "{}",
                  "disabled": false,
                  "description": "Comma separated lists of users"
                }
              ]
            },
            "description": "Opens or resumes a direct message or multi-person direct message"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "aeec7351-993c-4ea5-af09-47c76f130676"
            }
          ]
        }
      ]
    }
  ]
}