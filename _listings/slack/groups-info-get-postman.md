{
  "info": {
    "name": "Slack Get Group",
    "_postman_id": "c500c56a-d75d-4c83-8747-cc161f47023e",
    "description": "Gets information about a private channel.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "messaging",
      "item": [
        {
          "id": "7917e202-5e47-4324-b137-94558ebe1a90",
          "name": "groups_info",
          "request": {
            "url": "http://slack.com/api/groups.info?channel=%7B%7D&include_locale=%7B%7D&token=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Gets information about a private channel"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "c81cdbef-9155-4051-b1b9-6a80ed2d3ef3"
            }
          ]
        }
      ]
    }
  ]
}