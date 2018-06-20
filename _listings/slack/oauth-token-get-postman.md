{
  "info": {
    "name": "Slack Oauth Token",
    "_postman_id": "906f8452-eb7c-456a-a8e6-62b42b03a779",
    "description": "Exchanges a temporary OAuth verifier code for a workspace token.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Messaging",
      "item": [
        {
          "id": "1144a8e2-8bfd-484c-8a84-1ef93d7888a4",
          "name": "oauth_token",
          "request": {
            "url": "http://slack.com/api/oauth.token?client_id=%7B%7D&client_secret=%7B%7D&code=%7B%7D&redirect_uri=%7B%7D&single_channel=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Exchanges a temporary OAuth verifier code for a workspace token."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "024896ae-64bc-42d3-aba7-a6e62b348d88"
            }
          ]
        }
      ]
    }
  ]
}