---
swagger: "2.0"
x-collection-name: Slack
x-complete: 0
info:
  title: Slack Open Group
  description: Opens a private channel.
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
      x-api-path-slug: chatdelete-post
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
      x-api-path-slug: filescommentsedit-post
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
      x-api-path-slug: imclose-post
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
      x-api-path-slug: groupsreplies-get
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
      x-api-path-slug: botsinfo-get
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
      x-api-path-slug: groupsrename-post
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
      x-api-path-slug: usersprofileset-post
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
      x-api-path-slug: userssetpresence-post
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
      x-api-path-slug: conversationsclose-post
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
      x-api-path-slug: imopen-post
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
      x-api-path-slug: groupslist-get
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
      x-api-path-slug: teamintegrationlogs-get
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
        description: "Filter logs generated by this user\u2019s actions"
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
      x-api-path-slug: groupskick-post
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
      x-api-path-slug: dndinfo-get
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
      x-api-path-slug: channelsarchive-post
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
      x-api-path-slug: remindersinfo-get
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
      x-api-path-slug: channelsinfo-get
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
      x-api-path-slug: channelskick-post
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
      x-api-path-slug: groupsmark-post
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
      x-api-path-slug: mpimclose-post
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
      x-api-path-slug: conversationsjoin-post
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
      x-api-path-slug: channelshistory-get
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
      x-api-path-slug: immark-post
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
      x-api-path-slug: oauthtoken-get
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
      x-api-path-slug: filesupload-post
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
      x-api-path-slug: usergroupsuserslist-get
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
      x-api-path-slug: usersinfo-get
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
      x-api-path-slug: userslookupbyemail-get
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
      x-api-path-slug: reactionslist-get
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
      x-api-path-slug: conversationscreate-post
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
      x-api-path-slug: teambillableinfo-get
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
      x-api-path-slug: dndenddnd-post
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
      x-api-path-slug: searchall-get
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
      x-api-path-slug: filescommentsdelete-post
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
      x-api-path-slug: authrevoke-get
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
      x-api-path-slug: reactionsadd-post
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
      x-api-path-slug: starsadd-post
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
      x-api-path-slug: reminderscomplete-post
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
  /chat.unfurl:
    post:
      summary: Unfurl Message
      description: Provide custom unfurl behavior for user-posted URLs
      operationId: chat_unfurl
      x-api-path-slug: chatunfurl-post
      parameters:
      - in: formData
        name: channel
        description: Channel ID of the message
      - in: header
        name: token
        description: Authentication token
      - in: formData
        name: ts
        description: Timestamp of the message to add unfurl behavior to
      - in: formData
        name: unfurls
        description: URL-encoded JSON map with keys set to URLs featured in the the
          message, pointing to their unfurl message attachments
      - in: formData
        name: user_auth_message
        description: Provide a simply-formatted string to send as an ephemeral message
          to the user as invitation to authenticate further and enable full unfurling
          behavior
      - in: formData
        name: user_auth_required
        description: Set to `true` or `1` to indicate the user must install your Slack
          app to trigger unfurls for this domain
      - in: formData
        name: user_auth_url
        description: Send users to this custom URL where they will complete authentication
          in your app to fully trigger unfurling
      responses:
        200:
          description: OK
      tags:
      - Messages
  /conversations.unarchive:
    post:
      summary: Unarchve Conversation
      description: Reverses conversation archival.
      operationId: conversations_unarchive
      x-api-path-slug: conversationsunarchive-post
      parameters:
      - in: formData
        name: channel
        description: ID of conversation to unarchive
      - in: header
        name: token
        description: Authentication token
      responses:
        200:
          description: OK
      tags:
      - Messaging
      - Conversations
      - Archives
  /groups.info:
    get:
      summary: Get Group
      description: Gets information about a private channel.
      operationId: groups_info
      x-api-path-slug: groupsinfo-get
      parameters:
      - in: query
        name: channel
        description: Private channel to get info on
      - in: query
        name: include_locale
        description: Set this to `true` to receive the locale for this group
      - in: query
        name: token
        description: Authentication token
      responses:
        200:
          description: OK
      tags:
      - Messaging
      - Groups
  /files.revokePublicURL:
    post:
      summary: Revoke Public URL
      description: Revokes public/external sharing access for a file
      operationId: files_revokePublicURL
      x-api-path-slug: filesrevokepublicurl-post
      parameters:
      - in: formData
        name: file
        description: File to revoke
      - in: header
        name: token
        description: Authentication token
      responses:
        200:
          description: OK
      tags:
      - Messaging
      - Files
  /conversations.list:
    get:
      summary: List Conversations
      description: Lists all channels in a Slack team.
      operationId: conversations_list
      x-api-path-slug: conversationslist-get
      parameters:
      - in: query
        name: cursor
        description: Paginate through collections of data by setting the `cursor`
          parameter to a `next_cursor` attribute returned by a previous requests `response_metadata`
      - in: query
        name: exclude_archived
        description: Set to `true` to exclude archived channels from the list
      - in: query
        name: limit
        description: The maximum number of items to return
      - in: query
        name: token
        description: Authentication token
      - in: query
        name: types
        description: Mix and match channel types by providing a comma-separated list
          of any combination of `public_channel`, `private_channel`, `mpim`, `im`
      responses:
        200:
          description: OK
      tags:
      - Messaging
      - Conversations
  /stars.list:
    get:
      summary: List Stars
      description: Lists stars for a user.
      operationId: stars_list
      x-api-path-slug: starslist-get
      parameters:
      - in: query
        name: count
      - in: query
        name: page
      - in: query
        name: token
        description: Authentication token
      responses:
        200:
          description: OK
      tags:
      - Messaging
      - Stars
  /reactions.get:
    get:
      summary: Get Reaction
      description: Gets reactions for an item.
      operationId: reactions_get
      x-api-path-slug: reactionsget-get
      parameters:
      - in: query
        name: channel
        description: Channel where the message to get reactions for was posted
      - in: query
        name: file
        description: File to get reactions for
      - in: query
        name: file_comment
        description: File comment to get reactions for
      - in: query
        name: full
        description: If true always return the complete reaction list
      - in: query
        name: timestamp
        description: Timestamp of the message to get reactions for
      - in: query
        name: token
        description: Authentication token
      responses:
        200:
          description: OK
      tags:
      - Messaging
      - Reactions
  /im.history:
    get:
      summary: Get Messages History
      description: Fetches history of messages and events from direct message channel.
      operationId: im_history
      x-api-path-slug: imhistory-get
      parameters:
      - in: query
        name: channel
        description: Direct message channel to fetch history for
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
  /pins.add:
    post:
      summary: Pin Item
      description: Pins an item to a channel.
      operationId: pins_add
      x-api-path-slug: pinsadd-post
      parameters:
      - in: formData
        name: channel
        description: Channel to pin the item in
      - in: formData
        name: file
        description: File to pin
      - in: formData
        name: file_comment
        description: File comment to pin
      - in: formData
        name: timestamp
        description: Timestamp of the message to pin
      - in: header
        name: token
        description: Authentication token
      responses:
        200:
          description: OK
      tags:
      - Messaging
      - Pins
  /channels.leave:
    post:
      summary: Leave Channel
      description: Leaves a channel.
      operationId: channels_leave
      x-api-path-slug: channelsleave-post
      parameters:
      - in: formData
        name: channel
        description: Channel to leave
      - in: header
        name: token
        description: Authentication token
      responses:
        200:
          description: OK
      tags:
      - Messaging
      - Channels
  /chat.getPermalink:
    get:
      summary: Get Permalink
      description: Retrieve a permalink URL for a specific extant message
      operationId: chat_getPermalink
      x-api-path-slug: chatgetpermalink-get
      parameters:
      - in: query
        name: channel
        description: The ID of the conversation or channel containing the message
      - in: query
        name: message_ts
        description: A messages `ts` value, uniquely identifying it within a channel
      - in: query
        name: token
        description: Authentication token
      responses:
        200:
          description: OK
      tags:
      - Messages
  /channels.rename:
    post:
      summary: Rename Channel
      description: Renames a channel.
      operationId: channels_rename
      x-api-path-slug: channelsrename-post
      parameters:
      - in: formData
        name: channel
        description: Channel to rename
      - in: formData
        name: name
        description: New name for channel
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
      - Channels
  /files.list:
    get:
      summary: List Files
      description: Lists & filters team files.
      operationId: files_list
      x-api-path-slug: fileslist-get
      parameters:
      - in: query
        name: channel
        description: Filter files appearing in a specific channel, indicated by its
          ID
      - in: query
        name: count
      - in: query
        name: page
      - in: query
        name: token
        description: Authentication token
      - in: query
        name: ts_from
        description: Filter files created after this timestamp (inclusive)
      - in: query
        name: ts_to
        description: Filter files created before this timestamp (inclusive)
      - in: query
        name: types
        description: Filter files by type:* `all` - All files* `spaces` - Posts* `snippets`
          - Snippets* `images` - Image files* `gdocs` - Google docs* `zips` - Zip
          files* `pdfs` - PDF filesYou can pass multiple values in the types argument,
          like `types=spaces,snippets`
      - in: query
        name: user
        description: Filter files created by a single user
      responses:
        200:
          description: OK
      tags:
      - Messaging
      - Files
  /mpim.mark:
    post:
      summary: Mark Multiparty Direct Messages
      description: Sets the read cursor in a multiparty direct message channel.
      operationId: mpim_mark
      x-api-path-slug: mpimmark-post
      parameters:
      - in: formData
        name: channel
        description: multiparty direct message channel to set reading cursor in
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
  /usergroups.users.update:
    post:
      summary: Update Group Users
      description: Update the list of users for a User Group
      operationId: usergroups_users_update
      x-api-path-slug: usergroupsusersupdate-post
      parameters:
      - in: formData
        name: include_count
        description: Include the number of users in the User Group
      - in: header
        name: token
        description: Authentication token
      - in: formData
        name: usergroup
        description: The encoded ID of the User Group to update
      - in: formData
        name: users
        description: A comma separated string of encoded user IDs that represent the
          entire list of users for the User Group
      responses:
        200:
          description: OK
      tags:
      - Messaging
      - Groups
  /conversations.setTopic:
    post:
      summary: Set Conversation Topic
      description: Sets the topic for a conversation.
      operationId: conversations_setTopic
      x-api-path-slug: conversationssettopic-post
      parameters:
      - in: formData
        name: channel
        description: Conversation to set the topic of
      - in: header
        name: token
        description: Authentication token
      - in: formData
        name: topic
        description: The new topic string
      responses:
        200:
          description: OK
      tags:
      - Messaging
      - Conversations
  /conversations.members:
    get:
      summary: Get Conversation Members
      description: Retrieve members of a conversation.
      operationId: conversations_members
      x-api-path-slug: conversationsmembers-get
      parameters:
      - in: query
        name: channel
        description: ID of the conversation to retrieve members for
      - in: query
        name: cursor
        description: Paginate through collections of data by setting the `cursor`
          parameter to a `next_cursor` attribute returned by a previous requests `response_metadata`
      - in: query
        name: limit
        description: The maximum number of items to return
      - in: query
        name: token
        description: Authentication token
      responses:
        200:
          description: OK
      tags:
      - Messaging
      - Conversations
  /conversations.open:
    post:
      summary: Open Conversation
      description: Opens or resumes a direct message or multi-person direct message.
      operationId: conversations_open
      x-api-path-slug: conversationsopen-post
      parameters:
      - in: formData
        name: channel
        description: Resume a conversation by supplying an `im` or `mpim`s ID
      - in: formData
        name: return_im
        description: Boolean, indicates you want the full IM channel definition in
          the response
      - in: header
        name: token
        description: Authentication token
      - in: formData
        name: users
        description: Comma separated lists of users
      responses:
        200:
          description: OK
      tags:
      - Messaging
      - Conversations
  /pins.remove:
    post:
      summary: Unpin Item
      description: Un-pins an item from a channel.
      operationId: pins_remove
      x-api-path-slug: pinsremove-post
      parameters:
      - in: formData
        name: channel
        description: Channel where the item is pinned to
      - in: formData
        name: file
        description: File to un-pin
      - in: formData
        name: file_comment
        description: File comment to un-pin
      - in: formData
        name: timestamp
        description: Timestamp of the message to un-pin
      - in: header
        name: token
        description: Authentication token
      responses:
        200:
          description: OK
      tags:
      - Messaging
      - Pins
  /files.delete:
    post:
      summary: Delete File
      description: Deletes a file.
      operationId: files_delete
      x-api-path-slug: filesdelete-post
      parameters:
      - in: formData
        name: file
        description: ID of file to delete
      - in: header
        name: token
        description: Authentication token
      responses:
        200:
          description: OK
      tags:
      - Messaging
      - Files
  /pins.list:
    get:
      summary: List Pins
      description: Lists items pinned to a channel.
      operationId: pins_list
      x-api-path-slug: pinslist-get
      parameters:
      - in: query
        name: channel
        description: Channel to get pinned items for
      - in: query
        name: token
        description: Authentication token
      responses:
        200:
          description: OK
      tags:
      - Messaging
      - Pins
  /api.test:
    get:
      summary: Test API
      description: Checks API calling code.
      operationId: api_test
      x-api-path-slug: apitest-get
      parameters:
      - in: query
        name: error
        description: Error response to return
      - in: query
        name: foo
        description: example property to return
      responses:
        200:
          description: OK
      tags:
      - Messaging
  /reminders.list:
    get:
      summary: List Reminders
      description: Lists all reminders created by or for a given user.
      operationId: reminders_list
      x-api-path-slug: reminderslist-get
      parameters:
      - in: query
        name: token
        description: Authentication token
      responses:
        200:
          description: OK
      tags:
      - Messaging
      - Reminders
  /users.getPresence:
    get:
      summary: Get Presence
      description: Gets user presence information.
      operationId: users_getPresence
      x-api-path-slug: usersgetpresence-get
      parameters:
      - in: query
        name: token
        description: Authentication token
      - in: query
        name: user
        description: User to get presence info on
      responses:
        200:
          description: OK
      tags:
      - Messaging
      - Presence
  /usergroups.update:
    post:
      summary: Update Group
      description: Update an existing User Group
      operationId: usergroups_update
      x-api-path-slug: usergroupsupdate-post
      parameters:
      - in: formData
        name: channels
        description: A comma separated string of encoded channel IDs for which the
          User Group uses as a default
      - in: formData
        name: description
        description: A short description of the User Group
      - in: formData
        name: handle
        description: A mention handle
      - in: formData
        name: include_count
        description: Include the number of users in the User Group
      - in: formData
        name: name
        description: A name for the User Group
      - in: header
        name: token
        description: Authentication token
      - in: formData
        name: usergroup
        description: The encoded ID of the User Group to update
      responses:
        200:
          description: OK
      tags:
      - Messaging
      - Groups
  /conversations.leave:
    post:
      summary: Leave Conversation
      description: Leaves a conversation.
      operationId: conversations_leave
      x-api-path-slug: conversationsleave-post
      parameters:
      - in: formData
        name: channel
        description: Conversation to leave
      - in: header
        name: token
        description: Authentication token
      responses:
        200:
          description: OK
      tags:
      - Messaging
      - Conversations
  /files.info:
    get:
      summary: Get File
      description: Gets information about a team file.
      operationId: files_info
      x-api-path-slug: filesinfo-get
      parameters:
      - in: query
        name: count
      - in: query
        name: file
        description: Specify a file by providing its ID
      - in: query
        name: page
      - in: query
        name: token
        description: Authentication token
      responses:
        200:
          description: OK
      tags:
      - Messaging
      - Files
  /groups.leave:
    post:
      summary: Leave Group
      description: Leaves a private channel.
      operationId: groups_leave
      x-api-path-slug: groupsleave-post
      parameters:
      - in: formData
        name: channel
        description: Private channel to leave
      - in: header
        name: token
        description: Authentication token
      responses:
        200:
          description: OK
      tags:
      - Messaging
      - Groups
  /apps.permissions.info:
    get:
      summary: App Permissions
      description: Returns list of permissions this app has on a team.
      operationId: apps_permissions_info
      x-api-path-slug: appspermissionsinfo-get
      parameters:
      - in: query
        name: token
        description: Authentication token
      responses:
        200:
          description: OK
      tags:
      - Messaging
      - Permissions
  /usergroups.create:
    post:
      summary: Create Group
      description: Create a User Group
      operationId: usergroups_create
      x-api-path-slug: usergroupscreate-post
      parameters:
      - in: formData
        name: channels
        description: A comma separated string of encoded channel IDs for which the
          User Group uses as a default
      - in: formData
        name: description
        description: A short description of the User Group
      - in: formData
        name: handle
        description: A mention handle
      - in: formData
        name: include_count
        description: Include the number of users in each User Group
      - in: formData
        name: name
        description: A name for the User Group
      - in: header
        name: token
        description: Authentication token
      responses:
        200:
          description: OK
      tags:
      - Messaging
      - Groups
  /groups.createChild:
    post:
      summary: Create Child Group
      description: Clones and archives a private channel.
      operationId: groups_createChild
      x-api-path-slug: groupscreatechild-post
      parameters:
      - in: formData
        name: channel
        description: Private channel to clone and archive
      - in: formData
        name: token
        description: Authentication token
      responses:
        200:
          description: OK
      tags:
      - Messaging
      - Groups
      - archives
  /channels.mark:
    post:
      summary: Mark Channel
      description: Sets the read cursor in a channel.
      operationId: channels_mark
      x-api-path-slug: channelsmark-post
      parameters:
      - in: formData
        name: channel
        description: Channel to set reading cursor in
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
      - Channels
  /users.deletePhoto:
    post:
      summary: Delete Photo
      description: Delete the user profile photo
      operationId: users_deletePhoto
      x-api-path-slug: usersdeletephoto-post
      parameters:
      - in: formData
        name: token
        description: Authentication token
      responses:
        200:
          description: OK
      tags:
      - Messaging
      - Photos
  /users.setPhoto:
    post:
      summary: Set User Profile Photo
      description: Set the user profile photo
      operationId: users_setPhoto
      x-api-path-slug: userssetphoto-post
      parameters:
      - in: formData
        name: crop_w
        description: Width/height of crop box (always square)
      - in: formData
        name: crop_x
        description: X coordinate of top-left corner of crop box
      - in: formData
        name: crop_y
        description: Y coordinate of top-left corner of crop box
      - in: formData
        name: image
        description: File contents via `multipart/form-data`
      - in: formData
        name: token
        description: Authentication token
      responses:
        200:
          description: OK
      tags:
      - Messaging
      - Users
  /files.sharedPublicURL:
    post:
      summary: Share Public URL
      description: Enables a file for public/external sharing.
      operationId: files_sharedPublicURL
      x-api-path-slug: filessharedpublicurl-post
      parameters:
      - in: formData
        name: file
        description: File to share
      - in: header
        name: token
        description: Authentication token
      responses:
        200:
          description: OK
      tags:
      - Messaging
      - Files
  /conversations.kick:
    post:
      summary: Remove User From Conversation
      description: Removes a user from a conversation.
      operationId: conversations_kick
      x-api-path-slug: conversationskick-post
      parameters:
      - in: formData
        name: channel
        description: ID of conversation to remove user from
      - in: header
        name: token
        description: Authentication token
      - in: formData
        name: user
        description: User ID to be removed
      responses:
        200:
          description: OK
      tags:
      - Messaging
      - Conversations
  /chat.postEphemeral:
    post:
      summary: Sent Ephemeral lMessage
      description: Sends an ephemeral message to a user in a channel.
      operationId: chat_postEphemeral
      x-api-path-slug: chatpostephemeral-post
      parameters:
      - in: formData
        name: as_user
        description: Pass true to post the message as the authed bot
      - in: formData
        name: attachments
        description: A JSON-based array of structured attachments, presented as a
          URL-encoded string
      - in: formData
        name: channel
        description: Channel, private group, or IM channel to send message to
      - in: formData
        name: link_names
        description: Find and link channel names and usernames
      - in: formData
        name: parse
        description: Change how messages are treated
      - in: formData
        name: text
        description: Text of the message to send
      - in: header
        name: token
        description: Authentication token
      - in: formData
        name: user
        description: '`id` of the user who will receive the ephemeral message'
      responses:
        200:
          description: OK
      tags:
      - Messages
  /conversations.rename:
    post:
      summary: Rename Conversation
      description: Renames a conversation.
      operationId: conversations_rename
      x-api-path-slug: conversationsrename-post
      parameters:
      - in: formData
        name: channel
        description: ID of conversation to rename
      - in: formData
        name: name
        description: New name for conversation
      - in: header
        name: token
        description: Authentication token
      responses:
        200:
          description: OK
      tags:
      - Messaging
      - Conversations
  /migration.exchange:
    get:
      summary: Migration Exchange
      description: For Enterprise Grid workspaces, map local user IDs to global user
        IDs
      operationId: migration_exchange
      x-api-path-slug: migrationexchange-get
      parameters:
      - in: query
        name: token
        description: Authentication token
      - in: query
        name: to_old
        description: Specify `true` to convert `W` global user IDs to workspace-specific
          `U` IDs
      - in: query
        name: users
        description: A comma-separated list of user ids, up to 400 per request
      responses:
        200:
          description: OK
      tags:
      - Messaging
  /usergroups.enable:
    post:
      summary: Enable Group
      description: Enable a User Group
      operationId: usergroups_enable
      x-api-path-slug: usergroupsenable-post
      parameters:
      - in: formData
        name: include_count
        description: Include the number of users in the User Group
      - in: header
        name: token
        description: Authentication token
      - in: formData
        name: usergroup
        description: The encoded ID of the User Group to enable
      responses:
        200:
          description: OK
      tags:
      - Messaging
      - Groups
  /dnd.setSnooze:
    post:
      summary: End Do Not Disturb Snooze
      description: Turns on Do Not Disturb mode for the current user, or changes its
        duration.
      operationId: dnd_setSnooze
      x-api-path-slug: dndsetsnooze-post
      parameters:
      - in: formData
        name: num_minutes
        description: Number of minutes, from now, to snooze until
      - in: formData
        name: token
        description: Authentication token
      responses:
        200:
          description: OK
      tags:
      - Messaging
      - Do Not Disturb
  /chat.update:
    post:
      summary: Update Message
      description: Updates a message.
      operationId: chat_update
      x-api-path-slug: chatupdate-post
      parameters:
      - in: formData
        name: as_user
        description: Pass true to update the message as the authed user
      - in: formData
        name: attachments
        description: A JSON-based array of structured attachments, presented as a
          URL-encoded string
      - in: formData
        name: channel
        description: Channel containing the message to be updated
      - in: formData
        name: link_names
        description: Find and link channel names and usernames
      - in: formData
        name: parse
        description: Change how messages are treated
      - in: formData
        name: text
        description: New text for the message, using the [default formatting rules](/docs/formatting)
      - in: header
        name: token
        description: Authentication token
      - in: formData
        name: ts
        description: Timestamp of the message to be updated
      responses:
        200:
          description: OK
      tags:
      - Messages
  /mpim.history:
    get:
      summary: Get Multiparty Direct Message History
      description: Fetches history of messages and events from a multiparty direct
        message.
      operationId: mpim_history
      x-api-path-slug: mpimhistory-get
      parameters:
      - in: query
        name: channel
        description: Multiparty direct message to fetch history for
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
  /apps.permissions.request:
    get:
      summary: Request App Permissions
      description: Allows an app to request additional scopes
      operationId: apps_permissions_request
      x-api-path-slug: appspermissionsrequest-get
      parameters:
      - in: query
        name: scopes
        description: A comma separated list of scopes to request for
      - in: query
        name: token
        description: Authentication token
      - in: query
        name: trigger_id
        description: Token used to trigger the permissions API
      responses:
        200:
          description: OK
      tags:
      - Messaging
      - Permissions
  /search.files:
    get:
      summary: Start Real Time Messaging Files
      description: Searches for files matching a query.
      operationId: search_files
      x-api-path-slug: searchfiles-get
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
  /users.identity:
    get:
      summary: Get User Identity
      description: Get a user's identity.
      operationId: users_identity
      x-api-path-slug: usersidentity-get
      parameters:
      - in: query
        name: token
        description: Authentication token
      responses:
        200:
          description: OK
      tags:
      - Messaging
      - Users
  /team.accessLogs:
    get:
      summary: Get Logs
      description: Gets the access logs for the current team.
      operationId: team_accessLogs
      x-api-path-slug: teamaccesslogs-get
      parameters:
      - in: query
        name: before
        description: End of time range of logs to include in results (inclusive)
      - in: query
        name: count
      - in: query
        name: page
      - in: query
        name: token
        description: Authentication token
      responses:
        200:
          description: OK
      tags:
      - Messaging
      - Logs
  /groups.invite:
    post:
      summary: Invite User To Group
      description: Invites a user to a private channel.
      operationId: groups_invite
      x-api-path-slug: groupsinvite-post
      parameters:
      - in: formData
        name: channel
        description: Private channel to invite user to
      - in: header
        name: token
        description: Authentication token
      - in: formData
        name: user
        description: User to invite
      responses:
        200:
          description: OK
      tags:
      - Messaging
      - Groups
  /channels.unarchive:
    post:
      summary: Unarchive Channel
      description: Unarchives a channel.
      operationId: channels_unarchive
      x-api-path-slug: channelsunarchive-post
      parameters:
      - in: formData
        name: channel
        description: Channel to unarchive
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
  /rtm.connect:
    get:
      summary: Connect Real Time Messaging
      description: Starts a Real Time Messaging session.
      operationId: rtm_connect
      x-api-path-slug: rtmconnect-get
      parameters:
      - in: query
        name: batch_presence_aware
        description: Only deliver presence events when requested by subscription
      - in: query
        name: token
        description: Authentication token
      responses:
        200:
          description: OK
      tags:
      - Messaging
      - Real Time
  /team.info:
    get:
      summary: Get Team
      description: Gets information about the current team.
      operationId: team_info
      x-api-path-slug: teaminfo-get
      parameters:
      - in: query
        name: token
        description: Authentication token
      responses:
        200:
          description: OK
      tags:
      - Messaging
      - Teams
  /conversations.history:
    get:
      summary: Get Conversation History
      description: Fetches a conversation's history of messages and events.
      operationId: conversations_history
      x-api-path-slug: conversationshistory-get
      parameters:
      - in: query
        name: channel
        description: Conversation ID to fetch history for
      - in: query
        name: cursor
        description: Paginate through collections of data by setting the `cursor`
          parameter to a `next_cursor` attribute returned by a previous requests `response_metadata`
      - in: query
        name: inclusive
        description: Include messages with latest or oldest timestamp in results only
          when either timestamp is specified
      - in: query
        name: latest
        description: End of time range of messages to include in results
      - in: query
        name: limit
        description: The maximum number of items to return
      - in: query
        name: oldest
        description: Start of time range of messages to include in results
      - in: query
        name: token
        description: Authentication token
      responses:
        200:
          description: OK
      tags:
      - Messaging
      - Conversations
  /channels.create:
    post:
      summary: Create Channel
      description: Creates a channel.
      operationId: channels_create
      x-api-path-slug: channelscreate-post
      parameters:
      - in: formData
        name: name
        description: Name of channel to create
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
      - Channels
  /im.replies:
    get:
      summary: Reply to Messages
      description: Retrieve a thread of messages posted to a direct message conversation
      operationId: im_replies
      x-api-path-slug: imreplies-get
      parameters:
      - in: query
        name: channel
        description: Direct message channel to fetch thread from
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
  /groups.create:
    post:
      summary: Create Group
      description: Creates a private channel.
      operationId: groups_create
      x-api-path-slug: groupscreate-post
      parameters:
      - in: formData
        name: name
        description: Name of private channel to create
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
  /reminders.add:
    post:
      summary: Add Reminders
      description: Creates a reminder.
      operationId: reminders_add
      x-api-path-slug: remindersadd-post
      parameters:
      - in: formData
        name: text
        description: The content of the reminder
      - in: formData
        name: time
        description: 'When this reminder should happen: the Unix timestamp (up to
          five years from now), the number of seconds until the reminder (if within
          24 hours), or a natural language description (Ex'
      - in: header
        name: token
        description: Authentication token
      - in: formData
        name: user
        description: The user who will receive the reminder
      responses:
        200:
          description: OK
      tags:
      - Messaging
      - Reminders
  /conversations.setPurpose:
    post:
      summary: Set Conversation Purpose
      description: Sets the purpose for a conversation.
      operationId: conversations_setPurpose
      x-api-path-slug: conversationssetpurpose-post
      parameters:
      - in: formData
        name: channel
        description: Conversation to set the purpose of
      - in: formData
        name: purpose
        description: A new, specialer purpose
      - in: header
        name: token
        description: Authentication token
      responses:
        200:
          description: OK
      tags:
      - Messaging
      - Conversations
  /channels.join:
    post:
      summary: Join Channel
      description: Joins a channel, creating it if needed.
      operationId: channels_join
      x-api-path-slug: channelsjoin-post
      parameters:
      - in: formData
        name: name
        description: Name of channel to join
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
      - Channels
  /usergroups.list:
    get:
      summary: List Groups
      description: List all User Groups for a team
      operationId: usergroups_list
      x-api-path-slug: usergroupslist-get
      parameters:
      - in: query
        name: include_count
        description: Include the number of users in each User Group
      - in: query
        name: include_disabled
        description: Include disabled User Groups
      - in: query
        name: include_users
        description: Include the list of users for each User Group
      - in: query
        name: token
        description: Authentication token
      responses:
        200:
          description: OK
      tags:
      - Messaging
      - Groups
  /users.profile.get:
    get:
      summary: Get User Profile
      description: Retrieves a user's profile information.
      operationId: users_profile_get
      x-api-path-slug: usersprofileget-get
      parameters:
      - in: query
        name: include_labels
        description: Include labels for each ID in custom profile fields
      - in: query
        name: token
        description: Authentication token
      - in: query
        name: user
        description: User to retrieve profile info for
      responses:
        200:
          description: OK
      tags:
      - Messaging
      - Users
  /groups.open:
    post:
      summary: Open Group
      description: Opens a private channel.
      operationId: groups_open
      x-api-path-slug: groupsopen-post
      parameters:
      - in: formData
        name: channel
        description: Private channel to open
      - in: header
        name: token
        description: Authentication token
      responses:
        200:
          description: OK
      tags:
      - Messaging
      - Groups
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