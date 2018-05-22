{
  "info": {
    "name": "Slack Get User Profile",
    "_postman_id": "583342f3-9a48-45f8-b387-291f4228abf1",
    "description": "Retrieves a user's profile information.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "messaging",
      "item": [
        {
          "id": "fe839a67-af35-4243-a8b9-96fdd0dd667e",
          "name": "users_profile_get",
          "request": {
            "url": "http://slack.com/api/users.profile.get?include_labels=%7B%7D&token=%7B%7D&user=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Retrieves a user's profile information"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "4d98e094-cf0c-4de6-b276-eb547cb74985"
            }
          ]
        }
      ]
    }
  ]
}