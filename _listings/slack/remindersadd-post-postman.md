{
  "info": {
    "name": "Slack Add Reminders",
    "_postman_id": "80a39a88-e86e-491d-9c0a-a18f02b20ec5",
    "description": "Creates a reminder.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Messages",
      "item": [
        {
          "id": "29541f4b-c8d2-4323-82f0-ecc4169e51f9",
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
              "id": "98a4990f-4fc4-4f88-b455-e912011b4b74"
            }
          ]
        },
        {
          "id": "89d27b33-abd6-4b2e-9b91-0d9e3f9b6a95",
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
              "id": "c1ce1c84-d468-4fc0-9582-714007daf7b7"
            }
          ]
        },
        {
          "id": "7a425e40-6955-4629-a59d-17f9fabe6c45",
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
              "id": "dfb2ec8b-6ab6-4e5a-9727-47dd405bb53f"
            }
          ]
        },
        {
          "id": "75bc225a-7039-491c-92ad-67ff206404c6",
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
              "id": "7b5c98b5-1b5f-4a43-9376-efcf2bdd1b1c"
            }
          ]
        },
        {
          "id": "99f729b5-3a8e-475a-9f54-828df2e79e24",
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
              "id": "089adb9c-ac5a-429e-87a8-642c5bb8d0a0"
            }
          ]
        }
      ]
    },
    {
      "name": "Messaging",
      "item": [
        {
          "id": "6c53928c-c87d-4a85-913d-d7fe4f9b2cca",
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
              "id": "8dac1db4-e1c6-4300-b16e-b04ca62b1622"
            }
          ]
        },
        {
          "id": "b6554c38-f4ac-4ab7-a3c0-707c99d166db",
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
              "id": "d4bc03c2-3f74-4088-9dcf-263f56bbd97e"
            }
          ]
        },
        {
          "id": "3be66e11-3d00-45a0-a41f-870003c67254",
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
              "id": "c5f04b2a-fbc8-4235-b6ba-5f4478223dcb"
            }
          ]
        },
        {
          "id": "47ffc894-5753-409b-b819-8744fe14d3d3",
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
              "id": "c3567816-3148-4130-8262-0d2d8bce7e75"
            }
          ]
        },
        {
          "id": "40acc6c7-53a3-4d56-8fc7-c5db5fef4a6e",
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
              "id": "3227a485-d7e4-46d5-aefc-1011050f2558"
            }
          ]
        },
        {
          "id": "49f29e3f-4bc5-4f83-8fac-e977ce84ff42",
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
              "id": "dd43a25a-898c-4fe9-b0ce-35c9ee3be83e"
            }
          ]
        },
        {
          "id": "de074d8a-9a78-4f00-a37f-17dd6ab2c759",
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
              "id": "28945367-2abb-4aea-a8d7-5954f2007b60"
            }
          ]
        },
        {
          "id": "f200f194-0f5d-4e22-b2e0-a543e73f2c8b",
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
              "id": "bd761ed3-14f4-49f5-a3ce-a105e876d802"
            }
          ]
        },
        {
          "id": "1e21a576-f9fd-4f80-aca0-ef221add7161",
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
              "id": "e401e955-41e1-4ac1-a336-c046937ba051"
            }
          ]
        },
        {
          "id": "3af23462-1a6a-4ef6-b5c8-2457eac17927",
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
              "id": "002caf1e-4e91-4add-b4f7-c976df8c43f6"
            }
          ]
        },
        {
          "id": "012e72c8-a3d9-4dce-a289-efc937433c48",
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
              "id": "37695223-418e-4148-b1bf-0efd4632207a"
            }
          ]
        },
        {
          "id": "1260ab40-5171-4741-978a-1a8fc323816d",
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
              "id": "79eb7927-e3d5-4c64-86a3-638ee6f6202a"
            }
          ]
        },
        {
          "id": "9a4862bc-474b-45a9-9fa4-7e44209f4974",
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
              "id": "14e57645-f223-41ac-b97f-65d4d03246ad"
            }
          ]
        },
        {
          "id": "753b806f-2dfd-4f4c-aa15-bbdf6979c165",
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
              "id": "0bd09b93-e187-470f-89c4-c8c469165b4f"
            }
          ]
        },
        {
          "id": "35fa5425-b86a-418d-b0f1-2b6946514c4f",
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
              "id": "3c7a0514-5137-4c8c-9a2c-b3c6637c69a3"
            }
          ]
        },
        {
          "id": "10d91ec4-d344-4242-bff7-9e736dd7670f",
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
              "id": "bbe4ab22-8887-4521-9105-3eae6429d144"
            }
          ]
        },
        {
          "id": "7a79c122-b358-40fe-afd4-eceb8e00861c",
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
              "id": "48a949eb-168b-49ae-8aeb-bd605991ca59"
            }
          ]
        },
        {
          "id": "b64ee6f7-3cee-43c6-8213-ba2aaa1ff2b9",
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
              "id": "bffc9791-1d88-4879-bda9-a7f6fb23b109"
            }
          ]
        },
        {
          "id": "05738b23-aa7e-4bda-acae-f7e05406d219",
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
              "id": "c4e3dc2d-cdd1-4862-abf1-6b2b092ff5a7"
            }
          ]
        },
        {
          "id": "3dcaf381-4d88-4c7d-91f9-77ba0a455b55",
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
              "id": "ce79e28c-caf3-4c35-88a1-9a0ba2a7bd14"
            }
          ]
        },
        {
          "id": "ec81c9af-e8f6-42da-9d1b-5aa6b2113b09",
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
              "id": "f232de42-f602-4ec3-85d8-e092d356c05b"
            }
          ]
        },
        {
          "id": "4f8a531d-4b5b-4b79-a0d0-b67e6993835e",
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
              "id": "277a4ec5-0a2d-4759-8916-604915482887"
            }
          ]
        },
        {
          "id": "06fbfe31-fc8a-4286-9fb7-ee5db64952af",
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
              "id": "94645bf7-9f16-4251-b0b1-9f0f3c34636b"
            }
          ]
        },
        {
          "id": "d01fc619-c5c9-4ce4-bf87-fea9ffd176c7",
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
              "id": "3c6a3c45-38f2-4693-a1e9-c7e2a8e88022"
            }
          ]
        },
        {
          "id": "be0f5a88-3201-4c9a-afb7-0c28b88c7401",
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
              "id": "1f29da47-9f83-4705-9363-4ad64fb4c392"
            }
          ]
        },
        {
          "id": "787ab69d-b364-43fa-8930-a5cdfeaf3506",
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
              "id": "ae3f2f12-d0fe-4a01-bcaa-98fdb9c1607d"
            }
          ]
        },
        {
          "id": "d30874ee-f286-4330-85be-f8ae00620cb1",
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
              "id": "a55fcd83-39d3-475e-9270-b83ace7900e3"
            }
          ]
        },
        {
          "id": "fe36cc90-523c-4fce-8e25-2fe9e95fe2d2",
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
              "id": "314fd7eb-165d-4a1f-92eb-8720fd78a6c9"
            }
          ]
        },
        {
          "id": "479ccfcd-369e-4d1e-8db5-7d536dbb144d",
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
              "id": "2976815c-fae2-48d0-9c0a-0ba7c5b55b97"
            }
          ]
        },
        {
          "id": "099abec0-382e-40f9-8aa4-9725a0f47083",
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
              "id": "3540ca42-b69f-4c81-90a0-4a0420a2da60"
            }
          ]
        },
        {
          "id": "fc234990-c706-43f7-b918-9ec80d58a692",
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
              "id": "11102d79-f27f-48d9-b803-4aa4fca0b74b"
            }
          ]
        },
        {
          "id": "0cc0c0b6-0444-47b9-a132-776c8702fafb",
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
              "id": "1c4ae834-97b4-4902-9bdb-e4b8c32ccc04"
            }
          ]
        },
        {
          "id": "e183b7b0-d2ac-4ff7-a35d-5d2f6285de40",
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
              "id": "bdf7bd9a-4e58-42ba-8e89-a939507ba788"
            }
          ]
        },
        {
          "id": "ef89e14d-9fa5-4fc6-b685-6880f97199f8",
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
              "id": "a49d0f24-a05d-4b3e-967d-0c9f345d615c"
            }
          ]
        },
        {
          "id": "6e7dbb63-e329-4daa-8798-2700ccd926a3",
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
              "id": "3a58a4f3-f4d6-4632-9672-d781be276505"
            }
          ]
        },
        {
          "id": "203c6e53-a483-45f4-ad33-9da079607f97",
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
              "id": "0bca6189-5147-4cac-bb49-237bf56d9bde"
            }
          ]
        },
        {
          "id": "7868d919-e972-4543-9d52-052a74162244",
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
              "id": "27a12f24-21a1-4285-a237-e7a715750e36"
            }
          ]
        },
        {
          "id": "7747c7e4-97e6-4228-a523-7018ce376e16",
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
              "id": "d472e247-41e5-444b-b548-25d0a2960845"
            }
          ]
        },
        {
          "id": "47a425e9-c321-454d-8dea-dbb6d098663d",
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
              "id": "7745e4a4-2d46-4afe-8b40-7b36b694edec"
            }
          ]
        },
        {
          "id": "d112b50b-7ec4-49a4-88f0-9ece31e998e3",
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
              "id": "780d43da-c681-4577-8696-0e3b041b7fc3"
            }
          ]
        },
        {
          "id": "261b2345-dda0-40a3-8961-5d14afb70151",
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
              "id": "684dad01-80bc-4f89-a72b-df6968620fab"
            }
          ]
        },
        {
          "id": "eee7ea61-bd8d-4aa6-973b-556d25c5f9a9",
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
              "id": "880e0089-1a0e-4e7d-a4ee-8d559cabc2b5"
            }
          ]
        },
        {
          "id": "f9671318-af94-40a2-8bd7-b7a130ef59f3",
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
              "id": "f8e492bb-785d-4c94-901e-ad59def895bb"
            }
          ]
        },
        {
          "id": "0ef21bc3-2e0d-4b26-b73b-4b3a8e1804df",
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
              "id": "db57bb53-b8d5-4451-8bef-71c0938e010b"
            }
          ]
        },
        {
          "id": "da247ccb-13e5-4fc7-887a-1a08c7436ae5",
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
              "id": "f71e98f4-dffe-44a9-9ffa-6c9b508046a2"
            }
          ]
        },
        {
          "id": "b8348be1-a88b-4624-88f8-31c21c350c8f",
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
              "id": "a701e68f-28d7-4978-a940-fb14a816dbbe"
            }
          ]
        },
        {
          "id": "488a3735-fc44-481a-bd33-fadbfd9a0555",
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
              "id": "d3bbfa95-d03b-444a-acf4-f2fd4fd005f0"
            }
          ]
        },
        {
          "id": "833e2129-6111-49cd-bfd8-5eee5684d6c9",
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
              "id": "8ef2020e-e7c6-4854-a8a8-f9a60cd6afd1"
            }
          ]
        },
        {
          "id": "9ebaa40b-2adb-431c-972b-b6dd368120c1",
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
              "id": "94eb05e2-3fb9-463a-91a4-766a1d3d3516"
            }
          ]
        },
        {
          "id": "f931caa1-3be5-419c-baf2-9153fee4fff6",
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
              "id": "23c7063d-7a9c-4eb0-95cf-19f8ac9bf93c"
            }
          ]
        },
        {
          "id": "5d39fbeb-190b-4a20-916d-ac67699316ad",
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
              "id": "f4840271-d268-4947-ba8c-e287ccda858f"
            }
          ]
        },
        {
          "id": "7c7978b1-e2e1-48cb-8fb2-a91960103ce5",
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
              "id": "c20c1a25-e31a-4717-a5d8-9ae9a5b2b9b6"
            }
          ]
        },
        {
          "id": "2a904345-abd1-4b28-8d01-bc69f0cd3140",
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
              "id": "5111a5be-c11f-4780-a453-86cf3e4f5a23"
            }
          ]
        },
        {
          "id": "c619ae02-b242-4cdb-a4a1-3ef905e825b8",
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
              "id": "c116ffdc-cce6-4b3e-9fbc-ea90fc98db9f"
            }
          ]
        },
        {
          "id": "d6d116d1-2940-44b6-92f5-9e96fb0ce01e",
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
              "id": "48dc49ec-18e7-490c-bfc7-c1af9b19eb0e"
            }
          ]
        },
        {
          "id": "6d823bc8-2c30-4b9a-be48-7038c7c2b157",
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
              "id": "e21ae96c-42f3-43a6-8506-c777e7a042be"
            }
          ]
        },
        {
          "id": "7206b205-fd6f-4d6a-ba64-e8b259076a44",
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
              "id": "1da6efbb-f14a-4d00-afe7-a955c9ded199"
            }
          ]
        },
        {
          "id": "7b74af8f-9115-4f8f-aab5-605d9fc816ec",
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
              "id": "d90c78b0-adc0-41db-b7cb-dd7f17df0cdf"
            }
          ]
        },
        {
          "id": "b9b082fd-f179-4864-b40d-f05b184f20fc",
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
              "id": "23cf1e47-20c9-4cfa-8912-17ffcb6936fc"
            }
          ]
        },
        {
          "id": "e2926665-de19-42ba-9bee-02a7482dd241",
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
              "id": "9b762009-b0ed-4348-9491-9d0793897f22"
            }
          ]
        },
        {
          "id": "3ec6cf02-6f23-4a63-8798-cdf4ed0b4106",
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
              "id": "a10f9004-8392-440e-a1a1-617d8fbc5ac7"
            }
          ]
        },
        {
          "id": "383178c6-4728-4309-88fa-ea46c80703f7",
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
              "id": "cc3b01bb-328d-45d6-a9d1-b5f8247951c4"
            }
          ]
        },
        {
          "id": "45b6da17-aae9-4463-8ed1-f00196466133",
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
              "id": "9f6ddcc4-92f6-489a-9382-1f225ebb5e54"
            }
          ]
        },
        {
          "id": "98493cdf-37a5-468d-b3cb-9f794c193630",
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
              "id": "5fbfe299-0631-4ca8-ba5f-eca8cae05af6"
            }
          ]
        },
        {
          "id": "65b26799-15e4-4460-a52d-3f0a403fe39e",
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
              "id": "711f9e30-2969-4558-b811-307f1e2081c1"
            }
          ]
        },
        {
          "id": "ee4b2ed5-a7da-4cfc-8966-69b0ecb51272",
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
              "id": "c872f6dd-94bf-4315-94a2-d185c4b7566f"
            }
          ]
        },
        {
          "id": "485d1a24-3f23-4a0e-9f77-e0eacf79197b",
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
              "id": "ac004c0f-81ea-4f2a-97e5-904d83bbb791"
            }
          ]
        },
        {
          "id": "839dd1c1-f603-495c-9d0a-20417ba53d09",
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
              "id": "aafe348d-b2df-4092-81e7-8ec986ae84a9"
            }
          ]
        },
        {
          "id": "a6ceb9a6-0d83-45fc-832a-e61777b52e6d",
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
              "id": "6edab56d-9041-432b-8c75-9506161c83c7"
            }
          ]
        },
        {
          "id": "458ac281-a26f-4e27-a193-c36c1de9b4c2",
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
              "id": "19668c22-1fe3-4845-a164-e442efdd891e"
            }
          ]
        },
        {
          "id": "10452392-7403-4041-a9c5-1c2b7239da96",
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
              "id": "1bbe8f65-b72c-46f7-b479-968f34a58162"
            }
          ]
        },
        {
          "id": "c6ef9977-cd03-4817-86fe-2b89874bc2ce",
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
              "id": "68453fd5-f1e0-498c-954a-639c6bbf40e1"
            }
          ]
        },
        {
          "id": "10eb8a30-108e-43c5-9e80-8a4d628a8d51",
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
              "id": "ec8ed59c-cc1a-4ab6-8279-850c297129ad"
            }
          ]
        },
        {
          "id": "4b69e8f6-35ac-4873-beba-dce32ac02060",
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
              "id": "1bd32ef0-e6ae-4520-a60d-2ba3099dcf2b"
            }
          ]
        },
        {
          "id": "54092bb7-fd40-415c-b893-25b3aec800a2",
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
              "id": "3afcaa26-e3c0-483e-bae0-5294c1876ccb"
            }
          ]
        },
        {
          "id": "47990a80-05db-4d4c-b529-9642dc6a25fc",
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
              "id": "01c11736-170f-448e-8102-cfd1c8e4bfe9"
            }
          ]
        },
        {
          "id": "e6ecff30-87d1-483b-82a6-89634e074907",
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
              "id": "3d913c01-be90-474d-b053-b591090a764d"
            }
          ]
        },
        {
          "id": "a484f6be-2540-41f6-8a2f-6e191559e597",
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
              "id": "8cd0e2d0-ca52-4bd7-b6c0-03fe2cde87ee"
            }
          ]
        },
        {
          "id": "e1b07fbe-25ed-4d63-a25c-38fd4481c5aa",
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
              "id": "9d84c6f2-6b1b-4962-85b7-43773ce370e1"
            }
          ]
        },
        {
          "id": "eee2e626-f4ac-4fc7-84d4-130a494c1baf",
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
              "id": "e868d255-ee9c-48e5-ad50-40c20f447f45"
            }
          ]
        },
        {
          "id": "7e384244-1386-43b6-86e6-754c84bd40b2",
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
              "id": "61b34ece-8bf4-46de-b0d8-f18cc2a021df"
            }
          ]
        },
        {
          "id": "076b7113-1292-4a0c-9274-c53dcde92d36",
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
              "id": "65196466-d2d3-468b-bcd2-8ab60f6b701a"
            }
          ]
        },
        {
          "id": "8ebe055a-b08e-43f7-a28d-6408dfe6c382",
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
              "id": "9ddbb121-60bf-4578-b365-06f3cddd24cb"
            }
          ]
        },
        {
          "id": "583022ed-d556-4c41-a0f9-0aac43a874e6",
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
              "id": "07b9ebaf-fb64-499e-b686-71c6e9305fe2"
            }
          ]
        },
        {
          "id": "9536dd13-9776-45e9-851c-41982cb47ea8",
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
              "id": "dfb7b823-75aa-4391-9a00-594d92a0fae8"
            }
          ]
        },
        {
          "id": "65de7f4d-8b68-49a2-a105-a8d4462c6c71",
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
              "id": "f9e82705-48d7-4c5a-a646-3e4560ac58ae"
            }
          ]
        },
        {
          "id": "fdfb9fe4-b428-4636-b65b-92e543c362af",
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
              "id": "80a7df5d-a70c-4d27-a7c6-5b4902c85d8e"
            }
          ]
        },
        {
          "id": "5fcbd8f3-a2e0-4ea5-9452-c60ec2b053f2",
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
              "id": "961ae636-b136-4786-b38a-a53508fbb71c"
            }
          ]
        },
        {
          "id": "984afe74-3ecc-49d0-810d-5d57614bbebc",
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
              "id": "bdca5262-bbd2-444b-af95-4c7379b1491f"
            }
          ]
        }
      ]
    }
  ]
}