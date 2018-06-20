{
  "info": {
    "name": "Slack Get Presence",
    "_postman_id": "bd5da18f-2479-4c5d-87d7-253bc61c30fd",
    "description": "Gets user presence information.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Messages",
      "item": [
        {
          "id": "647e01d6-a411-4e83-b5cc-bc1cbe2be8a9",
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
              "id": "00ee61da-180c-4a64-ab8c-c122042ef565"
            }
          ]
        },
        {
          "id": "9b218d61-5e01-45a9-a8cf-f7dbd97f3af8",
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
              "id": "b7b6e2e0-76a4-4cc1-8391-cac5944b9327"
            }
          ]
        },
        {
          "id": "096668c3-a82c-4d34-9d5b-63c1281c11c2",
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
              "id": "638fadc8-7885-4663-a0ab-3dcf3225c2ee"
            }
          ]
        }
      ]
    },
    {
      "name": "Messaging",
      "item": [
        {
          "id": "d4b7c0be-1315-48c2-9286-0ed3f65d9659",
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
              "id": "12ff0497-d2ca-48a1-bbbe-845dd023f42b"
            }
          ]
        },
        {
          "id": "b6474977-4d31-4c58-88a8-91bb357bb112",
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
              "id": "cd6f5f1a-3768-4d07-a403-7770648e9eb5"
            }
          ]
        },
        {
          "id": "a175808e-5ba2-4d3c-84e4-dfcdcf4821f4",
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
              "id": "56522447-9c1c-49f5-bff0-442706818680"
            }
          ]
        },
        {
          "id": "5549baa6-169c-4fb7-8c3a-56bff2f71dea",
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
              "id": "8bc77b94-55e7-4401-82f1-6c541dedac7b"
            }
          ]
        },
        {
          "id": "cf6f909d-1050-4469-84ca-28bce2eeba0e",
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
              "id": "160560d9-0594-44b0-8bbc-3a3bf212f7c3"
            }
          ]
        },
        {
          "id": "68db524d-b440-463b-80e1-218ae5fe3271",
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
              "id": "f6c4cf8a-ac3d-4531-a546-43b7c04b791f"
            }
          ]
        },
        {
          "id": "46bd87fb-245d-4bbf-ae84-bd0cafe83f9d",
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
              "id": "e918503f-af48-4d40-9280-925022665a7b"
            }
          ]
        },
        {
          "id": "e3703a5e-f47f-4c62-9355-c5da06e7c35c",
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
              "id": "548570e7-5d29-4a0c-9f06-f70cd3195951"
            }
          ]
        },
        {
          "id": "f2e922a3-9b08-40c8-8ada-75946eff49eb",
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
              "id": "b6853805-896a-491c-960d-57a0aae825c7"
            }
          ]
        },
        {
          "id": "48a92e62-355d-4181-b306-ec03f7c1ae03",
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
              "id": "5b7b099f-c1fa-4cb8-a1d7-b95c0f446be8"
            }
          ]
        },
        {
          "id": "10e8cd5a-064c-4bc4-bd76-a062c8537bec",
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
              "id": "a2ef551e-e160-4946-8a65-0ff718a577f7"
            }
          ]
        },
        {
          "id": "eb27c003-05cb-44c8-9a4e-3502f16b288c",
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
              "id": "ef2bdd8e-957b-4048-8c55-cae095f56f9c"
            }
          ]
        },
        {
          "id": "ff2c61c6-6176-4886-8568-455c51db7e38",
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
              "id": "6537d75f-2571-465b-87bf-c6e62b291f86"
            }
          ]
        },
        {
          "id": "55983dcb-628a-4116-af11-e5b522ea42d5",
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
              "id": "5f09c08b-b09b-496e-b9d1-4cbccb984eac"
            }
          ]
        },
        {
          "id": "b339caba-33a4-40e8-9de4-ff5b7864966a",
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
              "id": "b980d1af-3b31-4991-9593-9caadda14da4"
            }
          ]
        },
        {
          "id": "c5c22801-9734-44c0-8c9d-5f4cc12e8eb0",
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
              "id": "84e69522-eced-4c88-93c7-5e14b31cb183"
            }
          ]
        },
        {
          "id": "0a8743bf-1c4e-4705-bea9-a5d65f7574e3",
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
              "id": "032e4985-e35d-4bed-96c3-7e59362c9558"
            }
          ]
        },
        {
          "id": "60ea74d5-0f41-4da3-8a98-48b4ad71c07b",
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
              "id": "8c0b71e3-b06d-479f-8126-099e858569ec"
            }
          ]
        },
        {
          "id": "fb3d92ef-f1fe-4dca-8398-6b3aec126430",
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
              "id": "21333e9d-13c0-4723-ab0c-3e8eaac3f876"
            }
          ]
        },
        {
          "id": "b574732c-67f4-4ea0-a68e-2e5a3b804a2b",
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
              "id": "e48009fc-aa8e-4ceb-8ed5-ec8ce1cb8b1c"
            }
          ]
        },
        {
          "id": "f1b6d3ed-d00a-4de7-94fd-d2228726dea4",
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
              "id": "2b0ec36d-50c1-4588-ba03-ffef899e2354"
            }
          ]
        },
        {
          "id": "76c41458-b668-4ff8-a46a-c64c17aa0966",
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
              "id": "e2e4e3fa-6cbc-4dff-9cb5-00ba749ea1a9"
            }
          ]
        },
        {
          "id": "6d1e7f2b-b516-431b-ab1c-d37fa3cf0dbe",
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
              "id": "cf3794e7-f936-4b02-9cc3-0a402379bc22"
            }
          ]
        },
        {
          "id": "5b71ef7b-da6a-4822-b12e-03d04397e604",
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
              "id": "57e83c74-49d9-430e-a99d-e88d8b3dd4b1"
            }
          ]
        },
        {
          "id": "d3fa2a89-f740-491c-af14-5d29272747da",
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
              "id": "023b5c44-ee61-4c33-88dd-d3daad47a1ec"
            }
          ]
        },
        {
          "id": "9fb33a46-9049-4259-87a3-b2afcb9bbba6",
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
              "id": "fa97a2af-acf6-455f-b23d-a9f477c7e631"
            }
          ]
        },
        {
          "id": "1ab3807a-60fb-4d3d-bc88-1b1b0b57970c",
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
              "id": "d0729b93-3776-41a5-a5d0-af26b6eaabef"
            }
          ]
        },
        {
          "id": "1cb2c422-c800-4dce-b89a-d64cfa59cd79",
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
              "id": "05e5f194-c8d9-4094-9c28-cff2075a87c6"
            }
          ]
        },
        {
          "id": "49632463-9c8f-4514-ae85-4d405330cc51",
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
              "id": "85e71b12-92d1-4ff9-a179-a28483c23795"
            }
          ]
        },
        {
          "id": "64e23b58-4038-4431-9ecb-20d4264fd6e6",
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
              "id": "47be3fe9-a4b8-430d-b1d7-1d901117cfb5"
            }
          ]
        },
        {
          "id": "4bd5c053-4efc-46f4-90b4-fb323e486652",
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
              "id": "e0c17057-7837-4dc1-a449-297f79257f35"
            }
          ]
        },
        {
          "id": "6d6af56c-26fb-4d1d-97ef-cf7d2a556552",
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
              "id": "adf2536d-3323-4ffe-8437-36667902d893"
            }
          ]
        },
        {
          "id": "17b8e17b-4e64-4785-9e61-0258e1cd95e7",
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
              "id": "689e6e12-b24e-4196-9aa2-22489a2d53b7"
            }
          ]
        },
        {
          "id": "e74a59ce-27c1-4099-92c9-9a88c9d99a66",
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
              "id": "ee4163eb-da9f-47a2-bd37-4cb58d6909e0"
            }
          ]
        },
        {
          "id": "3a653d99-fedf-414e-b6f7-f549cc05ef4d",
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
              "id": "84d290e0-47e9-463b-ada2-046184e8f38c"
            }
          ]
        },
        {
          "id": "771e9126-1b40-4178-a340-5fecf18ebc15",
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
              "id": "0be6ad39-9c39-4001-9324-bd8cb37c6bd5"
            }
          ]
        },
        {
          "id": "37ad24f7-80b6-4c4d-991a-d76bb569166a",
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
              "id": "2260cce9-1b8e-4337-891e-d66e765921f0"
            }
          ]
        },
        {
          "id": "4a137cd1-4ea7-4690-bf92-99d382622f75",
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
              "id": "8e65b879-a72f-4d4e-b9ad-97f8f7c80e4d"
            }
          ]
        },
        {
          "id": "82e5b1be-8200-422f-9442-cbbf31317990",
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
              "id": "1cf6e7dd-0a81-4a2f-aef6-64c11e99d9e5"
            }
          ]
        },
        {
          "id": "ea55e60a-1ae5-4121-a6c5-ab7c9955a59e",
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
              "id": "98d1f96d-5659-4740-b3ce-6043a392fe4d"
            }
          ]
        },
        {
          "id": "3e5b3c73-33d1-46ae-a46a-f76f4260eb50",
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
              "id": "164390da-3932-4317-8d85-483c292ec601"
            }
          ]
        },
        {
          "id": "be6efdcd-1c67-4caa-a0d1-c7aaac8b4d81",
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
              "id": "4f618814-33c0-4889-9b86-d0783f7b0ed6"
            }
          ]
        },
        {
          "id": "2717ba81-5047-45d4-8e74-a111e63b1d44",
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
              "id": "ebbf0c22-c473-4349-aad9-da46ae87d288"
            }
          ]
        },
        {
          "id": "3924abbc-0d2b-4764-a645-e822c822e623",
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
              "id": "c16a9c18-a4aa-44b6-b87c-c4849c29cb60"
            }
          ]
        },
        {
          "id": "8be3fd20-1499-4820-856d-516b197fc74a",
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
              "id": "ae6b5013-0936-456b-855e-a09815652149"
            }
          ]
        },
        {
          "id": "703420e5-f1e3-4b39-9be4-baeba0e7c4ef",
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
              "id": "cad089fa-29e4-4b9d-abec-d0147bf895b3"
            }
          ]
        },
        {
          "id": "242ea14f-1f62-479f-9261-3568a610eb99",
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
              "id": "afeb572e-e3d7-4c61-a232-7953d98730af"
            }
          ]
        },
        {
          "id": "ac190ede-5e7e-4931-b60d-8d11fac75ee8",
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
              "id": "eb18a9cb-0e63-4ebb-9a71-538d96834446"
            }
          ]
        },
        {
          "id": "8576b646-265f-4c11-8d39-207ecdf556dd",
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
              "id": "182c606c-e2e6-4111-9124-78702d3052e5"
            }
          ]
        },
        {
          "id": "d7a35062-d327-48b7-a30a-cfc56522f084",
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
              "id": "85d33530-1b3d-4fdf-8b5c-e49b0873a629"
            }
          ]
        },
        {
          "id": "e3191632-6360-448b-a8ef-19ac33c5c06e",
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
              "id": "de8b9570-085c-4e05-ae69-3c21ff76095a"
            }
          ]
        },
        {
          "id": "e6606cf7-0fc5-4c12-ba16-0c45e1bd64d0",
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
              "id": "f852c3cb-70b8-4ca3-b34b-044a24ee3d22"
            }
          ]
        },
        {
          "id": "570e3e46-1259-4fdf-a494-82f52dda5dfc",
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
              "id": "d7a02bc4-2610-4877-a5c2-48660d5705a6"
            }
          ]
        },
        {
          "id": "a9aa8a68-e4f1-41b7-bbd8-6b74fd6fa848",
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
              "id": "2d4a928b-ea1e-46bb-abf5-e9bb046ba8d7"
            }
          ]
        },
        {
          "id": "3b093774-c8f2-4211-bc4d-8318316bf4d9",
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
              "id": "a932cea7-4f70-4b5a-86a4-62dfc1d59c02"
            }
          ]
        },
        {
          "id": "dbe257ff-ee6d-412b-8c57-64016c051093",
          "name": "pins_list",
          "request": {
            "url": "http://slack.com/api/pins.list?channel=%7B%7D&token=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
   