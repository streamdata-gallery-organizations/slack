{
  "info": {
    "name": "Slack Delete File",
    "_postman_id": "a9cb2034-42b1-41e7-8164-ef2fa38b0b56",
    "description": "Deletes a file.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "messaging",
      "item": [
        {
          "id": "79410b6f-fcbc-4924-9190-9e9c1bbcc376",
          "name": "files_delete",
          "request": {
            "url": "http://slack.com/api/files.delete",
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
                  "description": "ID of file to delete"
                }
              ]
            },
            "description": "Deletes a file"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "3fedaf0c-b2a3-4342-a5f6-bf524db42237"
            }
          ]
        }
      ]
    }
  ]
}