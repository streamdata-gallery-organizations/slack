{
  "info": {
    "name": "Slack Share Public URL",
    "_postman_id": "8f3bc9e3-8b11-417b-b14e-6f27dfd10156",
    "description": "Enables a file for public/external sharing.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "messaging",
      "item": [
        {
          "id": "c25a4666-18d9-4c11-a3b4-4d3906d86780",
          "name": "files_sharedPublicURL",
          "request": {
            "url": "http://slack.com/api/files.sharedPublicURL",
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
                  "description": "File to share"
                }
              ]
            },
            "description": "Enables a file for public/external sharing"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "d8fc9a65-3768-4746-a8fc-5d57c5982862"
            }
          ]
        }
      ]
    }
  ]
}