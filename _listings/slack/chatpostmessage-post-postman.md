{
  "info": {
    "name": "Slack Send Channel Message",
    "_postman_id": "8fa2cf51-92ee-4353-9fb0-e7fdc3c37f4b",
    "description": "Sends a message to a channel.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "messages",
      "item": [
        {
          "id": "ad5a8d5b-aaf2-4708-b719-749e99797c56",
          "name": "chat_postMessage",
          "request": {
            "url": "http://slack.com/api/chat.postMessage",
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
                  "key": "as_user",
                  "value": "{}",
                  "disabled": false,
                  "description": "Pass true to post the message as the authed user, instead of as a bot"
                },
                {
                  "key": "attachments",
                  "value": "{}",
                  "disabled": false,
                  "description": "A JSON-based array of structured attachments, presented as a URL-encoded string"
                },
                {
                  "key": "channel",
                  "value": "{}",
                  "disabled": false,
                  "description": "Channel, private group, or IM channel to send message to"
                },
                {
                  "key": "icon_emoji",
                  "value": "{}",
                  "disabled": false,
                  "description": "Emoji to use as the icon for this message"
                },
                {
                  "key": "icon_url",
                  "value": "{}",
                  "disabled": false,
                  "description": "URL to an image to use as the icon for this message"
                },
                {
                  "key": "link_names",
                  "value": "{}",
                  "disabled": false,
                  "description": "Find and link channel names and usernames"
                },
                {
                  "key": "parse",
                  "value": "{}",
                  "disabled": false,
                  "description": "Change how messages are treated"
                },
                {
                  "key": "reply_broadcast",
                  "value": "{}",
                  "disabled": false,
                  "description": "Used in conjunction with `thread_ts` and indicates whether reply should be made visible to everyone in the channel or conversation"
                },
                {
                  "key": "text",
                  "value": "{}",
                  "disabled": false,
                  "description": "Text of the message to send"
                },
                {
                  "key": "thread_ts",
                  "value": "{}",
                  "disabled": false,
                  "description": "Provide another message's `ts` value to make this message a reply"
                },
                {
                  "key": "unfurl_links",
                  "value": "{}",
                  "disabled": false,
                  "description": "Pass true to enable unfurling of primarily text-based content"
                },
                {
                  "key": "unfurl_media",
                  "value": "{}",
                  "disabled": false,
                  "description": "Pass false to disable unfurling of media content"
                },
                {
                  "key": "username",
                  "value": "{}",
                  "disabled": false,
                  "description": "Set your bot's user name"
                }
              ]
            },
            "description": "Sends a message to a channel"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "ddd328ba-6564-4dab-83ef-eb68fb56cb19"
            }
          ]
        }
      ]
    }
  ]
}