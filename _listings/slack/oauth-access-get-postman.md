{
  "info": {
    "name": "Slack Oauth Access",
    "_postman_id": "8f0da263-0c7c-4d18-97f6-182b7038d4e5",
    "description": "Exchanges a temporary OAuth code for an API token.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Messaging",
      "item": [
        {
          "id": "65d141ca-1c9a-4546-a0cc-95f8e65b2555",
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
              "id": "576709fe-0460-4df0-9b8d-2945f5316cad"
            }
          ]
        },
        {
          "id": "f78c5b51-f506-431f-bf21-db843289b246",
          "name": "oauth_access",
          "request": {
            "url": "http://slack.com/api/oauth.access?client_id=%7B%7D&client_secret=%7B%7D&code=%7B%7D&redirect_uri=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Exchanges a temporary OAuth code for an API token."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "e14e3518-b6c9-47ab-83f5-b1418172dd6e"
            }
          ]
        }
      ]
    }
  ]
}