{
  "info": {
    "name": "Slack Create Group",
    "_postman_id": "cdb5a22c-12c1-4c1f-93e9-68c3ebef5740",
    "description": "Create a User Group",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "messaging",
      "item": [
        {
          "id": "b3c8937d-ad17-449a-99af-d48ce9328137",
          "name": "usergroups_create",
          "request": {
            "url": "http://slack.com/api/usergroups.create",
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
                  "key": "channels",
                  "value": "{}",
                  "disabled": false,
                  "description": "A comma separated string of encoded channel IDs for which the User Group uses as a default"
                },
                {
                  "key": "description",
                  "value": "{}",
                  "disabled": false,
                  "description": "A short description of the User Group"
                },
                {
                  "key": "handle",
                  "value": "{}",
                  "disabled": false,
                  "description": "A mention handle"
                },
                {
                  "key": "include_count",
                  "value": "{}",
                  "disabled": false,
                  "description": "Include the number of users in each User Group"
                },
                {
                  "key": "name",
                  "value": "{}",
                  "disabled": false,
                  "description": "A name for the User Group"
                }
              ]
            },
            "description": "Create a User Group"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "2727a8e2-ebba-48f9-9612-f5b8876f1f46"
            }
          ]
        }
      ]
    }
  ]
}