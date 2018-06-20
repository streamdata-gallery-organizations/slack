---
swagger: "2.0"
x-collection-name: Slack
x-complete: 0
info:
  title: Slack Delete Message
  description: Deletes a message.
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