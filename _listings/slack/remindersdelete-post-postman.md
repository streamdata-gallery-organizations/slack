{
  "info": {
    "name": "Slack Delete Reminders",
    "_postman_id": "c022cc3f-d061-4305-82df-673e3157eef6",
    "description": "Deletes a reminder.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Messages",
      "item": [
        {
          "id": "d8e82569-8e0a-4f82-af41-cd8de14154d4",
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
              "id": "e9d08e32-e52d-4569-a284-36e45d2672d5"
            }
          ]
        },
        {
          "id": "a5f54aaa-efdc-4917-9be3-026fb146306e",
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
              "id": "be72fd38-dc57-49fc-8353-9a50afb65870"
            }
          ]
        },
        {
          "id": "40966f12-12ba-478a-bda9-ea5cfd05a56b",
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
              "id": "08e6369f-dcc5-415b-9537-f231f8eff0f6"
            }
          ]
        },
        {
          "id": "82bb0dac-c059-4e74-b22e-48f8ca953b11",
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
              "id": "964b05a8-1870-4f35-9299-26312df6f9d5"
            }
          ]
        },
        {
          "id": "ad7baf3e-9c95-4422-82a5-7f3f71d6ccce",
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
              "id": "e952b6a5-24fd-47f7-ad96-2d366200a57f"
            }
          ]
        },
        {
          "id": "dfabbf5d-2d84-4599-912c-1dab91399864",
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
              "id": "641bf8e3-2471-4085-b6dd-47db18e7a39c"
            }
          ]
        }
      ]
    },
    {
      "name": "Messaging",
      "item": [
        {
          "id": "fbdd4e9a-c4a4-4558-930f-72fb9d9c377c",
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
              "id": "190772c1-25ab-4e9f-a741-2ab5d2de77d7"
            }
          ]
        },
        {
          "id": "e3eb4d55-794b-4c71-aee2-15a6239b2983",
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
              "id": "05885e0a-b13b-4545-9a4b-7efd577b8347"
            }
          ]
        },
        {
          "id": "927d6356-252d-491b-94eb-42cef85e3d06",
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
              "id": "7da052df-8e5e-40f7-b763-82faf83102fa"
            }
          ]
        },
        {
          "id": "74d25ead-3cc6-4e2d-b7b8-b0feb0d2cc9c",
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
              "id": "916bc805-17be-4352-b18e-31880642cb4d"
            }
          ]
        },
        {
          "id": "b01ba579-1931-4fdb-b56c-e5ba844800db",
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
              "id": "cae27a74-5836-4a24-95cc-75e8bf2d7b08"
            }
          ]
        },
        {
          "id": "42c4a090-7cab-4100-b026-b671d1b72802",
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
              "id": "a388cecb-031d-4858-ae39-f408546ba675"
            }
          ]
        },
        {
          "id": "0cdbd641-e2fa-406f-ad8e-51af4166ce3e",
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
              "id": "90fd2e06-db7d-4629-87de-4804696845cd"
            }
          ]
        },
        {
          "id": "a74f03a9-d38f-4eb6-b950-18a9965b9f84",
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
              "id": "65d67c1c-51e1-45ec-b1a1-8d02197addde"
            }
          ]
        },
        {
          "id": "e4c58e32-484f-4fd6-b595-f4c345af1008",
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
              "id": "ee48e817-c546-4334-ba6f-146450546d87"
            }
          ]
        },
        {
          "id": "f828b58e-de1c-4aa5-9c38-c8bd1651209f",
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
              "id": "e3bd4ed0-f0e8-4ef3-98bb-a966d9c20374"
            }
          ]
        },
        {
          "id": "d2093660-3238-463d-816d-f517255d3d80",
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
              "id": "dcae5c8e-d580-43c7-8689-84fdf4b377a1"
            }
          ]
        },
        {
          "id": "ec70ff4b-9b51-4d7f-9863-7eba61428f1b",
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
              "id": "b996ef2e-9fd8-4d5c-b6c6-c713dc6148ee"
            }
          ]
        },
        {
          "id": "d43ba142-ec21-4efc-905f-010e4c1cbea8",
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
              "id": "7ca0ca4c-7b02-4476-b73f-faff2d217635"
            }
          ]
        },
        {
          "id": "46360cad-2620-475d-8777-027ccd7b9772",
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
              "id": "b69ef20a-2fed-43c3-a88c-fd41e8f5acfc"
            }
          ]
        },
        {
          "id": "643d4f10-2fbb-4881-ab07-ac920630ce3e",
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
              "id": "fb58a4f9-a2c7-46ab-90b5-e3573ac414c7"
            }
          ]
        },
        {
          "id": "06ce514b-354d-418f-83a8-1e59910a7b08",
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
              "id": "ea708837-07b8-4f7c-980b-02b7ed443980"
            }
          ]
        },
        {
          "id": "b7e5e63e-2c29-44c7-8e02-9e7af37470d9",
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
              "id": "3132808b-c4fb-415a-aae5-5d0c05cc608b"
            }
          ]
        },
        {
          "id": "f107f45d-ba8b-4e02-96d5-f528d8809ea0",
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
              "id": "7bd2d001-2d61-46c9-be27-605f30186d75"
            }
          ]
        },
        {
          "id": "376d2afd-fd6f-4253-b0a1-14d6ec9ce830",
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
              "id": "f778940f-8870-46e6-b443-de30a1fc8755"
            }
          ]
        },
        {
          "id": "f2eb896d-3edc-4bf0-a1c8-f4702ddcdb74",
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
              "id": "26d26c3c-df34-4a6c-9075-fc18a151fadc"
            }
          ]
        },
        {
          "id": "f9b48061-e276-4b8a-8079-dd0186e8ab47",
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
              "id": "11d68b2b-4c81-423b-aeb0-889d82d361a4"
            }
          ]
        },
        {
          "id": "a6cce48c-164f-4c36-8505-eadbbcce0a6e",
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
              "id": "12b6d2fe-7abe-453e-971a-7ed88a289cb7"
            }
          ]
        },
        {
          "id": "02165b55-37fc-4f7a-a76c-2e98c5800e64",
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
              "id": "e0fc79e7-933a-467c-9730-fbfb7a6c816f"
            }
          ]
        },
        {
          "id": "b5f4229e-0e99-484b-b8c0-9cd8a5e50d6e",
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
              "id": "45e81496-1b97-426e-b46e-ba94dd326aa4"
            }
          ]
        },
        {
          "id": "b876d9ce-4a99-4dba-a490-9dc3c990e64f",
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
              "id": "a1ab0307-f528-4e3f-95f7-2ed41bced44e"
            }
          ]
        },
        {
          "id": "f2623d4e-f8da-4464-998b-1c4f614d00ff",
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
              "id": "42ae9663-258e-4eb7-9798-fd8b4930ca78"
            }
          ]
        },
        {
          "id": "7569e817-5b1b-4978-bcd8-2120cf28d375",
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
              "id": "b6966eb3-809a-49e8-83fd-10598c139e9d"
            }
          ]
        },
        {
          "id": "a479960b-e6e6-42d9-9ef4-998451c1233f",
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
              "id": "fd937522-bdcc-4b52-bf9d-777689446e9f"
            }
          ]
        },
        {
          "id": "91429e68-0f25-47e3-9f34-7169c7861ac4",
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
              "id": "42fface5-31bf-4e37-bef6-7357320cb134"
            }
          ]
        },
        {
          "id": "adba3754-c6f1-4ab9-abbd-a029c1812a0e",
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
              "id": "0ffdbe11-6667-4c4e-9531-274567311e4d"
            }
          ]
        },
        {
          "id": "da6719ad-b6c7-43ae-ac9e-7686af8b77a7",
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
              "id": "156dc549-b215-4f87-8022-c77958437bfc"
            }
          ]
        },
        {
          "id": "63e68559-a791-4387-9e95-5e9884503108",
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
              "id": "d4167c95-cb85-4890-8eb8-785b77d52d0a"
            }
          ]
        },
        {
          "id": "4694300a-e307-4a39-ae5e-8409248ab455",
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
              "id": "80019c22-6e39-4067-a5c5-018cc293aebd"
            }
          ]
        },
        {
          "id": "2cc594db-b187-445e-b695-59de70005ff2",
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
              "id": "84dafdee-5bfa-4255-b2d2-a71a54ded136"
            }
          ]
        },
        {
          "id": "874ff8a7-d1e1-4f1d-b006-730a3a9d798e",
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
              "id": "8dc59012-f288-471e-b4cc-a328e3c2002e"
            }
          ]
        },
        {
          "id": "6e4cd227-33db-4965-871e-6d96d57bcee1",
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
              "id": "0b1975b4-c8af-401a-9a66-62b37eba7f4b"
            }
          ]
        },
        {
          "id": "10e70206-b1f5-4728-92c0-626ccddfad2b",
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
              "id": "05247df6-c861-4527-85fa-d0b755ad4b57"
            }
          ]
        },
        {
          "id": "8e94704d-0c5f-4f6f-a065-b561f42b1d88",
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
              "id": "46bada2d-6e4f-473c-98a9-bf5d0defb35d"
            }
          ]
        },
        {
          "id": "64ec538c-b45e-49d5-a672-002dc7d81555",
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
              "id": "5b90bab2-987b-4cdb-b353-c54595744db1"
            }
          ]
        },
        {
          "id": "34ae0f7e-ec6f-40cc-b23c-ac9912a30b5e",
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
              "id": "3c1f614a-d4f6-4518-8b59-03c2c2610277"
            }
          ]
        },
        {
          "id": "97d2370e-c1f3-445d-b011-25c6206e4d52",
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
              "id": "e106de1f-e36f-4e87-8fcd-a7857852f6d8"
            }
          ]
        },
        {
          "id": "1be0e07a-80f7-4cd3-8db5-6aaefbd271b3",
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
              "id": "96148684-5d6f-45ef-a6de-95e6485a52a6"
            }
          ]
        },
        {
          "id": "71f43808-19db-4eda-b540-d17fd845f6c9",
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
              "id": "fa0f88d8-1851-4782-906d-d092b6653c12"
            }
          ]
        },
        {
          "id": "eb61adf2-d8a9-469d-8f43-5b1cc7ce9b1a",
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
              "id": "f75421ab-a3b3-4aac-9141-6100e93abf16"
            }
          ]
        },
        {
          "id": "b5953bde-b577-41fb-aab7-7860d175320c",
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
              "id": "95bc338a-3d33-4d78-ac48-654581c05343"
            }
          ]
        },
        {
          "id": "7b4a4d65-187c-44b6-b0a3-d5699fc5a1ea",
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
              "id": "be5e6a03-2c8d-42af-ab04-976ef8a1b84e"
            }
          ]
        },
        {
          "id": "a7558a0c-fc5a-42d8-881e-0a161fbae448",
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
              "id": "093baa68-161d-44ce-b627-95f36a2d5bc7"
            }
          ]
        },
        {
          "id": "8553f96b-46ba-449e-8ee3-cdd5e27b42dd",
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
              "id": "893c54c0-9a05-40e3-81f2-de8643fad3db"
            }
          ]
        },
        {
          "id": "a149762a-7ba1-4a78-9173-97d2b6776c50",
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
              "id": "9c96564f-1241-44bb-bbdd-93b4946e1ddc"
            }
          ]
        },
        {
          "id": "10ff744a-7958-4d62-be46-94c336e010c0",
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
              "id": "2d064da2-3b3f-485a-b640-ffc63404b6c6"
            }
          ]
        },
        {
          "id": "d9c34424-e02f-4c5d-9183-17f87767c3f0",
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
              "id": "bd039ed7-37f5-4150-8ae4-98dc264a4381"
            }
          ]
        },
        {
          "id": "ea835009-36fc-44c1-ba2d-127e60741a6b",
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
              "id": "dc87bbbb-f9b2-4da6-b8e7-5d150db36b37"
            }
          ]
        },
        {
          "id": "4b841778-500a-4b25-8d2a-062c2bd4866b",
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
              "id": "b33a88e4-edaa-4efa-bc18-ab6977e7f233"
            }
          ]
        },
        {
          "id": "4b5c67e0-5b27-40ad-b14b-0072370bea0f",
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
              "id": "8815d820-673d-4bf4-b5f0-0c9b1c76f3e0"
            }
          ]
        },
        {
          "id": "f1e0dd2e-3e9a-4627-aa45-70008f5ff6a6",
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
              "id": "035ad0e3-1f0d-4337-bab5-0eb699e104c1"
            }
          ]
        },
        {
          "id": "670c250c-930c-4b60-b6f6-9a2e72c36cd7",
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
              "id": "8177c0db-c638-4f48-b949-02895d4ffe1c"
            }
          ]
        },
        {
          "id": "ca14020a-b40b-4fd5-b91b-78a042e9e3cb",
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
              "id": "0d2b8cec-4459-4f4b-a687-dea5af960799"
            }
          ]
        },
        {
          "id": "a1d9d793-8630-42e7-873a-8bacb4865542",
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
              "id": "bb29826b-327b-4ca7-a8ea-afe0c8161eff"
            }
          ]
        },
        {
          "id": "436e7ab1-27ca-47d4-af70-e040f461fbff",
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
              "id": "b8238451-c917-4ace-93f8-a290c11a1e56"
            }
          ]
        },
        {
          "id": "99cfc9ae-9ba8-4ac6-b4cc-cfdabc78fc44",
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
              "id": "2a00f68e-03be-44ec-b045-d37bdd15ab80"
            }
          ]
        },
        {
          "id": "568a9fc1-d46e-4af8-9700-428d922e0f3b",
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
              "id": "e05bc915-6cef-43f2-93e6-65589450bdc4"
            }
          ]
        },
        {
          "id": "22be0577-d883-4aa2-8449-aaf539588169",
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
              "id": "e77a96ea-b8fc-4b18-9f69-7a19c1dbb5ec"
            }
          ]
        },
        {
          "id": "09faf702-129f-4618-afbd-4c59daabc493",
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
              "id": "2f0c85d9-51b1-4d92-90af-ad4d98bd27dc"
            }
          ]
        },
        {
          "id": "f60c5c38-5984-41ec-ad9c-fbc0be54e011",
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
              "id": "c9e20b64-f393-4be3-9cef-58781564b750"
            }
          ]
        },
        {
          "id": "fe278ba8-331a-4f0c-97a0-cf82e360c2ad",
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
              "id": "8a294d89-ac81-496e-aca2-85711288c800"
            }
          ]
        },
        {
          "id": "a6f953a8-e6e5-47c4-8adb-ff3d4d7dc768",
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
              "id": "1427530e-ea4e-41f8-8996-04788b8fc4e7"
            }
          ]
        },
        {
          "id": "b359e171-8cd8-483d-9775-948e6a383ced",
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
              "id": "f40ff3f9-a7fe-4af1-bda2-a5512de93c64"
            }
          ]
        },
        {
          "id": "c4154464-fb1c-4fe5-973b-21b662bc8539",
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
              "id": "ab218375-8959-42a2-a527-f6ae370bf10b"
            }
          ]
        },
        {
          "id": "c1f75066-8d86-4f73-9e4b-9a41feaf5e77",
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
              "id": "17a0242f-09ae-4094-a7e8-50d8fa64f6ca"
            }
          ]
        },
        {
          "id": "12dbf769-4e82-4f50-8d41-95c4a3273251",
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
              "id": "f973a624-3725-4f55-8799-bae254d07565"
            }
          ]
        },
        {
          "id": "4a532d57-ea99-4adf-b17c-faeddd415a19",
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
              "id": "a17e8b0a-b1d6-4cf1-9f82-d81e7a2356ad"
            }
          ]
        },
        {
          "id": "5f0c9dc8-2394-49fb-ad0c-64668967c78c",
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
              "id": "babbd4eb-db47-4a14-acbf-7c078c76a8f7"
            }
          ]
        },
        {
          "id": "9ba4c9c1-f54b-42e7-93a8-aee77e6b4a34",
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
              "id": "ea8ed894-a193-4134-ba81-54c72efc02bb"
            }
          ]
        },
        {
          "id": "e216baba-5a43-4908-b91e-925a16876455",
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
              "id": "f8ab0074-e485-46de-8bf7-4bda7b135a57"
            }
          ]
        },
        {
          "id": "aef1d940-ad00-41c3-b449-0d86f21d6069",
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
              "id": "12d252c3-ffc1-4047-9030-d8a8eb5e4bdd"
            }
          ]
        },
        {
          "id": "7cc5f666-c62f-4337-b17f-43efe267b725",
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
              "id": "885720b3-1c1d-45ab-b205-12e7776790e9"
            }
          ]
        },
        {
          "id": "a2e41e78-7631-495a-a390-90e9eb4ed4a4",
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
              "id": "acc0f5e3-3f61-4824-8f49-0ba3f8b4ecce"
            }
          ]
        },
        {
          "id": "f7aedbf6-d418-4d20-ae57-515f5e287ab1",
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
              "id": "5945c30b-b70b-4019-b5d9-37cb9651e68e"
            }
          ]
        },
        {
          "id": "146b724f-ceab-406f-99ac-34779e525f2e",
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
              "id": "482db5f4-02b0-48a9-af41-3886853ef5f2"
            }
          ]
        },
        {
          "id": "1f5b041a-980c-4691-99bd-e3337275f8da",
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
              "id": "9408d2ce-9e95-4bb0-94ac-8c11abc8b704"
            }
          ]
        },
        {
          "id": "47b63ef6-2970-4c69-a1e1-b6cab4117314",
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
              "id": "263e1d6a-ab3d-42be-baa2-a9993e212a40"
            }
          ]
        },
        {
          "id": "d1a56dc6-406c-4f71-8df5-712d20069be2",
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
              "id": "9cb6893d-2833-4710-a571-9d9259f5499d"
            }
          ]
        },
        {
          "id": "1aeca068-9e49-453e-a035-dd4e270acaa4",
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
              "id": "1a2f9a41-3d67-4397-a3aa-b020ad3deb18"
            }
          ]
        },
        {
          "id": "188c1c00-cb07-4a3b-a75b-0c7586e38835",
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
              "id": "319116f0-2379-4285-96ad-6090a16c6873"
            }
          ]
        },
        {
          "id": "663696f5-97d4-4857-a5c4-9cd9c8197878",
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
              "id": "8fb26ddb-d265-4959-9377-6cc03cdb4ebf"
            }
          ]
        },
        {
          "id": "a4516d55-7abf-4658-a720-35098f8e68b5",
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
              "id": "8a9f4746-2452-444c-8fda-33c36ce789da"
            }
          ]
        },
        {
          "id": "66cb9067-97f5-417c-941a-647f15fe85be",
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
              "id": "02d771f8-5eab-46d0-abc2-0154b29310ce"
            }
          ]
        },
        {
          "id": "79548115-a207-4ac6-b84c-7364605a1dc4",
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
              "id": "adcde1bd-d78a-470d-aab6-9b6112eeb70d"
            }
          ]
        },
        {
          "id": "29cef0be-758a-4359-a765-6d3cc4fc82e5",
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
              "id": "892a61da-6b54-44f2-8c4d-83a853de3f8d"
            }
          ]
        },
        {
          "id": "e97cc371-a339-4d1b-8d63-1404f55f9e89",
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
              "id": "741724f6-4335-441c-9a11-5a3dd79694d1"
            }
          ]
        },
        {
          "id": "461477e7-c423-43bb-ba0c-bdd91c3a4592",
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
              "id": "e69d028d-27c0-4e86-bc5a-3e427b370e1b"
            }
          ]
        },
        {
          "id": "1c18d4c5-a3d8-41e2-830f-14c78ba3c920",
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
              "id": "81b682cf-b61f-4af8-9a84-c533a8017abb"
            }
          ]
        },
        {
          "id": "65d4de95-a3d4-4044-812a-9563aafcc7a6",
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
              "id": "bd198cac-3158-4288-abcf-64f10fd95290"
            }
          ]
        },
        {
          "id": "01315f75-759c-4fd2-8bf3-2b508cb1828b",
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
              "id": "04a34317-5d36-4136-87a4-372fd5a0ac1b"
            }
          ]
        },
        {
          "id": "c0bb0143-f0cd-4f2f-8220-5db2bec65044",
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
              "id": "81aa3d39-b039-4daf-9ec2-79175fad7cba"
            }
          ]
        },
        {
          "id": "ec2b571d-5296-49b6-8f97-448d96b056b8",
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
              "id": "ed0203db-2c83-4de3-b57f-252a6d08be93"
            }
          ]
        },
        {
          "id": "81beda4e-33fd-43e9-bcf2-3e37826ca20b",
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
              "id": "eb00319b-7381-4e79-8dc1-551afa7cd439"
            }
          ]
        },
        {
          "id": "5052c5ad-fec2-4ce3-89fc-d540b0c7150a",
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
              "id": "b0be5707-1646-429b-811d-244c4cf255b9"
            }
          ]
        },
        {
          "id": "da7a3f49-5b54-42b6-a86e-48b706a445b7",
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
              "id": "aa9b5b3d-cc0e-4cda-b8bb-6a919aa6dd9c"
            }
          ]
        },
        {
          "id": "6e488546-fd07-4634-af64-0ab05b90ed94",
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
              "id": "e9cb2fdd-9d6e-47f4-a806-0f158fd4fdee"
            }
          ]
        },
        {
          "id": "922dd595-496a-401c-9e1e-a615ba68d725",
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
              "id": "b47d8a79-3b89-4cce-bf79-1d27e4bb5663"
            }
          ]
        },
        {
          "id": "35e56059-d6fc-4523-8203-8151eeeb0007",
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
              "id": "d7f097e7-c481-448e-9ae3-2fbc241adda3"
            }
          ]
        },
        {
          "id": "e294209a-7dfe-4cf1-94b5-a5c33fd36393",
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
              "id": "fbbcf72d-42e5-4dc1-ad34-a0d8054474d6"
            }
          ]
        },
        {
          "id": "1abb1667-f1d7-4002-8e7d-af9abff0cd53",
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
              "id": "2dcb1ace-ca4b-47fa-8492-e48b6cb98133"
            }
          ]
        },
        {
          "id": "8de1618a-e737-4e15-ab66-49efe77203e7",
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
              "id": "f8c9fa79-b93a-4be1-893b-aaf529b93e2a"
            }
          ]
        }
      ]
    }
  ]
}