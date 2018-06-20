{
  "info": {
    "name": "Slack Add File Comments",
    "_postman_id": "b8bb1940-28f8-4eca-8321-0dd196fa7062",
    "description": "Add a comment to an existing file.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "messaging",
      "item": [
        {
          "id": "38c21a0d-0d29-451b-8118-a79e7279c0c2",
          "name": "files_comments_add",
          "request": {
            "url": "http://slack.com/api/files.comments.add",
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
                  "key": "comment",
                  "value": "{}",
                  "disabled": false,
                  "description": "Text of the comment to add"
                },
                {
                  "key": "file",
                  "value": "{}",
                  "disabled": false,
                  "description": "File to add a comment to"
                }
              ]
            },
            "description": "Add a comment to an existing file"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "2c84ff65-9135-4177-9f38-87badad53ae7"
            }
          ]
        }
      ]
    }
  ]
}