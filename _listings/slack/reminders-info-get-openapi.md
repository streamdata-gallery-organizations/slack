---
swagger: "2.0"
x-collection-name: Slack
x-complete: 0
info:
  title: Slack Get Reminder
  description: Gets information about a reminder.
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
        description: Filter logs generated by this user???s actions
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