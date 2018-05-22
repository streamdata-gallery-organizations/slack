{
  "info": {
    "name": "Slack End Do Not Disturb Snooze",
    "_postman_id": "732daccf-f0a4-4b7f-b5a0-25c7c478d4cb",
    "description": "Ends the current user's snooze mode immediately.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Messages",
      "item": [
        {
          "id": "73fa5ddf-ca42-43fe-bfea-d737c0771447",
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
              "id": "c5ea394f-4792-440b-8cfc-3b0ad5649119"
            }
          ]
        },
        {
          "id": "81d9e320-f962-4c4c-bf02-1d7c9f676fcb",
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
              "id": "efb7081e-4d7d-4506-83de-b73d47ce1358"
            }
          ]
        },
        {
          "id": "097e21c9-af3c-48fc-8d7a-eb9e768dcd45",
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
              "id": "aef9848a-f6be-47e2-90da-5c2cef5469a9"
            }
          ]
        },
        {
          "id": "7d57a501-ad8c-4c70-a572-84eb8b8a1280",
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
              "id": "9e022964-8b09-460e-bf74-32e6c4b1daab"
            }
          ]
        },
        {
          "id": "628b6e57-2d85-493c-b3f3-2d38cac3cec9",
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
              "id": "07208165-9d1a-420c-9625-ad92d4a99cd7"
            }
          ]
        },
        {
          "id": "5455d4e5-ef04-47e7-a43d-f3dab517bd17",
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
              "id": "f5db3723-9be1-40fe-af1e-b161e41147c0"
            }
          ]
        }
      ]
    },
    {
      "name": "Messaging",
      "item": [
        {
          "id": "018f065d-9559-4556-8cce-d1998b259f80",
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
              "id": "32fac753-d47f-49f6-a8af-f9d243c1f7fc"
            }
          ]
        },
        {
          "id": "b84967b5-b9c6-43e5-a0f4-d3e932a9ab0a",
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
              "id": "34b34cac-532b-467a-b12c-dbc09f6393b3"
            }
          ]
        },
        {
          "id": "d0a159ef-c998-4b78-879d-04d0dd139f50",
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
              "id": "c748a95b-5bae-4194-b3c2-d0f5b0ba6d1b"
            }
          ]
        },
        {
          "id": "c289c09d-605b-4084-8a3e-3bf72b52b5ed",
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
              "id": "41aa8202-4805-4199-a611-be9e0ee920a2"
            }
          ]
        },
        {
          "id": "ef6f83b6-2e72-4704-98f3-7dd4395efa01",
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
              "id": "f1ab0237-c103-4169-b7d7-027497d903d1"
            }
          ]
        },
        {
          "id": "78212319-6523-4ca8-9b4e-3aec9075022a",
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
              "id": "ed8229ae-7dfa-481f-ae5a-ff2f20eb3715"
            }
          ]
        },
        {
          "id": "f6b3e75f-2f3c-485c-8465-ec3fb57d6e58",
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
              "id": "ed4d45f7-fe19-4b4b-a063-6e5da15dc3aa"
            }
          ]
        },
        {
          "id": "2a455663-b54c-4a26-8392-06412011506c",
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
              "id": "9fc22b6b-da80-4229-96d0-a64f1624dcbb"
            }
          ]
        },
        {
          "id": "7c97e5b1-7dd3-47de-914e-ac0efafd1309",
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
              "id": "c6a5dea0-b123-4382-a317-5a50153e9089"
            }
          ]
        },
        {
          "id": "66a247c7-36ac-4d18-a00a-c33d12e2d233",
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
              "id": "e847b8af-f11b-45ae-b03b-0b176105b813"
            }
          ]
        },
        {
          "id": "0b1b0d7a-c506-4b8a-8110-f2c7f6fa61d2",
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
              "id": "77546645-32f3-4477-9ea5-a78865790253"
            }
          ]
        },
        {
          "id": "abe8cdb7-8732-4dc0-95b3-2fef08a0b427",
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
              "id": "42c5ea49-8127-4b61-8484-18ca154f3328"
            }
          ]
        },
        {
          "id": "5ac5bd5f-1eb3-46eb-be0b-d4d173638a99",
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
              "id": "e5eb675f-4ebe-437f-b7fe-e0a5ea200df1"
            }
          ]
        },
        {
          "id": "e731913d-4f6f-426f-8a7e-88fa74aea73c",
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
              "id": "04485f99-f49b-4bf7-bb2e-7df8e4c7aff2"
            }
          ]
        },
        {
          "id": "14a2a0ed-7abd-437b-88c6-4d16608274e1",
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
              "id": "f67860ee-073e-4e7f-a672-40c48e6bf14c"
            }
          ]
        },
        {
          "id": "b1598d1c-bdf6-4a32-8808-acc8570262d9",
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
              "id": "2a6ea751-f813-4c25-83fe-3892c6da9406"
            }
          ]
        },
        {
          "id": "28e979a3-b781-45dd-9d8e-ddc373ae4d46",
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
              "id": "4e1e0ed4-ea77-4879-aa6b-46200d25dd77"
            }
          ]
        },
        {
          "id": "78597d62-7880-461a-afda-3b8f0975f7f3",
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
              "id": "3503a875-81ae-44ff-ace9-4a90e6044af6"
            }
          ]
        },
        {
          "id": "47362720-5c89-4e2d-9c32-d52636494112",
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
              "id": "bec5f42c-f2f2-4e90-ba8d-2131e8e58f40"
            }
          ]
        },
        {
          "id": "bf8660c0-3cba-41b8-b37e-5cbda5f5a0f5",
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
              "id": "ae138ef0-44f2-49fd-b5b6-88519eb7757d"
            }
          ]
        },
        {
          "id": "6a09d850-92d9-4a32-bb64-87834fe4b157",
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
              "id": "1dca578a-528f-44b6-a7c2-9fa3ed9f23ce"
            }
          ]
        },
        {
          "id": "1431b0db-3277-48b4-a49d-9007b13fa707",
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
              "id": "afea79dd-e586-416c-99ea-0b57cc626067"
            }
          ]
        },
        {
          "id": "f12be642-c87f-42cd-b12c-1b610bb7b5f6",
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
              "id": "51199a75-1af0-4245-8512-a315bf0fc628"
            }
          ]
        },
        {
          "id": "7c6222a9-5cf9-48d3-8b56-346d6cccb8c0",
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
              "id": "5b47dd19-d543-48ed-9bee-d79585791e85"
            }
          ]
        },
        {
          "id": "0a342508-a3ee-4cfa-a762-cd6b0d9cd19a",
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
              "id": "d4aa890f-7086-4748-8160-6490fd3210c9"
            }
          ]
        },
        {
          "id": "ef2870c6-2c35-4137-aec6-3d0e33665626",
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
              "id": "815dd29b-4dcc-4f96-80f7-39163169b442"
            }
          ]
        },
        {
          "id": "ad972e42-0bfa-40e7-a905-28357ca27ae8",
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
              "id": "caabdf69-1715-4c4d-8ee5-7f47bf892ba6"
            }
          ]
        },
        {
          "id": "ba471c79-c8a3-4716-90ba-292e4a0e1513",
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
              "id": "7d96b4d1-3763-4fd9-ab20-c8348e6e987c"
            }
          ]
        },
        {
          "id": "56cc0bed-6827-4dbd-94f3-fb63b4941a24",
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
              "id": "3518c478-5b64-49d0-8e3c-2f6f55184262"
            }
          ]
        },
        {
          "id": "9c20f4f5-882d-4687-9855-8b718ff63e42",
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
              "id": "50d243f3-2ac4-4153-b3ac-034a35b2bb63"
            }
          ]
        },
        {
          "id": "ecaeae0f-810e-41be-ba7b-45b5c91e9b19",
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
              "id": "f7aeaf7d-0c4f-4c9b-8bf9-a0fa11366668"
            }
          ]
        },
        {
          "id": "c728c937-a7c7-4a3c-ad86-c2664410d6fe",
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
              "id": "cd0733f6-d0f6-4030-8dad-f751c3edd8e2"
            }
          ]
        },
        {
          "id": "f115017e-ecb6-4169-9dff-39a6cebed240",
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
              "id": "4fb7c271-1b87-4ba6-b3ce-04478fc335f3"
            }
          ]
        },
        {
          "id": "6820c344-8cda-4b4a-b595-7a4b7f882b9a",
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
              "id": "2c6b8eeb-56c4-4612-b8e8-95cbcad2b8fe"
            }
          ]
        },
        {
          "id": "a8d51a37-6657-48c9-95c5-7a9839226772",
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
              "id": "2d980232-1c5a-449c-983d-842006dd95f9"
            }
          ]
        },
        {
          "id": "f0323dba-753a-4ace-b6d6-51a6e89f83d5",
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
              "id": "3e891fe1-3748-4e1b-9fdd-9993c6b92f8d"
            }
          ]
        },
        {
          "id": "b7c82b93-9ca5-4987-8456-e59c6f2379e9",
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
              "id": "2123620e-7cf4-4c0f-8899-538f78172dc7"
            }
          ]
        },
        {
          "id": "29f9c9d3-54a2-4f04-8607-2602a60cdfa3",
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
              "id": "68bcf25c-1aa0-474b-a092-df574a8307d6"
            }
          ]
        },
        {
          "id": "1db79b43-b68c-49da-ba41-5c8b9ef15ee3",
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
              "id": "5d3ff7b8-20d7-4409-a418-cdd93805aa99"
            }
          ]
        },
        {
          "id": "76d504a0-bc93-4707-93f6-94342d835634",
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
              "id": "96714e3b-d76b-4d7d-8e9c-449498fd8511"
            }
          ]
        },
        {
          "id": "723f6a70-c8f4-4375-b772-10fe6e153d97",
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
              "id": "e1e649f4-f3e4-4d73-a652-306f02d41d8a"
            }
          ]
        },
        {
          "id": "52d84857-1d4d-4322-a9b2-3c352474cf3b",
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
              "id": "da0d3fdb-66f0-4acd-8b4c-3d9e280fd79f"
            }
          ]
        },
        {
          "id": "c60ed852-7b4b-44d1-af82-4207db721fa4",
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
              "id": "af817d04-8cc4-4232-922e-9c896af2be72"
            }
          ]
        },
        {
          "id": "ec418d19-c727-4538-8719-be114766e793",
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
              "id": "133ca5fd-6c4c-484d-8814-37a8667c8266"
            }
          ]
        },
        {
          "id": "1d4db06a-7211-4910-8139-ee28c9143e3d",
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
              "id": "2af3985b-397a-4594-8429-47125cb7acaf"
            }
          ]
        },
        {
          "id": "8efee3dc-42df-4be9-a64e-57c98c4d3d8e",
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
              "id": "db5514af-1155-4e66-bfc6-4de56f3d076e"
            }
          ]
        },
        {
          "id": "32d47732-0161-459d-86c1-289df1478963",
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
              "id": "8f80dc7e-f85d-47ed-a5bd-504c47d657ab"
            }
          ]
        },
        {
          "id": "42cd390d-ba5b-4a0c-980a-12d508496a67",
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
              "id": "ec34647e-5ce8-4642-8f9a-c9859e1bbe0b"
            }
          ]
        },
        {
          "id": "a2f1e18f-8718-4d9a-95d3-1353e1c4f3ae",
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
              "id": "1af37d30-6db6-489d-aaf6-05cd4c839ac1"
            }
          ]
        },
        {
          "id": "e1fe58cc-3917-485b-a34a-c6cbcde28fb3",
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
              "id": "b5a620f0-528a-49c2-bbc7-a62d51cd2abd"
            }
          ]
        },
        {
          "id": "859f4801-cad6-4582-a8ef-7563ae44bfb1",
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
              "id": "139e38d1-7f3c-4c1a-8785-b1f5dc763a9a"
            }
          ]
        },
        {
          "id": "2583186d-33a6-4be0-8a54-4b14f3834073",
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
              "id": "5a304dac-afb4-45a4-9e84-157117ec4e0c"
            }
          ]
        },
        {
          "id": "1ab5e359-6fe9-477a-bd6c-6ea27427cec9",
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
              "id": "66faa4ac-d29c-4f07-957c-64f6b885153d"
            }
          ]
        },
        {
          "id": "e52f3449-799e-4012-8e84-0e336268b0d2",
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
              "id": "6f44e5d7-ca81-4860-b616-28a631b6c3d2"
            }
          ]
        },
        {
          "id": "627396d6-a0b6-487f-8774-bcb7de832f4c",
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
              "id": "8100d1aa-c203-40dc-beeb-db5db8e16906"
            }
          ]
        },
        {
          "id": "f59cc5e5-709a-4e03-bc10-53aae7393279",
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
              "id": "e30d7d20-d68f-4fe6-914f-514adf1f0ba9"
            }
          ]
        },
        {
          "id": "c43d1cda-d15f-4c3f-9806-74702e8fc011",
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
              "id": "587b193c-db8b-4aef-b567-46bf0b337c58"
            }
          ]
        },
        {
          "id": "0e01f754-717f-4a4e-a310-16ceef2e6a10",
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
              "id": "6e7f693c-c7f5-44f8-884a-df6ef0b3ff13"
            }
          ]
        },
        {
          "id": "5f1ff41b-2335-43d0-a363-30350f1da275",
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
              "id": "30f39dfe-be86-4c6c-a045-54f5f65b72ff"
            }
          ]
        },
        {
          "id": "45e763b9-317b-4aed-80c0-d59c86801bbb",
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
              "id": "5c7dfeef-97eb-4e70-82f5-ec63cc610ad1"
            }
          ]
        },
        {
          "id": "a03c2ded-de94-437b-b6f8-d44584ae8479",
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
              "id": "7864cd6f-9a37-4309-8464-27653e788a90"
            }
          ]
        },
        {
          "id": "06aeb355-1997-4baa-9836-1fcad8382a3c",
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
              "id": "712f1820-1f56-4d6d-9f3e-e5f7603285d6"
            }
          ]
        },
        {
          "id": "819c7382-29e3-4103-8916-822d2a032c5a",
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
              "id": "74ebb25e-9c32-4741-86a7-f850df97da63"
            }
          ]
        },
        {
          "id": "9c3ac286-6a10-4da2-8c09-504484333171",
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
              "id": "7a1acbca-3c50-4cd2-bfaa-a44b2a5d5e87"
            }
          ]
        },
        {
          "id": "b8402df3-3c38-45cb-8b13-340b7b8d1b6c",
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
              "id": "188bbb26-8741-46be-8ad0-07862c062fbd"
            }
          ]
        },
        {
          "id": "3bba0fa6-3afc-4aa1-8a0a-9f785022a210",
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
              "id": "879dee86-77f9-4766-b29e-c7852ef1e03a"
            }
          ]
        },
        {
          "id": "e0aa6648-f4e5-470f-b5b1-7e62ff8361d4",
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
              "id": "308fe820-cfc9-4c8f-b675-28cf9fde7cc5"
            }
          ]
        },
        {
          "id": "e1c51a43-96e6-4c14-a56e-646b7f8c9c69",
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
              "id": "187c74d7-6e1e-4e48-8600-d91dda7b959c"
            }
          ]
        },
        {
          "id": "39022a6c-4dfe-4349-873b-c36d2aa786c7",
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
              "id": "c32e9547-6a39-45ab-a0af-3c6edbf8366c"
            }
          ]
        },
        {
          "id": "5ddf8201-f34f-4d2f-98fd-c4d524276177",
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
              "id": "8e8fed48-585d-4918-877e-0e2dcecb8ddd"
            }
          ]
        },
        {
          "id": "0a3059f8-70a1-44d5-8b1a-911915625711",
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
              "id": "1c4f81e7-4bdb-424f-87fc-fa9344cf9187"
            }
          ]
        },
        {
          "id": "28687f66-81ab-4143-9c71-93f62d4da8c0",
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
              "id": "eb99a443-7cd7-4fbb-b215-99f1ccc8b84e"
            }
          ]
        },
        {
          "id": "c92f2df0-350f-48b4-a672-8bb7e0604478",
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
              "id": "4ed1fbb0-6d97-4ef4-9353-8fb30fce8b27"
            }
          ]
        },
        {
          "id": "1f1939a1-b365-4f85-8449-64a3764feddd",
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
              "id": "be53f790-cd0d-4e9b-abb1-f8668cd51f64"
            }
          ]
        },
        {
          "id": "a9a6afc7-ba99-4fde-be9a-02f374fafd36",
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
              "id": "e501f957-b77e-45d3-81f2-c5bf89dee75a"
            }
          ]
        },
        {
          "id": "3d25d784-ee5b-4494-bbb4-5163e949b995",
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
              "id": "59f78b10-2242-4730-9f9e-503bae7d71d6"
            }
          ]
        },
        {
          "id": "a3dd0c21-01e0-488a-895e-4d09d69e1b9c",
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
              "id": "87e2609d-74f5-4a81-89ff-49eeef93a6d5"
            }
          ]
        },
        {
          "id": "5d8fe550-e8d4-4374-a4c2-c5d209918536",
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
              "id": "c3864cdc-2bd0-4ba0-8a08-5d13802fc001"
            }
          ]
        },
        {
          "id": "6d75d49a-0efd-41bd-ae6a-4991c13a621f",
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
              "id": "0b874f14-1c41-493d-9f2f-89a0bbaf1955"
            }
          ]
        },
        {
          "id": "427bd548-37a4-44bb-8df1-e762fdfc3d31",
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
              "id": "93993b67-fb4f-41bc-b47f-f30114a2b37a"
            }
          ]
        },
        {
          "id": "a49fd7d0-4365-4ae4-a1e2-06fefcc0954d",
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
              "id": "49726f40-a20e-4fd5-88e8-8aadf707f37d"
            }
          ]
        },
        {
          "id": "d6148f64-527f-453d-a90a-fae28c75e186",
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
              "id": "6ab7035b-d688-4d44-af87-1cc276201d1a"
            }
          ]
        },
        {
          "id": "726ffc27-edb3-4fa8-83a8-e761208ba324",
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
              "id": "f905731a-c96f-4d28-9a98-4d5a4890f6db"
            }
          ]
        },
        {
          "id": "ac87a069-e526-4c92-82c9-5bfd7677566e",
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
              "id": "60df8243-5f62-4aaa-9e0e-26019a44dcac"
            }
          ]
        },
        {
          "id": "126cf782-74c7-47af-a44e-c7273e985aa6",
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
              "id": "cc58d530-300d-4ade-a51a-c49d75b75b6d"
            }
          ]
        },
        {
          "id": "08350c7b-fe4d-416e-bdbe-2d92c77227d0",
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
              "id": "c7663ba6-f0db-462d-aee5-57a431622e8b"
            }
          ]
        },
        {
          "id": "a8d2f2c9-7b12-4dd8-9e81-1d0814c2bece",
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
              "id": "b5f25321-ad8a-40ff-840e-532efddd93ec"
            }
          ]
        },
        {
          "id": "bbfa3ff6-5bd9-4d3a-aa3c-854f6bb7220b",
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
              "id": "cb2d3d0c-c189-481d-8de8-76e4dadbddfd"
            }
          ]
        },
        {
          "id": "e9c33914-1669-4deb-bcb5-71565c266000",
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
              "id": "b7333284-b9d9-4585-aaf3-5c22cd672ed9"
            }
          ]
        },
        {
          "id": "48e31ba7-2b3c-4c9f-a6ee-2c68d4a0790c",
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
              "id": "df9d2aad-64b5-461a-a915-79c806ab7324"
            }
          ]
        },
        {
          "id": "881dd87c-9da1-4544-8815-4f3de3a15ec7",
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
              "id": "93ed01cb-afbf-4bb0-8761-e6257c5c652d"
            }
          ]
        },
        {
          "id": "ac7ff0a5-da13-422e-a5fa-93b20d46dad2",
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
              "id": "5e44061f-2a9c-4a46-984f-3394ae3f588a"
            }
          ]
        },
        {
          "id": "3758fc47-4247-4233-857b-68d12b945187",
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
              "id": "ed971e9c-a4e0-49be-90c3-d5a7903e3857"
            }
          ]
        },
        {
          "id": "033a1d17-9a35-4b2a-acd4-58db427986ba",
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
              "id": "b63f1dbc-deef-4c0e-92fb-2f6c2ccb2de9"
            }
          ]
        },
        {
          "id": "88f1e4c0-091c-498a-bf38-c3e2d1d212e4",
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
              "id": "7e013384-888f-49d8-85fa-a1306a30d1df"
            }
          ]
        },
        {
          "id": "e398db4d-f843-4a02-b039-bbd9d55e72e4",
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
              "id": "e896f0fe-3314-46a0-9aa9-50c76253749d"
            }
          ]
        },
        {
          "id": "12c40f07-b15a-4990-8f0c-831868daedea",
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
              "id": "4e6b5c5b-aa4c-4e68-8d1c-0faac214d610"
            }
          ]
        }
      ]
    }
  ]
}