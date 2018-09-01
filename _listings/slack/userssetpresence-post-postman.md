{
  "info": {
    "name": "Slack Set User Presence",
    "_postman_id": "d1931712-768b-445e-aec8-df2c0e42c74b",
    "description": "Manually sets user presence.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "messaging",
      "item": [
        {
          "id": "4edc767b-b294-4662-94da-326a9daef7cc",
          "name": "users_setPresence",
          "request": {
            "url": "http://slack.com/api/users.setPresence",
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
                  "key": "presence",
                  "value": "{}",
                  "disabled": false,
                  "description": "Either `auto` or `away`"
                }
              ]
            },
            "description": "Manually sets user presence"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "5669e992-d51e-492a-a03e-36f1e390530b"
            }
          ]
        }
      ]
    }
  ]
}