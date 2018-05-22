{
  "info": {
    "name": "Slack Get Do Not Disturb",
    "_postman_id": "7b4fedd3-dc11-4de2-92fd-5015e18a524a",
    "description": "Retrieves a user's current Do Not Disturb status.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Messages",
      "item": [
        {
          "id": "1289a4e1-4431-4cb1-a481-a0a3668b1d0e",
          "name": "chat_delete",
          "request": {
            "url": "http://slack.com/api/chat.delete",
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
                  "description": "Pass true to delete the message as the authed user with `chat:write:user` scope"
                },
                {
                  "key": "channel",
                  "value": "{}",
                  "disabled": false,
                  "description": "Channel containing the message to be deleted"
                },
                {
                  "key": "ts",
                  "value": "{}",
                  "disabled": false,
                  "description": "Timestamp of the message to be deleted"
                }
              ]
            },
            "description": "Deletes a message."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "5fd89cbd-2959-4596-adae-0612022bf814"
            }
          ]
        }
      ]
    },
    {
      "name": "Messaging",
      "item": [
        {
          "id": "f8a0e727-b8ab-47de-9b20-89c90433cd03",
          "name": "files_comments_edit",
          "request": {
            "url": "http://slack.com/api/files.comments.edit",
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
                  "description": "Text of the comment to edit"
                },
                {
                  "key": "file",
                  "value": "{}",
                  "disabled": false,
                  "description": "File containing the comment to edit"
                },
                {
                  "key": "id",
                  "value": "{}",
                  "disabled": false,
                  "description": "The comment to edit"
                }
              ]
            },
            "description": "Edit an existing file comment."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "33a184bc-20f9-40ad-b62d-de621c28bc14"
            }
          ]
        },
        {
          "id": "4b28d513-b0b7-48ff-b878-1e7d0a493835",
          "name": "im_close",
          "request": {
            "url": "http://slack.com/api/im.close",
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
                  "key": "channel",
                  "value": "{}",
                  "disabled": false,
                  "description": "Direct message channel to close"
                }
              ]
            },
            "description": "Close a direct message channel."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "83295401-e83e-431f-a67e-618d38e40beb"
            }
          ]
        },
        {
          "id": "0f3955ed-b90c-4d09-aaa2-80a4c4affb62",
          "name": "groups_replies",
          "request": {
            "url": "http://slack.com/api/groups.replies?channel=%7B%7D&thread_ts=%7B%7D&token=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Retrieve a thread of messages posted to a private channel"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "856d5d0d-167c-4a80-b8d3-9daafc8645c0"
            }
          ]
        },
        {
          "id": "a653671d-e43a-4b69-aa82-d0e7f94de390",
          "name": "bots_info",
          "request": {
            "url": "http://slack.com/api/bots.info?bot=%7B%7D&token=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Gets information about a bot user."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "f498d459-d23d-4cbc-95f6-27a4dbb7d59e"
            }
          ]
        },
        {
          "id": "4bb918d9-9fbe-4191-b459-88a7f8887a9d",
          "name": "groups_rename",
          "request": {
            "url": "http://slack.com/api/groups.rename",
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
                  "key": "channel",
                  "value": "{}",
                  "disabled": false,
                  "description": "Private channel to rename"
                },
                {
                  "key": "name",
                  "value": "{}",
                  "disabled": false,
                  "description": "New name for private channel"
                },
                {
                  "key": "validate",
                  "value": "{}",
                  "disabled": false,
                  "description": "Whether to return errors on invalid channel name instead of modifying it to meet the specified criteria"
                }
              ]
            },
            "description": "Renames a private channel."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "4f36792e-995b-4399-a3e6-8ff55c841cd6"
            }
          ]
        },
        {
          "id": "54332645-fae5-4675-a741-78088750df76",
          "name": "users_profile_set",
          "request": {
            "url": "http://slack.com/api/users.profile.set",
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
                  "key": "name",
                  "value": "{}",
                  "disabled": false,
                  "description": "Name of a single key to set"
                },
                {
                  "key": "profile",
                  "value": "{}",
                  "disabled": false,
                  "description": "Collection of key:value pairs presented as a URL-encoded JSON hash"
                },
                {
                  "key": "user",
                  "value": "{}",
                  "disabled": false,
                  "description": "ID of user to change"
                },
                {
                  "key": "value",
                  "value": "{}",
                  "disabled": false,
                  "description": "Value to set a single key to"
                }
              ]
            },
            "description": "Set the profile information for a user."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "13177bbb-483d-4aac-ac8b-5f489b33d40c"
            }
          ]
        },
        {
          "id": "60c8093f-77a3-4023-8873-68b7d006b1e7",
          "name": "users_setPresence",
          "request": {
            "url": "http://slack.com/api/users.setPresence",
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
                  "key": "presence",
                  "value": "{}",
                  "disabled": false,
                  "description": "Either `auto` or `away`"
                }
              ]
            },
            "description": "Manually sets user presence."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "d580eb12-3340-4a59-b6ae-26206600ed43"
            }
          ]
        },
        {
          "id": "fd27cdf9-bfd0-4b8b-b231-de3523e8bcc0",
          "name": "conversations_close",
          "request": {
            "url": "http://slack.com/api/conversations.close",
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
                  "key": "channel",
                  "value": "{}",
                  "disabled": false,
                  "description": "Conversation to close"
                }
              ]
            },
            "description": "Closes a direct message or multi-person direct message."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "e87217e7-81fc-449c-9e8e-9eb9943d68f4"
            }
          ]
        },
        {
          "id": "472fc102-e97a-4543-94f4-86625f6901cb",
          "name": "im_open",
          "request": {
            "url": "http://slack.com/api/im.open",
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
                  "key": "include_locale",
                  "value": "{}",
                  "disabled": false,
                  "description": "Set this to `true` to receive the locale for this im"
                },
                {
                  "key": "return_im",
                  "value": "{}",
                  "disabled": false,
                  "description": "Boolean, indicates you want the full IM channel definition in the response"
                },
                {
                  "key": "user",
                  "value": "{}",
                  "disabled": false,
                  "description": "User to open a direct message channel with"
                }
              ]
            },
            "description": "Opens a direct message channel."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "9dd0b491-3bae-40b4-8cf3-8991c40ecf4d"
            }
          ]
        },
        {
          "id": "ba7c6597-bc5a-4025-8071-c2877fb99ca5",
          "name": "groups_list",
          "request": {
            "url": "http://slack.com/api/groups.list?exclude_archived=%7B%7D&exclude_members=%7B%7D&token=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Lists private channels that the calling user has access to."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "9cd91f65-7e37-4918-86f0-d4248d116fea"
            }
          ]
        },
        {
          "id": "dc131a0b-7791-444d-9896-30f9c5261e70",
          "name": "team_integrationLogs",
          "request": {
            "url": "http://slack.com/api/team.integrationLogs?app_id=%7B%7D&change_type=%7B%7D&count=%7B%7D&page=%7B%7D&service_id=%7B%7D&token=%7B%7D&user=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Gets the integration logs for the current team."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "ea59074e-fcf6-4567-842c-a62b889e9123"
            }
          ]
        },
        {
          "id": "7507f11f-0e91-4421-9817-92f4d93a318c",
          "name": "groups_kick",
          "request": {
            "url": "http://slack.com/api/groups.kick",
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
                  "key": "channel",
                  "value": "{}",
                  "disabled": false,
                  "description": "Private channel to remove user from"
                },
                {
                  "key": "user",
                  "value": "{}",
                  "disabled": false,
                  "description": "User to remove from private channel"
                }
              ]
            },
            "description": "Removes a user from a private channel."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "2e64bb8d-3d99-423f-abc8-3a4cbe276dc6"
            }
          ]
        },
        {
          "id": "67fe831c-0d2f-4c8a-b048-72c25c548f83",
          "name": "dnd_info",
          "request": {
            "url": "http://slack.com/api/dnd.info?token=%7B%7D&user=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Retrieves a user's current Do Not Disturb status."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "b44713f3-5986-44c1-a7b1-6e16c17a19bf"
            }
          ]
        }
      ]
    }
  ]
}