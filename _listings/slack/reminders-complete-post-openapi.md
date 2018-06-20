---
swagger: "2.0"
x-collection-name: Slack
x-complete: 0
info:
  title: Slack Mark Reminders Complete
  description: Marks a reminder as complete.
  version: 1.0.3
host: slack.com
basePath: /api
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /chat.delete:
    post:
      summary: Delete Message
      description: Deletes a message.
      operationId: chat_delete
      x-api-path-slug: chat-delete-post
      parameters:
      - in: formData
        name: as_user
        description: Pass true to delete the message as the authed user with `chat:write:user`
          scope
      - in: formData
        name: channel
        description: Channel containing the message to be deleted
      - in: header
        name: token
        description: Authentication token
      - in: formData
        name: ts
        description: Timestamp of the message to be deleted
      responses:
        200:
          description: OK
      tags:
      - Messages
  /files.comments.edit:
    post:
      summary: Edit File Comments
      description: Edit an existing file comment.
      operationId: files_comments_edit
      x-api-path-slug: files-comments-edit-post
      parameters:
      - in: formData
        name: comment
        description: Text of the comment to edit
      - in: formData
        name: file
        description: File containing the comment to edit
      - in: formData
        name: id
        description: The comment to edit
      - in: header
        name: token
        description: Authentication token
      responses:
        200:
          description: OK
      tags:
      - Messaging
      - Files
      - Comments
  /im.close:
    post:
      summary: Close Group
      description: Close a direct message channel.
      operationId: im_close
      x-api-path-slug: im-close-post
      parameters:
      - in: formData
        name: channel
        description: Direct message channel to close
      - in: header
        name: token
        description: Authentication token
      responses:
        200:
          description: OK
      tags:
      - Messaging
  /groups.replies:
    get:
      summary: Get Group Thread
      description: Retrieve a thread of messages posted to a private channel
      operationId: groups_replies
      x-api-path-slug: groups-replies-get
      parameters:
      - in: query
        name: channel
        description: Private channel to fetch thread from
      - in: query
        name: thread_ts
        description: Unique identifier of a threads parent message
      - in: query
        name: token
        description: Authentication token
      responses:
        200:
          description: OK
      tags:
      - Messaging
      - Groups
  /bots.info:
    get:
      summary: Get Bot Info
      description: Gets information about a bot user.
      operationId: bots_info
      x-api-path-slug: bots-info-get
      parameters:
      - in: query
        name: bot
        description: Bot user to get info on
      - in: query
        name: token
        description: Authentication token
      responses:
        200:
          description: OK
      tags:
      - Messaging
      - Bots
  /groups.rename:
    post:
      summary: Rename Group
      description: Renames a private channel.
      operationId: groups_rename
      x-api-path-slug: groups-rename-post
      parameters:
      - in: formData
        name: channel
        description: Private channel to rename
      - in: formData
        name: name
        description: New name for private channel
      - in: header
        name: token
        description: Authentication token
      - in: formData
        name: validate
        description: Whether to return errors on invalid channel name instead of modifying
          it to meet the specified criteria
      responses:
        200:
          description: OK
      tags:
      - Messaging
      - Groups
  /users.profile.set:
    post:
      summary: Set User Profile
      description: Set the profile information for a user.
      operationId: users_profile_set
      x-api-path-slug: users-profile-set-post
      parameters:
      - in: formData
        name: name
        description: Name of a single key to set
      - in: formData
        name: profile
        description: Collection of key:value pairs presented as a URL-encoded JSON
          hash
      - in: header
        name: token
        description: Authentication token
      - in: formData
        name: user
        description: ID of user to change
      - in: formData
        name: value
        description: Value to set a single key to
      responses:
        200:
          description: OK
      tags:
      - Messaging
      - Users
  /users.setPresence:
    post:
      summary: Set User Presence
      description: Manually sets user presence.
      operationId: users_setPresence
      x-api-path-slug: users-setpresence-post
      parameters:
      - in: formData
        name: presence
        description: Either `auto` or `away`
      - in: header
        name: token
        description: Authentication token
      responses:
        200:
          description: OK
      tags:
      - Messaging
      - Users
  /conversations.close:
    post:
      summary: Close Conversation
      description: Closes a direct message or multi-person direct message.
      operationId: conversations_close
      x-api-path-slug: conversations-close-post
      parameters:
      - in: formData
        name: channel
        description: Conversation to close
      - in: header
        name: token
        description: Authentication token
      responses:
        200:
          description: OK
      tags:
      - Messaging
      - Conversations
  /im.open:
    post:
      summary: Open Messages
      description: Opens a direct message channel.
      operationId: im_open
      x-api-path-slug: im-open-post
      parameters:
      - in: formData
        name: include_locale
        description: Set this to `true` to receive the locale for this im
      - in: formData
        name: return_im
        description: Boolean, indicates you want the full IM channel definition in
          the response
      - in: header
        name: token
        description: Authentication token
      - in: formData
        name: user
        description: User to open a direct message channel with
      responses:
        200:
          description: OK
      tags:
      - Messaging
  /groups.list:
    get:
      summary: Get Group
      description: Lists private channels that the calling user has access to.
      operationId: groups_list
      x-api-path-slug: groups-list-get
      parameters:
      - in: query
        name: exclude_archived
        description: Dont return archived private channels
      - in: query
        name: exclude_members
        description: Exclude the `members` from each `group`
      - in: query
        name: token
        description: Authentication token
      responses:
        200:
          description: OK
      tags:
      - Messaging
      - Groups
  /team.integrationLogs:
    get:
      summary: Get Team Logs
      description: Gets the integration logs for the current team.
      operationId: team_integrationLogs
      x-api-path-slug: team-integrationlogs-get
      parameters:
      - in: query
        name: app_id
        description: Filter logs to this Slack app
      - in: query
        name: change_type
        description: Filter logs with this change type
      - in: query
        name: count
      - in: query
        name: page
      - in: query
        name: service_id
        description: Filter logs to this service
      - in: query
        name: token
        description: Authentication token
      - in: query
        name: user
        description: Filter logs generated by this users actions
      responses:
        200:
          description: OK
      tags:
      - Messaging
      - Teams
  /groups.kick:
    post:
      summary: Remove User From Group
      description: Removes a user from a private channel.
      operationId: groups_kick
      x-api-path-slug: groups-kick-post
      parameters:
      - in: formData
        name: channel
        description: Private channel to remove user from
      - in: header
        name: token
        description: Authentication token
      - in: formData
        name: user
        description: User to remove from private channel
      responses:
        200:
          description: OK
      tags:
      - Messaging
      - Groups
  /dnd.info:
    get:
      summary: Get Do Not Disturb
      description: Retrieves a user's current Do Not Disturb status.
      operationId: dnd_info
      x-api-path-slug: dnd-info-get
      parameters:
      - in: query
        name: token
        description: Authentication token
      - in: query
        name: user
        description: User to fetch status for (defaults to current user)
      responses:
        200:
          description: OK
      tags:
      - Messaging
      - Do Not Disturb
  /channels.archive:
    post:
      summary: Archive Channel
      description: Archives a channel.
      operationId: channels_archive
      x-api-path-slug: channels-archive-post
      parameters:
      - in: formData
        name: channel
        description: Channel to archive
      - in: header
        name: token
        description: Authentication token
      responses:
        200:
          description: OK
      tags:
      - Messaging
      - Channels
      - Archives
  /reminders.info:
    get:
      summary: Get Reminder
      description: Gets information about a reminder.
      operationId: reminders_info
      x-api-path-slug: reminders-info-get
      parameters:
      - in: query
        name: reminder
        description: The ID of the reminder
      - in: query
        name: token
        description: Authentication token
      responses:
        200:
          description: OK
      tags:
      - Messaging
      - Reminders
  /channels.info:
    get:
      summary: Get Channel
      description: Gets information about a channel.
      operationId: channels_info
      x-api-path-slug: channels-info-get
      parameters:
      - in: query
        name: channel
        description: Channel to get info on
      - in: query
        name: include_locale
        description: Set this to `true` to receive the locale for this channel
      - in: query
        name: token
        description: Authentication token
      responses:
        200:
          description: OK
      tags:
      - Messaging
      - Channels
  /channels.kick:
    post:
      summary: Remove User From Channel
      description: Removes a user from a channel.
      operationId: channels_kick
      x-api-path-slug: channels-kick-post
      parameters:
      - in: formData
        name: channel
        description: Channel to remove user from
      - in: header
        name: token
        description: Authentication token
      - in: formData
        name: user
        description: User to remove from channel
      responses:
        200:
          description: OK
      tags:
      - Messaging
      - Channels
  /groups.mark:
    post:
      summary: Mark Group
      description: Sets the read cursor in a private channel.
      operationId: groups_mark
      x-api-path-slug: groups-mark-post
      parameters:
      - in: formData
        name: channel
        description: Private channel to set reading cursor in
      - in: header
        name: token
        description: Authentication token
      - in: formData
        name: ts
        description: Timestamp of the most recently seen message
      responses:
        200:
          description: OK
      tags:
      - Messaging
      - Groups
  /mpim.close:
    post:
      summary: Close Multiparty Direct Message
      description: Closes a multiparty direct message channel.
      operationId: mpim_close
      x-api-path-slug: mpim-close-post
      parameters:
      - in: formData
        name: channel
        description: MPIM to close
      - in: header
        name: token
        description: Authentication token
      responses:
        200:
          description: OK
      tags:
      - Messaging
  /conversations.join:
    post:
      summary: Join Conversation
      description: Joins an existing conversation.
      operationId: conversations_join
      x-api-path-slug: conversations-join-post
      parameters:
      - in: formData
        name: channel
        description: ID of conversation to join
      - in: header
        name: token
        description: Authentication token
      responses:
        200:
          description: OK
      tags:
      - Messaging
      - Conversations
  /channels.history:
    get:
      summary: Get Channel History
      description: Fetches history of messages and events from a channel.
      operationId: channels_history
      x-api-path-slug: channels-history-get
      parameters:
      - in: query
        name: channel
        description: Channel to fetch history for
      - in: query
        name: count
        description: Number of messages to return, between 1 and 1000
      - in: query
        name: inclusive
        description: Include messages with latest or oldest timestamp in results
      - in: query
        name: latest
        description: End of time range of messages to include in results
      - in: query
        name: oldest
        description: Start of time range of messages to include in results
      - in: query
        name: token
        description: Authentication token
      - in: query
        name: unreads
        description: Include `unread_count_display` in the output?
      responses:
        200:
          description: OK
      tags:
      - Messaging
      - Channels
  /im.mark:
    post:
      summary: Mark Messages
      description: Sets the read cursor in a direct message channel.
      operationId: im_mark
      x-api-path-slug: im-mark-post
      parameters:
      - in: formData
        name: channel
        description: Direct message channel to set reading cursor in
      - in: header
        name: token
        description: Authentication token
      - in: formData
        name: ts
        description: Timestamp of the most recently seen message
      responses:
        200:
          description: OK
      tags:
      - Messaging
  /oauth.token:
    get:
      summary: Oauth Token
      description: Exchanges a temporary OAuth verifier code for a workspace token.
      operationId: oauth_token
      x-api-path-slug: oauth-token-get
      parameters:
      - in: query
        name: client_id
        description: Issued when you created your application
      - in: query
        name: client_secret
        description: Issued when you created your application
      - in: query
        name: code
        description: The `code` param returned via the OAuth callback
      - in: query
        name: redirect_uri
        description: This must match the originally submitted URI (if one was sent)
      - in: query
        name: single_channel
        description: Request the user to add your app only to a single channel
      responses:
        200:
          description: OK
      tags:
      - Messaging
      - OAuth
  /files.upload:
    post:
      summary: Upload File
      description: Uploads or creates a file.
      operationId: files_upload
      x-api-path-slug: files-upload-post
      parameters:
      - in: formData
        name: channels
        description: Comma-separated list of channel names or IDs where the file will
          be shared
      - in: formData
        name: content
        description: File contents via a POST variable
      - in: formData
        name: file
        description: File contents via `multipart/form-data`
      - in: formData
        name: filename
        description: Filename of file
      - in: formData
        name: filetype
        description: A [file type](/types/file#file_types) identifier
      - in: formData
        name: initial_comment
        description: Initial comment to add to file
      - in: formData
        name: title
        description: Title of file
      - in: formData
        name: token
        description: Authentication token
      responses:
        200:
          description: OK
      tags:
      - Messaging
      - Files
  /usergroups.users.list:
    get:
      summary: List Group Users
      description: List all users in a User Group
      operationId: usergroups_users_list
      x-api-path-slug: usergroups-users-list-get
      parameters:
      - in: query
        name: include_disabled
        description: Allow results that involve disabled User Groups
      - in: query
        name: token
        description: Authentication token
      - in: query
        name: usergroup
        description: The encoded ID of the User Group to update
      responses:
        200:
          description: OK
      tags:
      - Messaging
      - Groups
  /users.info:
    get:
      summary: Get User Info
      description: Gets information about a user.
      operationId: users_info
      x-api-path-slug: users-info-get
      parameters:
      - in: query
        name: include_locale
        description: Set this to `true` to receive the locale for this user
      - in: query
        name: token
        description: Authentication token
      - in: query
        name: user
        description: User to get info on
      responses:
        200:
          description: OK
      tags:
      - Messaging
      - Users
  /users.lookupByEmail:
    get:
      summary: Find User
      description: Find a user with an email address.
      operationId: users_lookupByEmail
      x-api-path-slug: users-lookupbyemail-get
      parameters:
      - in: query
        name: email
        description: An email address belonging to a user in the workspace
      - in: query
        name: token
        description: Authentication token
      responses:
        200:
          description: OK
      tags:
      - Messaging
      - Users
  /reactions.list:
    get:
      summary: List Reactions
      description: Lists reactions made by a user.
      operationId: reactions_list
      x-api-path-slug: reactions-list-get
      parameters:
      - in: query
        name: count
      - in: query
        name: full
        description: If true always return the complete reaction list
      - in: query
        name: page
      - in: query
        name: token
        description: Authentication token
      - in: query
        name: user
        description: Show reactions made by this user
      responses:
        200:
          description: OK
      tags:
      - Messaging
      - Reactions
  /conversations.create:
    post:
      summary: Create Conversation
      description: Initiates a public or private channel-based conversation
      operationId: conversations_create
      x-api-path-slug: conversations-create-post
      parameters:
      - in: formData
        name: is_private
        description: Create a private channel instead of a public one
      - in: formData
        name: name
        description: Name of the public or private channel to create
      - in: header
        name: token
        description: Authentication token
      responses:
        200:
          description: OK
      tags:
      - Messaging
      - Conversations
  /team.billableInfo:
    get:
      summary: Get Billable Info
      description: Gets billable users information for the current team.
      operationId: team_billableInfo
      x-api-path-slug: team-billableinfo-get
      parameters:
      - in: query
        name: token
        description: Authentication token
      - in: query
        name: user
        description: A user to retrieve the billable information for
      responses:
        200:
          description: OK
      tags:
      - Messaging
      - Billing
  /dnd.endDnd:
    post:
      summary: End Do Not Disturb
      description: Ends the current user's Do Not Disturb session immediately.
      operationId: dnd_endDnd
      x-api-path-slug: dnd-enddnd-post
      parameters:
      - in: header
        name: token
        description: Authentication token
      responses:
        200:
          description: OK
      tags:
      - Messaging
      - Do Not Disturb
  /search.all:
    get:
      summary: Search Real Time Messaging
      description: Searches for messages and files matching a query.
      operationId: search_all
      x-api-path-slug: search-all-get
      parameters:
      - in: query
        name: count
      - in: query
        name: highlight
        description: Pass a value of `true` to enable query highlight markers (see
          below)
      - in: query
        name: page
      - in: query
        name: query
        description: Search query
      - in: query
        name: sort
        description: Return matches sorted by either `score` or `timestamp`
      - in: query
        name: sort_dir
        description: Change sort direction to ascending (`asc`) or descending (`desc`)
      - in: query
        name: token
        description: Authentication token
      responses:
        200:
          description: OK
      tags:
      - Messaging
      - Real Time
  /files.comments.delete:
    post:
      summary: Delete File Comments
      description: Deletes an existing comment on a file.
      operationId: files_comments_delete
      x-api-path-slug: files-comments-delete-post
      parameters:
      - in: formData
        name: file
        description: File to delete a comment from
      - in: formData
        name: id
        description: The comment to delete
      - in: header
        name: token
        description: Authentication token
      responses:
        200:
          description: OK
      tags:
      - Messaging
      - Files
      - Comments
  /auth.revoke:
    get:
      summary: Revoke Auth
      description: Revokes a token.
      operationId: auth_revoke
      x-api-path-slug: auth-revoke-get
      parameters:
      - in: query
        name: test
        description: Setting this parameter to `1` triggers a _testing mode_ where
          the specified token will not actually be revoked
      - in: query
        name: token
        description: Authentication token
      responses:
        200:
          description: OK
      tags:
      - Messaging
      - Authentication
  /reactions.add:
    post:
      summary: Add Reaction
      description: Adds a reaction to an item.
      operationId: reactions_add
      x-api-path-slug: reactions-add-post
      parameters:
      - in: formData
        name: channel
        description: Channel where the message to add reaction to was posted
      - in: formData
        name: file
        description: File to add reaction to
      - in: formData
        name: file_comment
        description: File comment to add reaction to
      - in: formData
        name: name
        description: Reaction (emoji) name
      - in: formData
        name: timestamp
        description: Timestamp of the message to add reaction to
      - in: header
        name: token
        description: Authentication token
      responses:
        200:
          description: OK
      tags:
      - Messaging
      - Reactions
  /stars.add:
    post:
      summary: Star Item
      description: Adds a star to an item.
      operationId: stars_add
      x-api-path-slug: stars-add-post
      parameters:
      - in: formData
        name: channel
        description: Channel to add star to, or channel where the message to add star
          to was posted (used with `timestamp`)
      - in: formData
        name: file
        description: File to add star to
      - in: formData
        name: file_comment
        description: File comment to add star to
      - in: formData
        name: timestamp
        description: Timestamp of the message to add star to
      - in: header
        name: token
        description: Authentication token
      responses:
        200:
          description: OK
      tags:
      - Messaging
      - Stars
  /reminders.complete:
    post:
      summary: Mark Reminders Complete
      description: Marks a reminder as complete.
      operationId: reminders_complete
      x-api-path-slug: reminders-complete-post
      parameters:
      - in: formData
        name: reminder
        description: The ID of the reminder to be marked as complete
      - in: header
        name: token
        description: Authentication token
      responses:
        200:
          description: OK
      tags:
      - Messaging
      - Reminders
x-streamrank:
  polling_total_time_average: 0
  polling_size_download_average: 0
  streaming_total_time_average: 0
  streaming_size_download_average: 0
  change_yes: 0
  change_no: 0
  time_percentage: 0
  size_percentage: 0
  change_percentage: 0
  last_run: ""
  days_run: 0
  minute_run: 0
---