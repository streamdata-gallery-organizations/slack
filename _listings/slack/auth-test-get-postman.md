{
  "info": {
    "name": "Slack Test Auth",
    "_postman_id": "40695cf9-84d5-4250-8aa1-bd6a9437f64f",
    "description": "Checks authentication & identity.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "messaging",
      "item": [
        {
          "id": "3047e70d-066a-476f-8eb7-e7ba3a19b446",
          "name": "auth_test",
          "request": {
            "url": "http://slack.com/api/auth.test",
            "method": "GET",
            "header": [
              {
                "key": "token",
                "value": "{}",
                "description": "Authentication token",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Checks authentication & identity"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "cd034db6-9bb1-472e-9f5e-1faef47bde8e"
            }
          ]
        }
      ]
    }
  ]
}