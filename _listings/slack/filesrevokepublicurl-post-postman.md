{
  "info": {
    "name": "Slack Revoke Public URL",
    "_postman_id": "f15c836d-56b3-4514-8761-ce79ebb799eb",
    "description": "Revokes public/external sharing access for a file",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "messaging",
      "item": [
        {
          "id": "39f5bfd7-b208-44d5-8de9-c88fc45aceca",
          "name": "files_revokePublicURL",
          "request": {
            "url": "http://slack.com/api/files.revokePublicURL",
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
                  "key": "file",
                  "value": "{}",
                  "disabled": false,
                  "description": "File to revoke"
                }
              ]
            },
            "description": "Revokes public/external sharing access for a file"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "7921a83a-5935-438c-bcdc-a191ec46cfb3"
            }
          ]
        }
      ]
    }
  ]
}