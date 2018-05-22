{
  "info": {
    "name": "Slack Remove Star from Item",
    "_postman_id": "b74ed2ad-894f-4bbf-ae2e-2a745c2fffb4",
    "description": "Removes a star from an item.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Messages",
      "item": [
        {
          "id": "3141c0d1-6bd2-45cb-a310-d3d823e2107a",
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
              "id": "0b371128-73ed-4e96-b52d-6e346ed7bfe6"
            }
          ]
        },
        {
          "id": "c168867e-5182-42b1-a89e-521d9bcf3a00",
          "name": "chat_unfurl",
          "request": {
            "url": "http://slack.com/api/chat.unfurl",
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
                  "description": "Channel ID of the message"
                },
                {
                  "key": "ts",
                  "value": "{}",
                  "disabled": false,
                  "description": "Timestamp of the message to add unfurl behavior to"
                },
                {
                  "key": "unfurls",
                  "value": "{}",
                  "disabled": false,
                  "description": "URL-encoded JSON map with keys set to URLs featured in the the message, pointing to their unfurl message attachments"
                },
                {
                  "key": "user_auth_message",
                  "value": "{}",
                  "disabled": false,
                  "description": "Provide a simply-formatted string to send as an ephemeral message to the user as invitation to authenticate further and enable full unfurling behavior"
                },
                {
                  "key": "user_auth_required",
                  "value": "{}",
                  "disabled": false,
                  "description": "Set to `true` or `1` to indicate the user must install your Slack app to trigger unfurls for this domain"
                },
                {
                  "key": "user_auth_url",
                  "value": "{}",
                  "disabled": false,
                  "description": "Send users to this custom URL where they will complete authentication in your app to fully trigger unfurling"
                }
              ]
            },
            "description": "Provide custom unfurl behavior for user-posted URLs"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "c9dad23c-2123-4436-aa88-f47d3c9d27b6"
            }
          ]
        },
        {
          "id": "bbd51381-df54-4257-acda-f5f8ab2f534a",
          "name": "chat_getPermalink",
          "request": {
            "url": "http://slack.com/api/chat.getPermalink?channel=%7B%7D&message_ts=%7B%7D&token=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Retrieve a permalink URL for a specific extant message"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "23ca9186-a99c-4c97-b586-2d9483fa3875"
            }
          ]
        },
        {
          "id": "48d57d4a-946d-4207-b7a9-917c4fe0c47c",
          "name": "chat_postEphemeral",
          "request": {
            "url": "http://slack.com/api/chat.postEphemeral",
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
                  "description": "Pass true to post the message as the authed bot"
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
                  "key": "text",
                  "value": "{}",
                  "disabled": false,
                  "description": "Text of the message to send"
                },
                {
                  "key": "user",
                  "value": "{}",
                  "disabled": false,
                  "description": "`id` of the user who will receive the ephemeral message"
                }
              ]
            },
            "description": "Sends an ephemeral message to a user in a channel."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "deca9baf-3dfc-4aa7-b611-1dc813656ec9"
            }
          ]
        },
        {
          "id": "35c4e685-9aa1-47f8-b6e9-78f9e21ce760",
          "name": "chat_update",
          "request": {
            "url": "http://slack.com/api/chat.update",
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
                  "description": "Pass true to update the message as the authed user"
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
                  "description": "Channel containing the message to be updated"
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
                  "key": "text",
                  "value": "{}",
                  "disabled": false,
                  "description": "New text for the message, using the [default formatting rules](/docs/formatting)"
                },
                {
                  "key": "ts",
                  "value": "{}",
                  "disabled": false,
                  "description": "Timestamp of the message to be updated"
                }
              ]
            },
            "description": "Updates a message."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "f6543dd0-1f86-466b-9960-75c22b1404c1"
            }
          ]
        },
        {
          "id": "26d18576-7f29-4b33-8cd5-c4f31223205f",
          "name": "chat_meMessage",
          "request": {
            "url": "http://slack.com/api/chat.meMessage",
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
                  "description": "Channel to send message to"
                },
                {
                  "key": "text",
                  "value": "{}",
                  "disabled": false,
                  "description": "Text of the message to send"
                }
              ]
            },
            "description": "Share a me message into a channel."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "34d9ffb7-2fc1-4c0c-8184-66bfc700a4df"
            }
          ]
        },
        {
          "id": "66284381-66ce-4968-8a74-3f57090aa8c0",
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
                  "description": "Provide another messages `ts` value to make this message a reply"
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
                  "description": "Set your bots user name"
                }
              ]
            },
            "description": "Sends a message to a channel."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "a23f9308-594d-47c9-86a2-fa2e50a67170"
            }
          ]
        }
      ]
    },
    {
      "name": "Messaging",
      "item": [
        {
          "id": "20d2a9dd-18e6-4998-80e1-9baa7adc8684",
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
              "id": "81141eb4-c09a-4594-b85b-88155893c10e"
            }
          ]
        },
        {
          "id": "1c8d1cf2-fd44-4e7d-8421-858ed0c7953e",
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
              "id": "d12238cd-685f-4704-9980-05d0c9d22ce5"
            }
          ]
        },
        {
          "id": "8ed200e4-7245-46ef-ae68-af1afa6b2442",
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
              "id": "d604db76-b368-43f9-a18f-0175a6846e62"
            }
          ]
        },
        {
          "id": "5dd0083c-d0df-4de7-967e-3dd3b6473118",
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
              "id": "f67a9d70-1211-490f-b6be-008bf06698cd"
            }
          ]
        },
        {
          "id": "63947e2c-a197-46f9-805b-eb3d7be053fe",
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
              "id": "eab7e7cf-7694-4c7b-a353-8199eb0a72b2"
            }
          ]
        },
        {
          "id": "52d7cb6a-3677-4a75-8070-8a1f5cd838b8",
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
              "id": "e895aa33-8d1a-4e12-858f-ad5a0201fac7"
            }
          ]
        },
        {
          "id": "7d3917d4-b387-46af-b65d-d042cababb75",
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
              "id": "a1e5df14-57c9-49c0-a22a-08e4187fd2c4"
            }
          ]
        },
        {
          "id": "df22c591-b98e-4ac9-a3f8-6c20fd1a010f",
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
              "id": "9788c8f5-64be-488c-a949-11b1a1d82fa3"
            }
          ]
        },
        {
          "id": "2ac3e1c4-4413-4ed7-9f64-4fd75d4c3d29",
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
              "id": "24aacab3-5267-47e3-87e8-17c95670f008"
            }
          ]
        },
        {
          "id": "bc3d7276-011d-4490-862a-72ef00dc5862",
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
              "id": "9d4d8271-e81b-40fb-ba39-405ae4b8daf9"
            }
          ]
        },
        {
          "id": "e9df2351-21a7-44d9-a904-2b4292b78286",
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
              "id": "e144a506-73b3-4c69-ab92-535564ae9174"
            }
          ]
        },
        {
          "id": "ca93df33-ca54-4ca2-91cb-0b0e0be024fe",
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
              "id": "c0bf21c6-2176-4561-81ee-6224f9ec161c"
            }
          ]
        },
        {
          "id": "ed279d39-4a91-4c16-af03-b193b7e93329",
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
              "id": "f7f16ee8-78cf-4399-beb6-6a2610cd6929"
            }
          ]
        },
        {
          "id": "52563ed8-c39e-4a7c-9f9e-7f714eca56c7",
          "name": "channels_archive",
          "request": {
            "url": "http://slack.com/api/channels.archive",
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
                  "description": "Channel to archive"
                }
              ]
            },
            "description": "Archives a channel."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "fcfd2b70-9488-485f-8afa-414fcdb6f6a5"
            }
          ]
        },
        {
          "id": "6a648059-fd30-4ad5-aad8-def4d5851894",
          "name": "reminders_info",
          "request": {
            "url": "http://slack.com/api/reminders.info?reminder=%7B%7D&token=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Gets information about a reminder."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "b5ab90a3-a022-4b74-8298-8c879ee72ea6"
            }
          ]
        },
        {
          "id": "4296c4dd-20fe-4c83-bda0-06b64da9cab4",
          "name": "channels_info",
          "request": {
            "url": "http://slack.com/api/channels.info?channel=%7B%7D&include_locale=%7B%7D&token=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Gets information about a channel."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "6f828369-4a7c-495f-9769-e2feaa8ee9fc"
            }
          ]
        },
        {
          "id": "0c3c038e-db57-4df4-b265-9470cfc2a8c8",
          "name": "channels_kick",
          "request": {
            "url": "http://slack.com/api/channels.kick",
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
                  "description": "Channel to remove user from"
                },
                {
                  "key": "user",
                  "value": "{}",
                  "disabled": false,
                  "description": "User to remove from channel"
                }
              ]
            },
            "description": "Removes a user from a channel."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "6efed6fe-87e4-4957-8b59-6b38cf39c71e"
            }
          ]
        },
        {
          "id": "c539d080-597d-4cd6-a89e-6bf7dd0e71bd",
          "name": "groups_mark",
          "request": {
            "url": "http://slack.com/api/groups.mark",
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
                  "description": "Private channel to set reading cursor in"
                },
                {
                  "key": "ts",
                  "value": "{}",
                  "disabled": false,
                  "description": "Timestamp of the most recently seen message"
                }
              ]
            },
            "description": "Sets the read cursor in a private channel."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "1f433044-70fc-41be-b24d-54b8c6ae6c39"
            }
          ]
        },
        {
          "id": "1581e1ce-0ed6-4453-aa23-3fd0aa74bf36",
          "name": "mpim_close",
          "request": {
            "url": "http://slack.com/api/mpim.close",
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
                  "description": "MPIM to close"
                }
              ]
            },
            "description": "Closes a multiparty direct message channel."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "64655fec-d50b-4444-a3a2-09bd8b0babd8"
            }
          ]
        },
        {
          "id": "056906ce-2491-4e0d-9065-a78f225c35ca",
          "name": "conversations_join",
          "request": {
            "url": "http://slack.com/api/conversations.join",
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
                  "description": "ID of conversation to join"
                }
              ]
            },
            "description": "Joins an existing conversation."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "e73c975a-68c0-427b-bc2b-eddb3e9d143f"
            }
          ]
        },
        {
          "id": "96ff56cd-1ff0-4ef5-a335-fd06262b33ff",
          "name": "channels_history",
          "request": {
            "url": "http://slack.com/api/channels.history?channel=%7B%7D&count=%7B%7D&inclusive=%7B%7D&latest=%7B%7D&oldest=%7B%7D&token=%7B%7D&unreads=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Fetches history of messages and events from a channel."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "9d13b7f5-136d-49bc-afbf-b10a28f2f5e0"
            }
          ]
        },
        {
          "id": "56f07288-2ff0-44df-ab6a-71db0b9f43c8",
          "name": "im_mark",
          "request": {
            "url": "http://slack.com/api/im.mark",
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
                  "description": "Direct message channel to set reading cursor in"
                },
                {
                  "key": "ts",
                  "value": "{}",
                  "disabled": false,
                  "description": "Timestamp of the most recently seen message"
                }
              ]
            },
            "description": "Sets the read cursor in a direct message channel."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "f7e6afb4-ab9f-44a5-944d-e2f4c7bc6a11"
            }
          ]
        },
        {
          "id": "c4d8f425-1977-4b5b-b9e0-80ca0eeb8f35",
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
              "id": "9eacecbe-d58a-4001-a6ca-922e6e011d98"
            }
          ]
        },
        {
          "id": "e461d0aa-e56d-49de-aaff-193faba29bb6",
          "name": "files_upload",
          "request": {
            "url": "http://slack.com/api/files.upload",
            "method": "POST",
            "body": {
              "mode": "urlencoded",
              "urlencoded": [
                {
                  "key": "channels",
                  "value": "{}",
                  "disabled": false,
                  "description": "Comma-separated list of channel names or IDs where the file will be shared"
                },
                {
                  "key": "content",
                  "value": "{}",
                  "disabled": false,
                  "description": "File contents via a POST variable"
                },
                {
                  "key": "file",
                  "value": "{}",
                  "disabled": false,
                  "description": "File contents via `multipart/form-data`"
                },
                {
                  "key": "filename",
                  "value": "{}",
                  "disabled": false,
                  "description": "Filename of file"
                },
                {
                  "key": "filetype",
                  "value": "{}",
                  "disabled": false,
                  "description": "A [file type](/types/file#file_types) identifier"
                },
                {
                  "key": "initial_comment",
                  "value": "{}",
                  "disabled": false,
                  "description": "Initial comment to add to file"
                },
                {
                  "key": "title",
                  "value": "{}",
                  "disabled": false,
                  "description": "Title of file"
                },
                {
                  "key": "token",
                  "value": "{}",
                  "disabled": false,
                  "description": "Authentication token"
                }
              ]
            },
            "description": "Uploads or creates a file."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "c08a5a55-04d0-4eab-b67d-1039efb0a793"
            }
          ]
        },
        {
          "id": "89fd76ba-4341-42c6-9c5b-527c1de7d264",
          "name": "usergroups_users_list",
          "request": {
            "url": "http://slack.com/api/usergroups.users.list?include_disabled=%7B%7D&token=%7B%7D&usergroup=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "List all users in a User Group"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "0ba93378-7639-46b2-81d3-e864ea56ab45"
            }
          ]
        },
        {
          "id": "0fcee10f-caa1-4533-949e-bd333defa8e6",
          "name": "users_info",
          "request": {
            "url": "http://slack.com/api/users.info?include_locale=%7B%7D&token=%7B%7D&user=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Gets information about a user."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "cdd251a8-517f-4cf7-afa2-a9a087fd511e"
            }
          ]
        },
        {
          "id": "ba15f6ba-05f6-45c9-a85a-5b440668e600",
          "name": "users_lookupByEmail",
          "request": {
            "url": "http://slack.com/api/users.lookupByEmail?email=%7B%7D&token=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Find a user with an email address."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "225a2a6a-4b4d-4faa-bc97-12e3c627d587"
            }
          ]
        },
        {
          "id": "3b198a47-0fc0-49cf-a222-90877f764d2c",
          "name": "reactions_list",
          "request": {
            "url": "http://slack.com/api/reactions.list?count=%7B%7D&full=%7B%7D&page=%7B%7D&token=%7B%7D&user=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Lists reactions made by a user."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "90ad0811-8c9d-418d-bf51-842a2487f55f"
            }
          ]
        },
        {
          "id": "77b931a4-061e-400e-b20c-d9d949248e78",
          "name": "conversations_create",
          "request": {
            "url": "http://slack.com/api/conversations.create",
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
                  "key": "is_private",
                  "value": "{}",
                  "disabled": false,
                  "description": "Create a private channel instead of a public one"
                },
                {
                  "key": "name",
                  "value": "{}",
                  "disabled": false,
                  "description": "Name of the public or private channel to create"
                }
              ]
            },
            "description": "Initiates a public or private channel-based conversation"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "f6132b48-9ad9-4cca-bece-e924a3da795f"
            }
          ]
        },
        {
          "id": "c3b53d02-3d28-4f78-a57d-f645df4da099",
          "name": "team_billableInfo",
          "request": {
            "url": "http://slack.com/api/team.billableInfo?token=%7B%7D&user=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Gets billable users information for the current team."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "7c32b233-d0b5-454e-a123-d44a4eb1eac7"
            }
          ]
        },
        {
          "id": "4e838f15-66b3-49c6-945b-2cffcd08a24c",
          "name": "dnd_endDnd",
          "request": {
            "url": "http://slack.com/api/dnd.endDnd",
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
              "mode": "raw"
            },
            "description": "Ends the current user's Do Not Disturb session immediately."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "ee3abfee-ce67-478e-9f69-de627269a5eb"
            }
          ]
        },
        {
          "id": "14249d69-0317-45f3-8c7f-c259021511fd",
          "name": "search_all",
          "request": {
            "url": "http://slack.com/api/search.all?count=%7B%7D&highlight=%7B%7D&page=%7B%7D&query=%7B%7D&sort=%7B%7D&sort_dir=%7B%7D&token=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Searches for messages and files matching a query."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "c1159c79-138c-43f9-a7ef-2e34392c37d6"
            }
          ]
        },
        {
          "id": "a1ccae91-16b0-4459-978d-e5a9c5ae297d",
          "name": "files_comments_delete",
          "request": {
            "url": "http://slack.com/api/files.comments.delete",
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
                  "description": "File to delete a comment from"
                },
                {
                  "key": "id",
                  "value": "{}",
                  "disabled": false,
                  "description": "The comment to delete"
                }
              ]
            },
            "description": "Deletes an existing comment on a file."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "70108bb2-3fd2-4678-b97b-837c68e82214"
            }
          ]
        },
        {
          "id": "2d0d54fd-35f7-4e98-9fc7-933949ae7fe9",
          "name": "auth_revoke",
          "request": {
            "url": "http://slack.com/api/auth.revoke?test=%7B%7D&token=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Revokes a token."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "58a7f946-5ba9-4d59-b9a2-df4d2b351694"
            }
          ]
        },
        {
          "id": "a34dbdc6-1fd3-4478-982d-067e638bd9bb",
          "name": "reactions_add",
          "request": {
            "url": "http://slack.com/api/reactions.add",
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
                  "description": "Channel where the message to add reaction to was posted"
                },
                {
                  "key": "file",
                  "value": "{}",
                  "disabled": false,
                  "description": "File to add reaction to"
                },
                {
                  "key": "file_comment",
                  "value": "{}",
                  "disabled": false,
                  "description": "File comment to add reaction to"
                },
                {
                  "key": "name",
                  "value": "{}",
                  "disabled": false,
                  "description": "Reaction (emoji) name"
                },
                {
                  "key": "timestamp",
                  "value": "{}",
                  "disabled": false,
                  "description": "Timestamp of the message to add reaction to"
                }
              ]
            },
            "description": "Adds a reaction to an item."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "cd8bb6a4-3933-44ef-b77d-0a0c8ad83d7f"
            }
          ]
        },
        {
          "id": "a4710b5c-3ada-43ad-abd0-27349ed22390",
          "name": "stars_add",
          "request": {
            "url": "http://slack.com/api/stars.add",
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
                  "description": "Channel to add star to, or channel where the message to add star to was posted (used with `timestamp`)"
                },
                {
                  "key": "file",
                  "value": "{}",
                  "disabled": false,
                  "description": "File to add star to"
                },
                {
                  "key": "file_comment",
                  "value": "{}",
                  "disabled": false,
                  "description": "File comment to add star to"
                },
                {
                  "key": "timestamp",
                  "value": "{}",
                  "disabled": false,
                  "description": "Timestamp of the message to add star to"
                }
              ]
            },
            "description": "Adds a star to an item."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "f22ce1e0-3f5d-4d2e-b6e0-a2d005acf2ca"
            }
          ]
        },
        {
          "id": "5519a4d2-42f4-4f90-9352-13b26b038054",
          "name": "reminders_complete",
          "request": {
            "url": "http://slack.com/api/reminders.complete",
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
                  "key": "reminder",
                  "value": "{}",
                  "disabled": false,
                  "description": "The ID of the reminder to be marked as complete"
                }
              ]
            },
            "description": "Marks a reminder as complete."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "60e011e6-bf6e-4d66-a532-90f10eb30c7d"
            }
          ]
        },
        {
          "id": "cb092b24-21a2-4755-8c45-1537fc810563",
          "name": "conversations_unarchive",
          "request": {
            "url": "http://slack.com/api/conversations.unarchive",
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
                  "description": "ID of conversation to unarchive"
                }
              ]
            },
            "description": "Reverses conversation archival."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "e8500f24-0da5-4674-978c-2fb67dfbf86f"
            }
          ]
        },
        {
          "id": "206a5603-58e7-4147-be44-ebb9e69cb308",
          "name": "groups_info",
          "request": {
            "url": "http://slack.com/api/groups.info?channel=%7B%7D&include_locale=%7B%7D&token=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Gets information about a private channel."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "71aced53-d8d2-4dc0-bf7f-178a3caf9ae5"
            }
          ]
        },
        {
          "id": "fb3ab9d0-c737-46b2-95ef-f9da605a3117",
          "name": "files_revokePublicURL",
          "request": {
            "url": "http://slack.com/api/files.revokePublicURL",
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
                  "description": "File to revoke"
                }
              ]
            },
            "description": "Revokes public/external sharing access for a file"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "266c4b1b-9ba4-4a1a-a3b3-0328dc502633"
            }
          ]
        },
        {
          "id": "a6b1b685-f891-4042-a2d3-f670c6a6dc19",
          "name": "conversations_list",
          "request": {
            "url": "http://slack.com/api/conversations.list?cursor=%7B%7D&exclude_archived=%7B%7D&limit=%7B%7D&token=%7B%7D&types=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Lists all channels in a Slack team."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "a36eef03-235b-4025-832f-d04c3b8bb26d"
            }
          ]
        },
        {
          "id": "d741d188-daae-465b-a496-24ef314148a0",
          "name": "stars_list",
          "request": {
            "url": "http://slack.com/api/stars.list?count=%7B%7D&page=%7B%7D&token=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Lists stars for a user."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "327c9268-9c60-4471-8c70-2e03e5f16ffa"
            }
          ]
        },
        {
          "id": "3776e5ba-b84d-4070-9006-37fc829255ae",
          "name": "reactions_get",
          "request": {
            "url": "http://slack.com/api/reactions.get?channel=%7B%7D&file=%7B%7D&file_comment=%7B%7D&full=%7B%7D&timestamp=%7B%7D&token=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Gets reactions for an item."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "f870e267-f372-4b24-9dbc-abc1bce989d7"
            }
          ]
        },
        {
          "id": "7eab084a-e4df-436b-b3a5-75f7bf9d5311",
          "name": "im_history",
          "request": {
            "url": "http://slack.com/api/im.history?channel=%7B%7D&count=%7B%7D&inclusive=%7B%7D&latest=%7B%7D&oldest=%7B%7D&token=%7B%7D&unreads=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Fetches history of messages and events from direct message channel."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "bc6959ae-8111-408c-a93f-0bde60ba233d"
            }
          ]
        },
        {
          "id": "3d1efb7c-a4c9-480a-be6f-f237576f0852",
          "name": "pins_add",
          "request": {
            "url": "http://slack.com/api/pins.add",
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
                  "description": "Channel to pin the item in"
                },
                {
                  "key": "file",
                  "value": "{}",
                  "disabled": false,
                  "description": "File to pin"
                },
                {
                  "key": "file_comment",
                  "value": "{}",
                  "disabled": false,
                  "description": "File comment to pin"
                },
                {
                  "key": "timestamp",
                  "value": "{}",
                  "disabled": false,
                  "description": "Timestamp of the message to pin"
                }
              ]
            },
            "description": "Pins an item to a channel."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "95095d60-a638-4691-9689-aa377666359b"
            }
          ]
        },
        {
          "id": "b86bf1c0-6b70-4b14-8cc1-de56b6185823",
          "name": "channels_leave",
          "request": {
            "url": "http://slack.com/api/channels.leave",
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
                  "description": "Channel to leave"
                }
              ]
            },
            "description": "Leaves a channel."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "a644f9b9-ad32-4624-974f-9f081212f1d1"
            }
          ]
        },
        {
          "id": "7e941fab-2073-472c-abd8-1ba8a996ce92",
          "name": "channels_rename",
          "request": {
            "url": "http://slack.com/api/channels.rename",
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
                  "description": "Channel to rename"
                },
                {
                  "key": "name",
                  "value": "{}",
                  "disabled": false,
                  "description": "New name for channel"
                },
                {
                  "key": "validate",
                  "value": "{}",
                  "disabled": false,
                  "description": "Whether to return errors on invalid channel name instead of modifying it to meet the specified criteria"
                }
              ]
            },
            "description": "Renames a channel."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "be2fb414-f264-49ed-a83e-d4d6d897944a"
            }
          ]
        },
        {
          "id": "ef9734f9-d403-4cd9-a66e-a5a942696b36",
          "name": "files_list",
          "request": {
            "url": "http://slack.com/api/files.list?channel=%7B%7D&count=%7B%7D&page=%7B%7D&token=%7B%7D&ts_from=%7B%7D&ts_to=%7B%7D&types=%7B%7D&user=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Lists & filters team files."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "14af85fa-a7b9-4d6c-921a-0882071cd6d7"
            }
          ]
        },
        {
          "id": "66e697e7-ce74-48ed-b3b6-0c890ee77b3e",
          "name": "mpim_mark",
          "request": {
            "url": "http://slack.com/api/mpim.mark",
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
                  "description": "multiparty direct message channel to set reading cursor in"
                },
                {
                  "key": "ts",
                  "value": "{}",
                  "disabled": false,
                  "description": "Timestamp of the most recently seen message"
                }
              ]
            },
            "description": "Sets the read cursor in a multiparty direct message channel."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "8d079c8c-52da-423a-bf31-def71c62baf9"
            }
          ]
        },
        {
          "id": "15d0f4ed-c7ff-4f8c-b9be-f6139cd0a08d",
          "name": "usergroups_users_update",
          "request": {
            "url": "http://slack.com/api/usergroups.users.update",
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
                  "key": "include_count",
                  "value": "{}",
                  "disabled": false,
                  "description": "Include the number of users in the User Group"
                },
                {
                  "key": "usergroup",
                  "value": "{}",
                  "disabled": false,
                  "description": "The encoded ID of the User Group to update"
                },
                {
                  "key": "users",
                  "value": "{}",
                  "disabled": false,
                  "description": "A comma separated string of encoded user IDs that represent the entire list of users for the User Group"
                }
              ]
            },
            "description": "Update the list of users for a User Group"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "e9846633-731e-44e8-9347-97d0850fb577"
            }
          ]
        },
        {
          "id": "6b886982-efdd-4ed0-b444-acd3f09dddbe",
          "name": "conversations_setTopic",
          "request": {
            "url": "http://slack.com/api/conversations.setTopic",
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
                  "description": "Conversation to set the topic of"
                },
                {
                  "key": "topic",
                  "value": "{}",
                  "disabled": false,
                  "description": "The new topic string"
                }
              ]
            },
            "description": "Sets the topic for a conversation."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "fcab2c3b-7a96-41a3-8214-66906cb9aebf"
            }
          ]
        },
        {
          "id": "355b99e0-6c42-4f96-9cf5-4830506a5040",
          "name": "conversations_members",
          "request": {
            "url": "http://slack.com/api/conversations.members?channel=%7B%7D&cursor=%7B%7D&limit=%7B%7D&token=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Retrieve members of a conversation."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "929e1a01-5bf4-48e2-908d-170d4a186390"
            }
          ]
        },
        {
          "id": "e42e55b2-b192-422b-b6d3-89b6ca7e6001",
          "name": "conversations_open",
          "request": {
            "url": "http://slack.com/api/conversations.open",
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
                  "description": "Resume a conversation by supplying an `im` or `mpim`s ID"
                },
                {
                  "key": "return_im",
                  "value": "{}",
                  "disabled": false,
                  "description": "Boolean, indicates you want the full IM channel definition in the response"
                },
                {
                  "key": "users",
                  "value": "{}",
                  "disabled": false,
                  "description": "Comma separated lists of users"
                }
              ]
            },
            "description": "Opens or resumes a direct message or multi-person direct message."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "3e94d460-aa62-4029-b41b-a2ff15546b35"
            }
          ]
        },
        {
          "id": "f47394c8-d95e-4c4a-9ca2-47bf437e4a12",
          "name": "pins_remove",
          "request": {
            "url": "http://slack.com/api/pins.remove",
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
                  "description": "Channel where the item is pinned to"
                },
                {
                  "key": "file",
                  "value": "{}",
                  "disabled": false,
                  "description": "File to un-pin"
                },
                {
                  "key": "file_comment",
                  "value": "{}",
                  "disabled": false,
                  "description": "File comment to un-pin"
                },
                {
                  "key": "timestamp",
                  "value": "{}",
                  "disabled": false,
                  "description": "Timestamp of the message to un-pin"
                }
              ]
            },
            "description": "Un-pins an item from a channel."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "2025475c-391d-4b8d-a53e-35edb0b765f0"
            }
          ]
        },
        {
          "id": "fae29fc7-0190-4546-941f-12f1765de1ad",
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
            "description": "Deletes a file."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "9536f2c6-7a3b-43a7-a511-7b08ba9080ee"
            }
          ]
        },
        {
          "id": "8576cc34-18ad-46f4-ac1e-7ee53079482a",
          "name": "pins_list",
          "request": {
            "url": "http://slack.com/api/pins.list?channel=%7B%7D&token=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Lists items pinned to a channel."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "147f0959-a04f-462c-8aee-0694693c9119"
            }
          ]
        },
        {
          "id": "ea68ef29-6790-47c6-84af-7e1f065422f6",
          "name": "api_test",
          "request": {
            "url": "http://slack.com/api/api.test?error=%7B%7D&foo=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Checks API calling code."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "9b8c4995-f965-492b-a240-9c2b13af117e"
            }
          ]
        },
        {
          "id": "5c5f1331-951b-4a56-a94f-063b862a1585",
          "name": "reminders_list",
          "request": {
            "url": "http://slack.com/api/reminders.list?token=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Lists all reminders created by or for a given user."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "2bfb0e62-1f21-40e8-9746-9b1d63ad48ad"
            }
          ]
        },
        {
          "id": "97cae4b9-1885-49b7-8f5c-f498bab79d5f",
          "name": "users_getPresence",
          "request": {
            "url": "http://slack.com/api/users.getPresence?token=%7B%7D&user=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Gets user presence information."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "b1e284af-a80f-4396-b97e-a4113a529b32"
            }
          ]
        },
        {
          "id": "0163545d-0a3a-47d4-85a6-d24185830312",
          "name": "usergroups_update",
          "request": {
            "url": "http://slack.com/api/usergroups.update",
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
                  "description": "Include the number of users in the User Group"
                },
                {
                  "key": "name",
                  "value": "{}",
                  "disabled": false,
                  "description": "A name for the User Group"
                },
                {
                  "key": "usergroup",
                  "value": "{}",
                  "disabled": false,
                  "description": "The encoded ID of the User Group to update"
                }
              ]
            },
            "description": "Update an existing User Group"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "4c2e8d83-5f96-4652-ae37-69037e77654c"
            }
          ]
        },
        {
          "id": "fbd64508-d35c-4af8-8466-bcc53510945f",
          "name": "conversations_leave",
          "request": {
            "url": "http://slack.com/api/conversations.leave",
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
                  "description": "Conversation to leave"
                }
              ]
            },
            "description": "Leaves a conversation."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "59970a9c-3685-4c47-bd87-0a13744a21b8"
            }
          ]
        },
        {
          "id": "185c6fb8-0b19-4778-b00b-0c9a7407f7f2",
          "name": "files_info",
          "request": {
            "url": "http://slack.com/api/files.info?count=%7B%7D&file=%7B%7D&page=%7B%7D&token=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Gets information about a team file."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "ddd151e1-3673-442a-bcf6-bf52dda4e999"
            }
          ]
        },
        {
          "id": "8ae73c36-08ef-4af9-a216-4f3fa2dfe436",
          "name": "groups_leave",
          "request": {
            "url": "http://slack.com/api/groups.leave",
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
                  "description": "Private channel to leave"
                }
              ]
            },
            "description": "Leaves a private channel."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "d370c933-59fe-42b6-b925-2462f4148cf5"
            }
          ]
        },
        {
          "id": "da94b89c-a1c7-4f55-926c-cd5aa14e2b70",
          "name": "apps_permissions_info",
          "request": {
            "url": "http://slack.com/api/apps.permissions.info?token=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns list of permissions this app has on a team."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "a7b72aaa-e286-4fd0-8a2d-5fc5042e4389"
            }
          ]
        },
        {
          "id": "d2a7abf8-b0fc-411f-8632-753ec748522d",
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
              "id": "3d11532d-ff01-4704-9f5a-7a5d938af186"
            }
          ]
        },
        {
          "id": "e75347d1-3298-46f5-bd82-6a1f0e1bfc88",
          "name": "groups_createChild",
          "request": {
            "url": "http://slack.com/api/groups.createChild",
            "method": "POST",
            "body": {
              "mode": "urlencoded",
              "urlencoded": [
                {
                  "key": "channel",
                  "value": "{}",
                  "disabled": false,
                  "description": "Private channel to clone and archive"
                },
                {
                  "key": "token",
                  "value": "{}",
                  "disabled": false,
                  "description": "Authentication token"
                }
              ]
            },
            "description": "Clones and archives a private channel."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "7cb7bd9a-2239-4276-9aef-fcc6c283de01"
            }
          ]
        },
        {
          "id": "e6e32c8e-7f71-4abb-acf5-d6cb959fbd0d",
          "name": "channels_mark",
          "request": {
            "url": "http://slack.com/api/channels.mark",
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
                  "description": "Channel to set reading cursor in"
                },
                {
                  "key": "ts",
                  "value": "{}",
                  "disabled": false,
                  "description": "Timestamp of the most recently seen message"
                }
              ]
            },
            "description": "Sets the read cursor in a channel."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "b36ac326-7096-404f-9282-2458f3d4d0e6"
            }
          ]
        },
        {
          "id": "fc9e5340-46e5-4e09-bb42-382d31a02102",
          "name": "users_deletePhoto",
          "request": {
            "url": "http://slack.com/api/users.deletePhoto",
            "method": "POST",
            "body": {
              "mode": "urlencoded",
              "urlencoded": [
                {
                  "key": "token",
                  "value": "{}",
                  "disabled": false,
                  "description": "Authentication token"
                }
              ]
            },
            "description": "Delete the user profile photo"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "17930ba6-cdbc-4cc6-92ea-1038d3768e03"
            }
          ]
        },
        {
          "id": "d9100e2e-c16f-4999-8d50-820b21fd67aa",
          "name": "users_setPhoto",
          "request": {
            "url": "http://slack.com/api/users.setPhoto",
            "method": "POST",
            "body": {
              "mode": "urlencoded",
              "urlencoded": [
                {
                  "key": "crop_w",
                  "value": "{}",
                  "disabled": false,
                  "description": "Width/height of crop box (always square)"
                },
                {
                  "key": "crop_x",
                  "value": "{}",
                  "disabled": false,
                  "description": "X coordinate of top-left corner of crop box"
                },
                {
                  "key": "crop_y",
                  "value": "{}",
                  "disabled": false,
                  "description": "Y coordinate of top-left corner of crop box"
                },
                {
                  "key": "image",
                  "value": "{}",
                  "disabled": false,
                  "description": "File contents via `multipart/form-data`"
                },
                {
                  "key": "token",
                  "value": "{}",
                  "disabled": false,
                  "description": "Authentication token"
                }
              ]
            },
            "description": "Set the user profile photo"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "062262b3-24f0-4bb4-a3c7-5f77367900f1"
            }
          ]
        },
        {
          "id": "fb772b56-8f9a-4e5a-b5b4-545484651fc8",
          "name": "files_sharedPublicURL",
          "request": {
            "url": "http://slack.com/api/files.sharedPublicURL",
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
                  "description": "File to share"
                }
              ]
            },
            "description": "Enables a file for public/external sharing."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "9a837ec6-4c2d-4d55-95e5-af6cb9a06482"
            }
          ]
        },
        {
          "id": "9dabeaca-ce3c-4365-a5aa-790455befa34",
          "name": "conversations_kick",
          "request": {
            "url": "http://slack.com/api/conversations.kick",
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
                  "description": "ID of conversation to remove user from"
                },
                {
                  "key": "user",
                  "value": "{}",
                  "disabled": false,
                  "description": "User ID to be removed"
                }
              ]
            },
            "description": "Removes a user from a conversation."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "a0df5eb3-7b58-45c8-ae3e-1137bec75e28"
            }
          ]
        },
        {
          "id": "81146341-6d32-4bae-a9b1-38ac590348b0",
          "name": "conversations_rename",
          "request": {
            "url": "http://slack.com/api/conversations.rename",
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
                  "description": "ID of conversation to rename"
                },
                {
                  "key": "name",
                  "value": "{}",
                  "disabled": false,
                  "description": "New name for conversation"
                }
              ]
            },
            "description": "Renames a conversation."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "975e30dd-6669-4af6-9095-2a8c29e1115d"
            }
          ]
        },
        {
          "id": "91a5fd06-7095-47ac-9317-9afaf76905d1",
          "name": "migration_exchange",
          "request": {
            "url": "http://slack.com/api/migration.exchange?token=%7B%7D&to_old=%7B%7D&users=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "For Enterprise Grid workspaces, map local user IDs to global user IDs"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "391f6959-050b-4ef1-87ee-662e50986d3d"
            }
          ]
        },
        {
          "id": "4072bd0b-a470-4da9-b0d4-233bc68b1a2c",
          "name": "usergroups_enable",
          "request": {
            "url": "http://slack.com/api/usergroups.enable",
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
                  "key": "include_count",
                  "value": "{}",
                  "disabled": false,
                  "description": "Include the number of users in the User Group"
                },
                {
                  "key": "usergroup",
                  "value": "{}",
                  "disabled": false,
                  "description": "The encoded ID of the User Group to enable"
                }
              ]
            },
            "description": "Enable a User Group"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "c54e00ac-8d73-45ab-850e-da901ca2aec8"
            }
          ]
        },
        {
          "id": "481e1514-ef1e-4c43-a897-ce1e1309141e",
          "name": "dnd_setSnooze",
          "request": {
            "url": "http://slack.com/api/dnd.setSnooze",
            "method": "POST",
            "body": {
              "mode": "urlencoded",
              "urlencoded": [
                {
                  "key": "num_minutes",
                  "value": "{}",
                  "disabled": false,
                  "description": "Number of minutes, from now, to snooze until"
                },
                {
                  "key": "token",
                  "value": "{}",
                  "disabled": false,
                  "description": "Authentication token"
                }
              ]
            },
            "description": "Turns on Do Not Disturb mode for the current user, or changes its duration."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "f3b789ea-6251-4102-8eca-3545313a7d67"
            }
          ]
        },
        {
          "id": "ab070d0e-776f-48c8-8a48-131ab137a82a",
          "name": "mpim_history",
          "request": {
            "url": "http://slack.com/api/mpim.history?channel=%7B%7D&count=%7B%7D&inclusive=%7B%7D&latest=%7B%7D&oldest=%7B%7D&token=%7B%7D&unreads=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Fetches history of messages and events from a multiparty direct message."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "30580918-f3a1-419f-941e-c92d85977e61"
            }
          ]
        },
        {
          "id": "dfc8de0a-a9b4-490f-97a9-918de9e30605",
          "name": "apps_permissions_request",
          "request": {
            "url": "http://slack.com/api/apps.permissions.request?scopes=%7B%7D&token=%7B%7D&trigger_id=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Allows an app to request additional scopes"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "fc6e04cc-8645-4270-9eda-24c83331002e"
            }
          ]
        },
        {
          "id": "7f73a726-e91a-40f6-abce-673938f42462",
          "name": "search_files",
          "request": {
            "url": "http://slack.com/api/search.files?count=%7B%7D&highlight=%7B%7D&page=%7B%7D&query=%7B%7D&sort=%7B%7D&sort_dir=%7B%7D&token=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Searches for files matching a query."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "75378ddb-831c-4092-b3ce-a731de5c25ff"
            }
          ]
        },
        {
          "id": "903f5650-f33e-4147-9ace-d15eda7b08ac",
          "name": "users_identity",
          "request": {
            "url": "http://slack.com/api/users.identity?token=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Get a user's identity."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "b5d8c61b-658a-404f-8ea9-25ba2a8f318f"
            }
          ]
        },
        {
          "id": "2e56ecc2-dc36-420d-a252-a31d912fd8f1",
          "name": "team_accessLogs",
          "request": {
            "url": "http://slack.com/api/team.accessLogs?before=%7B%7D&count=%7B%7D&page=%7B%7D&token=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Gets the access logs for the current team."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "e2cdbd5a-6f07-4fa3-916c-989b50e590f9"
            }
          ]
        },
        {
          "id": "28acb929-44c4-460d-b269-919cfb30642f",
          "name": "groups_invite",
          "request": {
            "url": "http://slack.com/api/groups.invite",
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
                  "description": "Private channel to invite user to"
                },
                {
                  "key": "user",
                  "value": "{}",
                  "disabled": false,
                  "description": "User to invite"
                }
              ]
            },
            "description": "Invites a user to a private channel."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "65b29958-6fe6-440a-8a5e-133f2fb9684f"
            }
          ]
        },
        {
          "id": "324ea456-18a5-4e63-b72b-678c6d69cf24",
          "name": "channels_unarchive",
          "request": {
            "url": "http://slack.com/api/channels.unarchive",
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
                  "description": "Channel to unarchive"
                }
              ]
            },
            "description": "Unarchives a channel."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "249f9d18-aa07-4f0d-846c-8187cdc01366"
            }
          ]
        },
        {
          "id": "1dc99886-b302-42e6-929d-297f09b88b8e",
          "name": "rtm_connect",
          "request": {
            "url": "http://slack.com/api/rtm.connect?batch_presence_aware=%7B%7D&token=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Starts a Real Time Messaging session."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "921aa35d-ac4d-469d-b8f6-e6a712d697df"
            }
          ]
        },
        {
          "id": "c5a68899-ed95-4030-b88e-a8d5480000a0",
          "name": "team_info",
          "request": {
            "url": "http://slack.com/api/team.info?token=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Gets information about the current team."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "4e5e3a92-a9e3-47c3-91aa-e4d4a420e576"
            }
          ]
        },
        {
          "id": "844eb4b1-dd94-4476-a6cf-61cd24189854",
          "name": "conversations_history",
          "request": {
            "url": "http://slack.com/api/conversations.history?channel=%7B%7D&cursor=%7B%7D&inclusive=%7B%7D&latest=%7B%7D&limit=%7B%7D&oldest=%7B%7D&token=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Fetches a conversation's history of messages and events."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "27b8a3a9-e250-4c89-a001-707077088b33"
            }
          ]
        },
        {
          "id": "a0e71eb6-e0d6-42f0-8c46-54171badb6d6",
          "name": "channels_create",
          "request": {
            "url": "http://slack.com/api/channels.create",
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
                  "description": "Name of channel to create"
                },
                {
                  "key": "validate",
                  "value": "{}",
                  "disabled": false,
                  "description": "Whether to return errors on invalid channel name instead of modifying it to meet the specified criteria"
                }
              ]
            },
            "description": "Creates a channel."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "b403f3cb-db9b-4e2a-a667-9a8d99a84c0f"
            }
          ]
        },
        {
          "id": "e021179a-9a92-48af-ab38-b082bd4e308d",
          "name": "im_replies",
          "request": {
            "url": "http://slack.com/api/im.replies?channel=%7B%7D&thread_ts=%7B%7D&token=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Retrieve a thread of messages posted to a direct message conversation"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "8046b495-84d9-4363-9b77-95c61daf4447"
            }
          ]
        },
        {
          "id": "dc6f58c9-21c3-41ce-93f9-81ef9df92e8b",
          "name": "groups_create",
          "request": {
            "url": "http://slack.com/api/groups.create",
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
                  "description": "Name of private channel to create"
                },
                {
                  "key": "validate",
                  "value": "{}",
                  "disabled": false,
                  "description": "Whether to return errors on invalid channel name instead of modifying it to meet the specified criteria"
                }
              ]
            },
            "description": "Creates a private channel."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "d7152be6-a249-483d-8018-39e0aea65e81"
            }
          ]
        },
        {
          "id": "2703f211-a687-449f-aec5-06196e6e99b3",
          "name": "reminders_add",
          "request": {
            "url": "http://slack.com/api/reminders.add",
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
                  "key": "text",
                  "value": "{}",
                  "disabled": false,
                  "description": "The content of the reminder"
                },
                {
                  "key": "time",
                  "value": "{}",
                  "disabled": false,
                  "description": "When this reminder should happen: the Unix timestamp (up to five years from now), the number of seconds until the reminder (if within 24 hours), or a natural language description (Ex"
                },
                {
                  "key": "user",
                  "value": "{}",
                  "disabled": false,
                  "description": "The user who will receive the reminder"
                }
              ]
            },
            "description": "Creates a reminder."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "57b68aa6-4830-45c5-83be-667a96db582e"
            }
          ]
        },
        {
          "id": "267af2b9-4f5c-41a6-aa5e-c64dc7b1e39e",
          "name": "conversations_setPurpose",
          "request": {
            "url": "http://slack.com/api/conversations.setPurpose",
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
                  "description": "Conversation to set the purpose of"
                },
                {
                  "key": "purpose",
                  "value": "{}",
                  "disabled": false,
                  "description": "A new, specialer purpose"
                }
              ]
            },
            "description": "Sets the purpose for a conversation."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "cbbdc4e9-0fc7-4eeb-9b69-7d55449c6d4c"
            }
          ]
        },
        {
          "id": "894bbe30-0b4f-4cc8-bb11-cc134ade5286",
          "name": "channels_join",
          "request": {
            "url": "http://slack.com/api/channels.join",
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
                  "description": "Name of channel to join"
                },
                {
                  "key": "validate",
                  "value": "{}",
                  "disabled": false,
                  "description": "Whether to return errors on invalid channel name instead of modifying it to meet the specified criteria"
                }
              ]
            },
            "description": "Joins a channel, creating it if needed."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "8083babc-2a68-4af3-b1d4-1236e267c779"
            }
          ]
        },
        {
          "id": "c71e14cd-b1a8-46cd-bc6f-1f30f8bdcf92",
          "name": "usergroups_list",
          "request": {
            "url": "http://slack.com/api/usergroups.list?include_count=%7B%7D&include_disabled=%7B%7D&include_users=%7B%7D&token=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "List all User Groups for a team"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "37c9a04e-9d8b-47b1-bd3f-4b3d86a78ae8"
            }
          ]
        },
        {
          "id": "9afeabed-ade6-44ab-b260-fc40eb0b34cf",
          "name": "users_profile_get",
          "request": {
            "url": "http://slack.com/api/users.profile.get?include_labels=%7B%7D&token=%7B%7D&user=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Retrieves a user's profile information."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "301b9ef4-5085-4635-8125-223ca21e6d05"
            }
          ]
        },
        {
          "id": "024bb5dc-f8b5-4c86-9130-5f761c4a273e",
          "name": "groups_open",
          "request": {
            "url": "http://slack.com/api/groups.open",
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
                  "description": "Private channel to open"
                }
              ]
            },
            "description": "Opens a private channel."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "7195b600-0348-43d8-8062-1af59c87277e"
            }
          ]
        },
        {
          "id": "d2526862-d7a6-41c1-b281-8b9807d3506d",
          "name": "emoji_list",
          "request": {
            "url": "http://slack.com/api/emoji.list?token=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Lists custom emoji for a team."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "76c46c5d-ef6b-4849-8d81-bbbc308cbbba"
            }
          ]
        },
        {
          "id": "54f023df-b0d7-44df-b8fe-a70253954978",
          "name": "conversations_info",
          "request": {
            "url": "http://slack.com/api/conversations.info?channel=%7B%7D&include_locale=%7B%7D&token=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Retrieve information about a conversation."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "56da3ca6-7b88-4749-9439-6d606bcc8b9c"
            }
          ]
        },
        {
          "id": "e9ead319-d6fb-489f-84f4-74505e75b925",
          "name": "dnd_endSnooze",
          "request": {
            "url": "http://slack.com/api/dnd.endSnooze",
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
              "mode": "raw"
            },
            "description": "Ends the current user's snooze mode immediately."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "264c1e19-64de-4c69-974f-393b2f9102fa"
            }
          ]
        },
        {
          "id": "0f29b6af-4a1f-45f9-b9f8-db1593e2cad5",
          "name": "groups_history",
          "request": {
            "url": "http://slack.com/api/groups.history?channel=%7B%7D&count=%7B%7D&inclusive=%7B%7D&latest=%7B%7D&oldest=%7B%7D&token=%7B%7D&unreads=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Fetches history of messages and events from a private channel."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "bbf084a6-53bb-491c-835b-f46f52fb1e81"
            }
          ]
        },
        {
          "id": "9f8065fc-1f3b-4b84-bb9c-b00190054ce5",
          "name": "search_messages",
          "request": {
            "url": "http://slack.com/api/search.messages?count=%7B%7D&highlight=%7B%7D&page=%7B%7D&query=%7B%7D&sort=%7B%7D&sort_dir=%7B%7D&token=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Searches for messages matching a query."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "0ed3709a-f4da-4741-8bb3-1b8cdfbbb4e8"
            }
          ]
        },
        {
          "id": "eab225b8-3619-4cde-8eea-d622c0f022f5",
          "name": "rtm_start",
          "request": {
            "url": "http://slack.com/api/rtm.start?batch_presence_aware=%7B%7D&include_locale=%7B%7D&mpim_aware=%7B%7D&no_latest=%7B%7D&no_unreads=%7B%7D&simple_latest=%7B%7D&token=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Starts a Real Time Messaging session."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "b3dc85a3-0720-4927-8614-e5203f4c77ba"
            }
          ]
        },
        {
          "id": "739cb77d-896f-4e6b-bb32-05e0ba7e3f6f",
          "name": "channels_setTopic",
          "request": {
            "url": "http://slack.com/api/channels.setTopic",
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
                  "description": "Channel to set the topic of"
                },
                {
                  "key": "topic",
                  "value": "{}",
                  "disabled": false,
                  "description": "The new topic"
                }
              ]
            },
            "description": "Sets the topic for a channel."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "97d68d5a-0072-47a7-a166-6fc5c4378c8d"
            }
          ]
        },
        {
          "id": "4c1566cb-412c-48e1-9c28-ea78757d75d3",
          "name": "groups_setTopic",
          "request": {
            "url": "http://slack.com/api/groups.setTopic",
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
                  "description": "Private channel to set the topic of"
                },
                {
                  "key": "topic",
                  "value": "{}",
                  "disabled": false,
                  "description": "The new topic"
                }
              ]
            },
            "description": "Sets the topic for a private channel."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "1a497b43-16b2-447a-aaee-af53cc78c6e1"
            }
          ]
        },
        {
          "id": "8ada1cfe-deb5-400a-a245-7076aa8c5443",
          "name": "mpim_open",
          "request": {
            "url": "http://slack.com/api/mpim.open",
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
                  "key": "users",
                  "value": "{}",
                  "disabled": false,
                  "description": "Comma separated lists of users"
                }
              ]
            },
            "description": "This method opens a multiparty direct message."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "9dfb1095-a247-4a0a-b693-75f83bef3447"
            }
          ]
        },
        {
          "id": "280c0ee9-ce09-4bb2-a454-c7c155009a07",
          "name": "reactions_remove",
          "request": {
            "url": "http://slack.com/api/reactions.remove",
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
                  "description": "Channel where the message to remove reaction from was posted"
                },
                {
                  "key": "file",
                  "value": "{}",
                  "disabled": false,
                  "description": "File to remove reaction from"
                },
                {
                  "key": "file_comment",
                  "value": "{}",
                  "disabled": false,
                  "description": "File comment to remove reaction from"
                },
                {
                  "key": "name",
                  "value": "{}",
                  "disabled": false,
                  "description": "Reaction (emoji) name"
                },
                {
                  "key": "timestamp",
                  "value": "{}",
                  "disabled": false,
                  "description": "Timestamp of the message to remove reaction from"
                }
              ]
            },
            "description": "Removes a reaction from an item."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "0c997aa1-bfa3-4453-beef-f9558ba86186"
            }
          ]
        },
        {
          "id": "969b89c0-7f23-44ac-be94-02801425418e",
          "name": "reminders_delete",
          "request": {
            "url": "http://slack.com/api/reminders.delete",
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
                  "key": "reminder",
                  "value": "{}",
                  "disabled": false,
                  "description": "The ID of the reminder"
                }
              ]
            },
            "description": "Deletes a reminder."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "1ea56a63-545e-4269-8723-a0bea8e0431e"
            }
          ]
        },
        {
          "id": "d017d7e6-169b-4495-b490-7c079c2a0cb4",
          "name": "usergroups_disable",
          "request": {
            "url": "http://slack.com/api/usergroups.disable",
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
                  "key": "include_count",
                  "value": "{}",
                  "disabled": false,
                  "description": "Include the number of users in the User Group"
                },
                {
                  "key": "usergroup",
                  "value": "{}",
                  "disabled": false,
                  "description": "The encoded ID of the User Group to disable"
                }
              ]
            },
            "description": "Disable an existing User Group"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "fe4d6c21-21f9-40ee-b9a7-374109d8564d"
            }
          ]
        },
        {
          "id": "c458ba74-af85-43fb-906f-88778ede49ea",
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
            "description": "Add a comment to an existing file."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "f88bc5e6-d683-445a-adbc-364fe4d58fc0"
            }
          ]
        },
        {
          "id": "5e5e6a04-d213-49f3-8844-1daf98e4d41a",
          "name": "im_list",
          "request": {
            "url": "http://slack.com/api/im.list?cursor=%7B%7D&limit=%7B%7D&token=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Lists direct message channels for the calling user."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "ae4de4c2-f879-4c9b-a468-dbab3c5ee4e5"
            }
          ]
        },
        {
          "id": "bc5790b7-478a-4f13-87ce-29e350b6000a",
          "name": "channels_setPurpose",
          "request": {
            "url": "http://slack.com/api/channels.setPurpose",
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
                  "description": "Channel to set the purpose of"
                },
                {
                  "key": "purpose",
                  "value": "{}",
                  "disabled": false,
                  "description": "The new purpose"
                }
              ]
            },
            "description": "Sets the purpose for a channel."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "aa13bf19-10ea-475f-b6b0-616bb00bb13b"
            }
          ]
        },
        {
          "id": "a9ce9a43-666d-4bc8-b690-b393799d2a9c",
          "name": "mpim_replies",
          "request": {
            "url": "http://slack.com/api/mpim.replies?channel=%7B%7D&thread_ts=%7B%7D&token=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Retrieve a thread of messages posted to a direct message conversation from a multiparty direct message."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "b132c41f-c352-41a8-b860-57058c9ecf5a"
            }
          ]
        },
        {
          "id": "60b38de4-38e4-48f1-b733-945c3a61a326",
          "name": "dialog_open",
          "request": {
            "url": "http://slack.com/api/dialog.open?dialog=%7B%7D&trigger_id=%7B%7D",
            "method": "GET",
            "header": [
              {
                "key": "token",
                "value": "{}",
                "description": "Authentication token",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Open a dialog with a user"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "6c7942b9-26cd-470c-bc3a-b2e565afb23f"
            }
          ]
        },
        {
          "id": "f96ba047-1429-46d2-b27a-16a36b71f124",
          "name": "dnd_teamInfo",
          "request": {
            "url": "http://slack.com/api/dnd.teamInfo?token=%7B%7D&users=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Retrieves the Do Not Disturb status for users on a team."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "1e8b6dbd-a5a8-4d63-8c73-440838bf8508"
            }
          ]
        },
        {
          "id": "7f805147-4094-463b-a951-71043334a350",
          "name": "users_list",
          "request": {
            "url": "http://slack.com/api/users.list?cursor=%7B%7D&include_locale=%7B%7D&limit=%7B%7D&presence=%7B%7D&token=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Lists all users in a Slack team."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "9276f79a-3760-4815-99f7-4a878104ff93"
            }
          ]
        },
        {
          "id": "5d714ce5-39d6-4ff4-b0c5-06d0b313a39e",
          "name": "conversations_invite",
          "request": {
            "url": "http://slack.com/api/conversations.invite",
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
                  "description": "The ID of the public or private channel to invite user(s) to"
                },
                {
                  "key": "users",
                  "value": "{}",
                  "disabled": false,
                  "description": "A comma separated list of user IDs"
                }
              ]
            },
            "description": "Invites users to a channel."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "825c1a04-7413-4c59-869d-fa12ce17323d"
            }
          ]
        },
        {
          "id": "e4b9c87d-88ff-4158-ae04-c0a65a2e50eb",
          "name": "auth_test",
          "request": {
            "url": "http://slack.com/api/auth.test",
            "method": "GET",
            "header": [
              {
                "key": "token",
                "value": "{}",
                "description": "Authentication token",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Checks authentication & identity."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "70c0f4bc-cefc-4590-8508-d8edecc22682"
            }
          ]
        },
        {
          "id": "9f760f59-6af6-45f5-922f-0a3659accb39",
          "name": "channels_list",
          "request": {
            "url": "http://slack.com/api/channels.list?cursor=%7B%7D&exclude_archived=%7B%7D&exclude_members=%7B%7D&limit=%7B%7D&token=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Lists all channels in a Slack team."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "667689f1-540e-42de-abec-b05464cb4e14"
            }
          ]
        },
        {
          "id": "8893d214-41e5-40c4-af7c-da34ff27af91",
          "name": "groups_setPurpose",
          "request": {
            "url": "http://slack.com/api/groups.setPurpose",
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
                  "description": "Private channel to set the purpose of"
                },
                {
                  "key": "purpose",
                  "value": "{}",
                  "disabled": false,
                  "description": "The new purpose"
                }
              ]
            },
            "description": "Sets the purpose for a private channel."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "9f8b81b6-7d42-4296-8730-497cb4313fa2"
            }
          ]
        },
        {
          "id": "3d306723-43cc-4e21-b050-50b819e2070b",
          "name": "channels_invite",
          "request": {
            "url": "http://slack.com/api/channels.invite",
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
                  "description": "Channel to invite user to"
                },
                {
                  "key": "user",
                  "value": "{}",
                  "disabled": false,
                  "description": "User to invite to channel"
                }
              ]
            },
            "description": "Invites a user to a channel."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "3b92c719-d4ab-425a-b058-ef2020f7b6fa"
            }
          ]
        },
        {
          "id": "d95c7a9c-0c5f-40d2-9cb4-8e5019bb1083",
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
              "id": "1e4005fc-b1ac-41ff-9b3c-7030a68c5691"
            }
          ]
        },
        {
          "id": "e7b23a14-18cf-4ba4-9aca-ee92bbbfbcc7",
          "name": "mpim_list",
          "request": {
            "url": "http://slack.com/api/mpim.list?token=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Lists multiparty direct message channels for the calling user."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "03fe0945-4d8c-4e1a-9095-c3f4531a8cd9"
            }
          ]
        },
        {
          "id": "ea7f007f-7800-4db7-ab71-45df0a23a8a0",
          "name": "groups_unarchive",
          "request": {
            "url": "http://slack.com/api/groups.unarchive",
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
                  "description": "Private channel to unarchive"
                }
              ]
            },
            "description": "Unarchives a private channel."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "40afcf31-3d1e-472d-bdfd-925dc899cd0d"
            }
          ]
        },
        {
          "id": "1c467c26-4981-4bd1-844e-107df69e289c",
          "name": "channels_replies",
          "request": {
            "url": "http://slack.com/api/channels.replies?channel=%7B%7D&thread_ts=%7B%7D&token=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Retrieve a thread of messages posted to a channel"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "649115a9-18bc-4772-b709-06ea6db172a2"
            }
          ]
        },
        {
          "id": "78233283-8538-47ff-9d68-3a23b217c8ed",
          "name": "users_setActive",
          "request": {
            "url": "http://slack.com/api/users.setActive",
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
              "mode": "raw"
            },
            "description": "Marks a user as active."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "c8ccbd6e-6633-41f7-a75f-94ced22efb14"
            }
          ]
        },
        {
          "id": "caccde5d-3cda-4a0e-9f86-287dfe87be75",
          "name": "conversations_archive",
          "request": {
            "url": "http://slack.com/api/conversations.archive",
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
                  "description": "ID of conversation to archive"
                }
              ]
            },
            "description": "Archives a conversation."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "15784164-0981-41a3-8e10-4ed5c100badb"
            }
          ]
        },
        {
          "id": "1b1d6afb-cfef-4423-ac19-680238f3c3d6",
          "name": "team_profile_get",
          "request": {
            "url": "http://slack.com/api/team.profile.get?token=%7B%7D&visibility=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Retrieve a team's profile."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "9257f9c1-43d3-4026-b4d0-bf6516524e51"
            }
          ]
        },
        {
          "id": "c68e2c9e-4973-4208-94f8-bab671e1989e",
          "name": "groups_archive",
          "request": {
            "url": "http://slack.com/api/groups.archive",
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
                  "description": "Private channel to archive"
                }
              ]
            },
            "description": "Archives a private channel."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "a0785f81-469c-46de-a0b4-9a036bf915d4"
            }
          ]
        },
        {
          "id": "092e09e3-0062-47c7-8179-60ecb67ae26d",
          "name": "conversations_replies",
          "request": {
            "url": "http://slack.com/api/conversations.replies?channel=%7B%7D&cursor=%7B%7D&inclusive=%7B%7D&latest=%7B%7D&limit=%7B%7D&oldest=%7B%7D&token=%7B%7D&ts=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Retrieve a thread of messages posted to a conversation"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "54eb27d3-7325-4c8e-b5fa-180c5c803fa4"
            }
          ]
        },
        {
          "id": "114ab51e-b3d5-477f-a941-54b02fbaedd5",
          "name": "stars_remove",
          "request": {
            "url": "http://slack.com/api/stars.remove",
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
                  "description": "Channel to remove star from, or channel where the message to remove star from was posted (used with `timestamp`)"
                },
                {
                  "key": "file",
                  "value": "{}",
                  "disabled": false,
                  "description": "File to remove star from"
                },
                {
                  "key": "file_comment",
                  "value": "{}",
                  "disabled": false,
                  "description": "File comment to remove star from"
                },
                {
                  "key": "timestamp",
                  "value": "{}",
                  "disabled": false,
                  "description": "Timestamp of the message to remove star from"
                }
              ]
            },
            "description": "Removes a star from an item."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "507687e1-6ddb-4a09-9a24-a0162ba5a32f"
            }
          ]
        }
      ]
    }
  ]
}