{
  "info": {
    "name": "Slack Get Group",
    "_postman_id": "368e2544-33de-429d-8495-559824e9fe67",
    "description": "Lists private channels that the calling user has access to.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "messaging",
      "item": [
        {
          "id": "eb63233b-9405-4041-9fa5-fc3807a4d450",
          "name": "groups_list",
          "request": {
            "url": "http://slack.com/api/groups.list?exclude_archived=%7B%7D&exclude_members=%7B%7D&token=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Lists private channels that the calling user has access to"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "e43dba80-dafd-439f-912a-e5aaebefc697"
            }
          ]
        }
      ]
    }
  ]
}