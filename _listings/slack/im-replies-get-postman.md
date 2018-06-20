{
  "info": {
    "name": "Slack Reply to Messages",
    "_postman_id": "853344d8-347a-472d-92f7-4de16c13645d",
    "description": "Retrieve a thread of messages posted to a direct message conversation",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Messages",
      "item": [
        {
          "id": "4e1fdb01-0ba6-4109-9109-1b50d694aeb8",
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
              "id": "ff4f64a9-bbcb-4335-ad60-ad96f99bea55"
            }
          ]
        },
        {
          "id": "867de184-fa5b-48e1-bc18-953c4784eefb",
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
              "id": "bc711b9e-2392-436f-9089-a26252e72082"
            }
          ]
        },
        {
          "id": "fd952ad1-fe6f-4a90-87f5-cea5fd42e897",
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
              "id": "a3635af6-793c-4800-9b92-5b8b564db4b7"
            }
          ]
        },
        {
          "id": "25cf20ed-d22c-4e9a-9fe6-594754cd9d15",
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
              "id": "ffba0e49-d0d3-4b7b-8ceb-e70131bb41a3"
            }
          ]
        },
        {
          "id": "5981c72c-ce49-4252-bf95-b1049bb13b8f",
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
              "id": "c81de815-8ffe-4636-a673-9f539a09bad6"
            }
          ]
        }
      ]
    },
    {
      "name": "Messaging",
      "item": [
        {
          "id": "b5782428-5d6d-4f3f-9cc4-417c81f5c5d6",
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
              "id": "2ce464ef-8f7d-404e-8a3b-7f35da350c8e"
            }
          ]
        },
        {
          "id": "b22bc54a-cde8-4e6a-9768-a12d204aaef5",
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
              "id": "25ef9149-2c0f-4022-b1ed-dc79a14686c2"
            }
          ]
        },
        {
          "id": "27718e56-d6ab-4809-9050-a1c070b9981a",
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
              "id": "78454b51-5841-4417-987c-6e1e0b183977"
            }
          ]
        },
        {
          "id": "9f5bedbd-2558-4acd-87a4-283229564313",
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
              "id": "e6ae9eb5-3d5a-47e4-b0ac-022163f8002a"
            }
          ]
        },
        {
          "id": "54ce43de-9774-4e78-96cf-557a6ef809e2",
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
              "id": "c04f46df-4c9a-4631-bd32-71a13c01d90b"
            }
          ]
        },
        {
          "id": "b0f0ea3f-2234-4ef7-ac61-a68c54ba17e5",
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
              "id": "b8d3fbde-7280-495b-8a45-aa4df0b8515b"
            }
          ]
        },
        {
          "id": "4c95c0da-6d55-48ca-bea1-317f75db5514",
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
              "id": "e37a5be5-7bfc-4970-bcd1-d6267e52d2b9"
            }
          ]
        },
        {
          "id": "cda85d85-3dc4-4522-85e4-43e5a6d813ca",
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
              "id": "4b4a44f4-6172-4f18-b165-f34a2c97f6a8"
            }
          ]
        },
        {
          "id": "ab3cd72a-bedc-4102-adac-d9b66d0ea2de",
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
              "id": "c02be5e7-a2d5-4772-b346-f04c0e443e58"
            }
          ]
        },
        {
          "id": "7fa69277-e777-40bb-b39a-94c6531e2a75",
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
              "id": "9652190b-6e4e-4786-ac32-e2f27dfa3807"
            }
          ]
        },
        {
          "id": "7f6e2508-c9f7-4027-b76f-bbf5fb26b0fd",
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
              "id": "e2aa7965-e6ba-4611-9736-46f5ba7d6ad0"
            }
          ]
        },
        {
          "id": "79668dcc-132f-4536-ba74-1710c2c3e67f",
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
              "id": "7fe1a705-38eb-43a8-a1a7-d551e37ff166"
            }
          ]
        },
        {
          "id": "c3d8cf92-40db-40b8-8298-3e72d8303918",
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
              "id": "282d1d35-bb09-4059-b4b2-4edfbecf4d34"
            }
          ]
        },
        {
          "id": "6a662dd7-aec0-4a0d-9fdd-3472a76af2f5",
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
              "id": "24b699dc-2bdf-4828-a60c-1e3c1aac5fa5"
            }
          ]
        },
        {
          "id": "b2b4a41a-37f3-419a-a1ef-8022e0c56f34",
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
              "id": "5d1d047b-060a-40a3-b561-e03b13e89b90"
            }
          ]
        },
        {
          "id": "b8b7b7fd-b7b3-4c9d-b48b-72a7ecd4583f",
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
              "id": "c793f260-b0c8-48cb-94e7-b9f9e68765d2"
            }
          ]
        },
        {
          "id": "c8320e2e-01ed-472d-ad6b-558ee788b691",
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
              "id": "97d8d044-f84a-4148-8394-1d92ccf2aa82"
            }
          ]
        },
        {
          "id": "c9e748fc-a380-4172-9cfc-2a5b669a9482",
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
              "id": "752305ee-b9f9-4108-8315-bef9a732e3de"
            }
          ]
        },
        {
          "id": "8670491c-45a0-4c49-b0f2-710ab1c777fc",
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
              "id": "547f5a70-a922-43ca-a4db-9cec900cfeb1"
            }
          ]
        },
        {
          "id": "4eac0ea4-eb9c-4a3e-9fa7-f005daed2f8c",
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
              "id": "34c9a12e-8fce-4bf6-8acf-7f96be263ced"
            }
          ]
        },
        {
          "id": "67b67356-6365-4608-ac36-3c433964a307",
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
              "id": "ee48ebc0-6532-4ff0-b40b-e14b12b62233"
            }
          ]
        },
        {
          "id": "4f4c9abd-7340-4aeb-af99-2e3d8d142886",
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
              "id": "787b3dad-d7f2-45ff-81eb-aba3dd00116c"
            }
          ]
        },
        {
          "id": "a7cff674-bef0-4528-a89b-6f89ac588eb4",
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
              "id": "1b273370-e61c-41e4-a275-98b49c92b391"
            }
          ]
        },
        {
          "id": "4029b8e2-7f19-4e92-a5a3-145def107c31",
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
              "id": "cde0e062-1c19-47e7-9d0e-2cfc9ab6e919"
            }
          ]
        },
        {
          "id": "6b79535e-faaf-4db2-9c41-598e5c2f6380",
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
              "id": "084d5d87-27f8-410b-a7e0-1634f105f2ad"
            }
          ]
        },
        {
          "id": "75cd50d2-aab3-4020-b948-f76e2ecb9813",
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
              "id": "a9778fbd-e68c-43e1-b692-35c07e4ddcb2"
            }
          ]
        },
        {
          "id": "74a1b7d0-585a-4b88-8f9f-8423002302c2",
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
              "id": "7c5ac701-ce73-480d-a6af-ca1507ab5e48"
            }
          ]
        },
        {
          "id": "6d208d05-7323-4ab1-a750-fdd5dd94d365",
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
              "id": "008735b3-f71f-41e0-89c1-1b403d3549fa"
            }
          ]
        },
        {
          "id": "6bb84775-4225-4a8b-ab62-2803f4056a7d",
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
              "id": "20b62d1e-41fa-408c-8429-9068e4b8932d"
            }
          ]
        },
        {
          "id": "2e9ebdb5-0114-4399-abf9-56bdd6f636cf",
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
              "id": "5b211772-161f-4307-a5c0-410737d4f5f5"
            }
          ]
        },
        {
          "id": "aff39028-a2a9-47e8-9039-80ffa07792b3",
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
              "id": "69c9dd9f-8ff2-472b-b035-d2918d3a42ef"
            }
          ]
        },
        {
          "id": "5fe912d9-bcbb-4470-bd6d-37ebcc58ce1d",
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
              "id": "fe26b384-fe18-44cd-8cb8-ea9009befe62"
            }
          ]
        },
        {
          "id": "e34b8499-f795-4776-b6f4-13d968dad06f",
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
              "id": "2c37aa4c-fbb3-4a38-afc1-ab804f94afaf"
            }
          ]
        },
        {
          "id": "3b5df821-2219-48f8-b9a6-55160d36776e",
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
              "id": "4266b824-fcc3-4f55-92b1-13fcd794d3e2"
            }
          ]
        },
        {
          "id": "7bc0ac59-d563-4de1-9e9c-11971479cff7",
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
              "id": "11577186-002b-4be4-a782-db50e74d7182"
            }
          ]
        },
        {
          "id": "0fc077b1-1706-4588-84fd-c6fa3b9bfad5",
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
              "id": "35fb78d3-8d23-4c3d-92f8-bcadd0287b34"
            }
          ]
        },
        {
          "id": "78b4429c-6d83-4134-b3e8-6b9f1689a87b",
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
              "id": "c1bf0f09-9567-47b7-8fb2-82a788409e2d"
            }
          ]
        },
        {
          "id": "3a82da74-1b27-4f11-9ac0-d2ecb7294e56",
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
              "id": "4646fbe9-e967-4073-b1af-988544eb0006"
            }
          ]
        },
        {
          "id": "47fe5d94-e7b9-408e-85e6-5275357d4a1e",
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
              "id": "5a3b5291-2374-4daf-b45f-cfd84f6bfa57"
            }
          ]
        },
        {
          "id": "839829cb-2a11-4de4-9159-e67073dcc24e",
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
              "id": "8fd49181-ef06-4899-a027-5e2169a27d09"
            }
          ]
        },
        {
          "id": "4bf0d7a1-2780-4e61-8118-3bb5031b2235",
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
              "id": "2e7440d9-07ac-4d4a-a6f6-4e4040863122"
            }
          ]
        },
        {
          "id": "f2172dc8-d293-4503-a4d4-1ef2830518d4",
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
              "id": "40589ed5-ef18-458c-b329-aee90d4115cd"
            }
          ]
        },
        {
          "id": "c2bb1f28-5149-47b1-b07b-135264ddcde8",
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
              "id": "dfa2d259-d680-4289-843c-fbb3121e37a0"
            }
          ]
        },
        {
          "id": "5cc099e1-c8d9-471c-b763-9a764f3e442f",
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
              "id": "d045f8b2-eef7-4d62-95cf-be05ffe366a0"
            }
          ]
        },
        {
          "id": "122c6852-52ef-42b8-bbd6-25d29488f246",
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
              "id": "69dae19f-89a0-4490-b520-61e1e832bba3"
            }
          ]
        },
        {
          "id": "54c7c163-f50e-44e5-99fc-9c5f73646220",
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
              "id": "772a08ea-0db8-4742-85b6-8cf473a11018"
            }
          ]
        },
        {
          "id": "26394ac3-5b88-4d8b-9029-11ddb0428afc",
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
              "id": "4228eadd-e7dc-4905-8ee1-cc379741892e"
            }
          ]
        },
        {
          "id": "f429ca31-d128-48a5-930a-855b39af4260",
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
              "id": "8d60f113-7cf8-4e6b-ae7d-42e9f828b3a9"
            }
          ]
        },
        {
          "id": "4409ba35-800e-4aab-b2a5-ee4e5e5f1421",
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
              "id": "0c1afda9-636c-49e6-9f31-825e485deed2"
            }
          ]
        },
        {
          "id": "41538d8e-92cf-489c-93e8-073b1f71c3e5",
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
              "id": "e2478c84-9dca-43c7-a0ed-fa9180885e5d"
            }
          ]
        },
        {
          "id": "64869abd-7b76-4d32-a452-6a30680507a9",
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
              "id": "e6771449-a84f-49aa-8e15-d137c1fed455"
            }
          ]
        },
        {
          "id": "0555d64b-95b7-4f1e-9faf-41eca3fdd4d0",
          "name": "conversations_members",
          "request": {
            "url": "http://slack.com/api/conversations.members?channel=%7B%7D&cursor=%7B%7D&limit=%7B%7D&token=%7B%7D",
            "method": "GET",
          