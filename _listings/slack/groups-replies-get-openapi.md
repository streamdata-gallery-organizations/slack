---
swagger: "2.0"
x-collection-name: Slack
x-complete: 0
info:
  title: Slack Get Group Thread
  description: Retrieve a thread of messages posted to a private channel
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