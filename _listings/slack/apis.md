---
name: Slack
x-slug: slack
description: Slack is a team communication application providing services such as
  real-time messaging, archiving, and to search for modern teams. It offers one-on-one
  messaging, private groups, persistent chat rooms, and direct messaging as well as
  group chats organized by topic. All content inside Slack is searchable from one
  search box and it integrates with a number of third-party services, including Google
  Docs, Dropbox, Heroku, Crashlytics, GitHub, and Zendesk.
image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/slack-logo.png
x-kinRank: "9"
x-alexaRank: ""
tags: Slack
created: "2018-05-22"
modified: "2018-05-22"
url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/apis.md
specificationVersion: "0.14"
apis:
- name: Slack Delete Message
  x-api-slug: slack
  description: Deletes a message.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/slack-logo.png
  humanURL: https://slack.com
  baseURL: https://slack.com//api//chat.delete
  tags: Messages
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/chatdelete-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/chatdelete-post-openapi.md
- name: Slack Edit File Comments
  x-api-slug: slack
  description: Edit an existing file comment.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/slack-logo.png
  humanURL: https://slack.com
  baseURL: https://slack.com//api//files.comments.edit
  tags: Messaging,Files,Comments
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/filescommentsedit-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/filescommentsedit-post-openapi.md
- name: Slack Close Group
  x-api-slug: slack
  description: Close a direct message channel.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/slack-logo.png
  humanURL: https://slack.com
  baseURL: https://slack.com//api//im.close
  tags: Messaging
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/imclose-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/imclose-post-openapi.md
- name: Slack Get Group Thread
  x-api-slug: slack
  description: Retrieve a thread of messages posted to a private channel
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/slack-logo.png
  humanURL: https://slack.com
  baseURL: https://slack.com//api//groups.replies
  tags: Messaging,Groups
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/groupsreplies-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/groupsreplies-get-openapi.md
- name: Slack Get Bot Info
  x-api-slug: slack
  description: Gets information about a bot user.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/slack-logo.png
  humanURL: https://slack.com
  baseURL: https://slack.com//api//bots.info
  tags: Messaging,Bots
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/botsinfo-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/botsinfo-get-openapi.md
- name: Slack Rename Group
  x-api-slug: slack
  description: Renames a private channel.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/slack-logo.png
  humanURL: https://slack.com
  baseURL: https://slack.com//api//groups.rename
  tags: Messaging,Groups
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/groupsrename-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/groupsrename-post-openapi.md
- name: Slack Set User Profile
  x-api-slug: slack
  description: Set the profile information for a user.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/slack-logo.png
  humanURL: https://slack.com
  baseURL: https://slack.com//api//users.profile.set
  tags: Messaging,Users
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/usersprofileset-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/usersprofileset-post-openapi.md
- name: Slack Set User Presence
  x-api-slug: slack
  description: Manually sets user presence.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/slack-logo.png
  humanURL: https://slack.com
  baseURL: https://slack.com//api//users.setPresence
  tags: Messaging,Users
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/userssetpresence-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/userssetpresence-post-openapi.md
- name: Slack Close Conversation
  x-api-slug: slack
  description: Closes a direct message or multi-person direct message.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/slack-logo.png
  humanURL: https://slack.com
  baseURL: https://slack.com//api//conversations.close
  tags: Messaging,Conversations
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/conversationsclose-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/conversationsclose-post-openapi.md
- name: Slack Open Messages
  x-api-slug: slack
  description: Opens a direct message channel.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/slack-logo.png
  humanURL: https://slack.com
  baseURL: https://slack.com//api//im.open
  tags: Messaging
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/imopen-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/imopen-post-openapi.md
- name: Slack Get Group
  x-api-slug: slack
  description: Lists private channels that the calling user has access to.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/slack-logo.png
  humanURL: https://slack.com
  baseURL: https://slack.com//api//groups.list
  tags: Messaging,Groups
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/groupslist-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/groupslist-get-openapi.md
- name: Slack Get Team Logs
  x-api-slug: slack
  description: Gets the integration logs for the current team.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/slack-logo.png
  humanURL: https://slack.com
  baseURL: https://slack.com//api//team.integrationLogs
  tags: Messaging,Teams
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/teamintegrationlogs-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/teamintegrationlogs-get-openapi.md
- name: Slack Remove User From Group
  x-api-slug: slack
  description: Removes a user from a private channel.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/slack-logo.png
  humanURL: https://slack.com
  baseURL: https://slack.com//api//groups.kick
  tags: Messaging,Groups
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/groupskick-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/groupskick-post-openapi.md
- name: Slack Get Do Not Disturb
  x-api-slug: slack
  description: Retrieves a user's current Do Not Disturb status.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/slack-logo.png
  humanURL: https://slack.com
  baseURL: https://slack.com//api//dnd.info
  tags: Messaging,Do Not Disturb
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/dndinfo-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/dndinfo-get-openapi.md
- name: Slack Archive Channel
  x-api-slug: slack
  description: Archives a channel.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/slack-logo.png
  humanURL: https://slack.com
  baseURL: https://slack.com//api//channels.archive
  tags: Messaging,Channels, Archives
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/channelsarchive-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/channelsarchive-post-openapi.md
- name: Slack Get Reminder
  x-api-slug: slack
  description: Gets information about a reminder.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/slack-logo.png
  humanURL: https://slack.com
  baseURL: https://slack.com//api//reminders.info
  tags: Messaging,Reminders
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/remindersinfo-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/remindersinfo-get-openapi.md
- name: Slack Get Channel
  x-api-slug: slack
  description: Gets information about a channel.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/slack-logo.png
  humanURL: https://slack.com
  baseURL: https://slack.com//api//channels.info
  tags: Messaging,Channels
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/channelsinfo-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/channelsinfo-get-openapi.md
- name: Slack Remove User From Channel
  x-api-slug: slack
  description: Removes a user from a channel.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/slack-logo.png
  humanURL: https://slack.com
  baseURL: https://slack.com//api//channels.kick
  tags: Messaging,Channels
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/channelskick-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/channelskick-post-openapi.md
- name: Slack Mark Group
  x-api-slug: slack
  description: Sets the read cursor in a private channel.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/slack-logo.png
  humanURL: https://slack.com
  baseURL: https://slack.com//api//groups.mark
  tags: Messaging,Groups
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/groupsmark-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/groupsmark-post-openapi.md
- name: Slack Close Multiparty Direct Message
  x-api-slug: slack
  description: Closes a multiparty direct message channel.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/slack-logo.png
  humanURL: https://slack.com
  baseURL: https://slack.com//api//mpim.close
  tags: Messaging
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/mpimclose-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/mpimclose-post-openapi.md
- name: Slack Join Conversation
  x-api-slug: slack
  description: Joins an existing conversation.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/slack-logo.png
  humanURL: https://slack.com
  baseURL: https://slack.com//api//conversations.join
  tags: Messaging,Conversations
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/conversationsjoin-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/conversationsjoin-post-openapi.md
- name: Slack Get Channel History
  x-api-slug: slack
  description: Fetches history of messages and events from a channel.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/slack-logo.png
  humanURL: https://slack.com
  baseURL: https://slack.com//api//channels.history
  tags: Messaging,Channels
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/channelshistory-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/channelshistory-get-openapi.md
- name: Slack Mark Messages
  x-api-slug: slack
  description: Sets the read cursor in a direct message channel.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/slack-logo.png
  humanURL: https://slack.com
  baseURL: https://slack.com//api//im.mark
  tags: Messaging
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/immark-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/immark-post-openapi.md
- name: Slack Oauth Token
  x-api-slug: slack
  description: Exchanges a temporary OAuth verifier code for a workspace token.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/slack-logo.png
  humanURL: https://slack.com
  baseURL: https://slack.com//api//oauth.token
  tags: Messaging,OAuth
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/oauthtoken-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/oauthtoken-get-openapi.md
- name: Slack Upload File
  x-api-slug: slack
  description: Uploads or creates a file.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/slack-logo.png
  humanURL: https://slack.com
  baseURL: https://slack.com//api//files.upload
  tags: Messaging,Files
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/filesupload-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/filesupload-post-openapi.md
- name: Slack List Group Users
  x-api-slug: slack
  description: List all users in a User Group
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/slack-logo.png
  humanURL: https://slack.com
  baseURL: https://slack.com//api//usergroups.users.list
  tags: Messaging,Groups
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/usergroupsuserslist-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/usergroupsuserslist-get-openapi.md
- name: Slack Get User Info
  x-api-slug: slack
  description: Gets information about a user.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/slack-logo.png
  humanURL: https://slack.com
  baseURL: https://slack.com//api//users.info
  tags: Messaging,Users
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/usersinfo-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/usersinfo-get-openapi.md
- name: Slack Find User
  x-api-slug: slack
  description: Find a user with an email address.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/slack-logo.png
  humanURL: https://slack.com
  baseURL: https://slack.com//api//users.lookupByEmail
  tags: Messaging,Users
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/userslookupbyemail-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/userslookupbyemail-get-openapi.md
- name: Slack List Reactions
  x-api-slug: slack
  description: Lists reactions made by a user.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/slack-logo.png
  humanURL: https://slack.com
  baseURL: https://slack.com//api//reactions.list
  tags: Messaging,Reactions
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/reactionslist-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/reactionslist-get-openapi.md
- name: Slack Create Conversation
  x-api-slug: slack
  description: Initiates a public or private channel-based conversation
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/slack-logo.png
  humanURL: https://slack.com
  baseURL: https://slack.com//api//conversations.create
  tags: Messaging,Conversations
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/conversationscreate-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/conversationscreate-post-openapi.md
- name: Slack Get Billable Info
  x-api-slug: slack
  description: Gets billable users information for the current team.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/slack-logo.png
  humanURL: https://slack.com
  baseURL: https://slack.com//api//team.billableInfo
  tags: Messaging,Billing
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/teambillableinfo-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/teambillableinfo-get-openapi.md
- name: Slack End Do Not Disturb
  x-api-slug: slack
  description: Ends the current user's Do Not Disturb session immediately.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/slack-logo.png
  humanURL: https://slack.com
  baseURL: https://slack.com//api//dnd.endDnd
  tags: Messaging,Do Not Disturb
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/dndenddnd-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/dndenddnd-post-openapi.md
- name: Slack Search Real Time Messaging
  x-api-slug: slack
  description: Searches for messages and files matching a query.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/slack-logo.png
  humanURL: https://slack.com
  baseURL: https://slack.com//api//search.all
  tags: Messaging,Real Time
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/searchall-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/searchall-get-openapi.md
- name: Slack Delete File Comments
  x-api-slug: slack
  description: Deletes an existing comment on a file.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/slack-logo.png
  humanURL: https://slack.com
  baseURL: https://slack.com//api//files.comments.delete
  tags: Messaging,Files,Comments
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/filescommentsdelete-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/filescommentsdelete-post-openapi.md
- name: Slack Revoke Auth
  x-api-slug: slack
  description: Revokes a token.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/slack-logo.png
  humanURL: https://slack.com
  baseURL: https://slack.com//api//auth.revoke
  tags: Messaging,Authentication
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/authrevoke-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/authrevoke-get-openapi.md
- name: Slack Add Reaction
  x-api-slug: slack
  description: Adds a reaction to an item.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/slack-logo.png
  humanURL: https://slack.com
  baseURL: https://slack.com//api//reactions.add
  tags: Messaging,Reactions
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/reactionsadd-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/reactionsadd-post-openapi.md
- name: Slack Star Item
  x-api-slug: slack
  description: Adds a star to an item.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/slack-logo.png
  humanURL: https://slack.com
  baseURL: https://slack.com//api//stars.add
  tags: Messaging,Stars
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/starsadd-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/starsadd-post-openapi.md
- name: Slack Mark Reminders Complete
  x-api-slug: slack
  description: Marks a reminder as complete.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/slack-logo.png
  humanURL: https://slack.com
  baseURL: https://slack.com//api//reminders.complete
  tags: Messaging,Reminders
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/reminderscomplete-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/reminderscomplete-post-openapi.md
- name: Slack Unfurl Message
  x-api-slug: slack
  description: Provide custom unfurl behavior for user-posted URLs
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/slack-logo.png
  humanURL: https://slack.com
  baseURL: https://slack.com//api//chat.unfurl
  tags: Messages
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/chatunfurl-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/chatunfurl-post-openapi.md
- name: Slack Unarchve Conversation
  x-api-slug: slack
  description: Reverses conversation archival.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/slack-logo.png
  humanURL: https://slack.com
  baseURL: https://slack.com//api//conversations.unarchive
  tags: Messaging,Conversations, Archives
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/conversationsunarchive-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/conversationsunarchive-post-openapi.md
- name: Slack Get Group
  x-api-slug: slack
  description: Gets information about a private channel.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/slack-logo.png
  humanURL: https://slack.com
  baseURL: https://slack.com//api//groups.info
  tags: Messaging,Groups
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/groupsinfo-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/groupsinfo-get-openapi.md
- name: Slack Revoke Public URL
  x-api-slug: slack
  description: Revokes public/external sharing access for a file
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/slack-logo.png
  humanURL: https://slack.com
  baseURL: https://slack.com//api//files.revokePublicURL
  tags: Messaging,Files
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/filesrevokepublicurl-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/filesrevokepublicurl-post-openapi.md
- name: Slack List Conversations
  x-api-slug: slack
  description: Lists all channels in a Slack team.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/slack-logo.png
  humanURL: https://slack.com
  baseURL: https://slack.com//api//conversations.list
  tags: Messaging,Conversations
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/conversationslist-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/conversationslist-get-openapi.md
- name: Slack List Stars
  x-api-slug: slack
  description: Lists stars for a user.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/slack-logo.png
  humanURL: https://slack.com
  baseURL: https://slack.com//api//stars.list
  tags: Messaging,Stars
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/starslist-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/starslist-get-openapi.md
- name: Slack Get Reaction
  x-api-slug: slack
  description: Gets reactions for an item.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/slack-logo.png
  humanURL: https://slack.com
  baseURL: https://slack.com//api//reactions.get
  tags: Messaging,Reactions
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/reactionsget-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/reactionsget-get-openapi.md
- name: Slack Get Messages History
  x-api-slug: slack
  description: Fetches history of messages and events from direct message channel.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/slack-logo.png
  humanURL: https://slack.com
  baseURL: https://slack.com//api//im.history
  tags: Messaging
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/imhistory-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/imhistory-get-openapi.md
- name: Slack Pin Item
  x-api-slug: slack
  description: Pins an item to a channel.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/slack-logo.png
  humanURL: https://slack.com
  baseURL: https://slack.com//api//pins.add
  tags: Messaging,Pins
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/pinsadd-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/pinsadd-post-openapi.md
- name: Slack Leave Channel
  x-api-slug: slack
  description: Leaves a channel.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/slack-logo.png
  humanURL: https://slack.com
  baseURL: https://slack.com//api//channels.leave
  tags: Messaging,Channels
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/channelsleave-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/channelsleave-post-openapi.md
- name: Slack Get Permalink
  x-api-slug: slack
  description: Retrieve a permalink URL for a specific extant message
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/slack-logo.png
  humanURL: https://slack.com
  baseURL: https://slack.com//api//chat.getPermalink
  tags: Messages
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/chatgetpermalink-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/chatgetpermalink-get-openapi.md
- name: Slack Rename Channel
  x-api-slug: slack
  description: Renames a channel.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/slack-logo.png
  humanURL: https://slack.com
  baseURL: https://slack.com//api//channels.rename
  tags: Messaging,Channels
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/channelsrename-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/channelsrename-post-openapi.md
- name: Slack List Files
  x-api-slug: slack
  description: Lists & filters team files.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/slack-logo.png
  humanURL: https://slack.com
  baseURL: https://slack.com//api//files.list
  tags: Messaging,Files
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/fileslist-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/fileslist-get-openapi.md
- name: Slack Mark Multiparty Direct Messages
  x-api-slug: slack
  description: Sets the read cursor in a multiparty direct message channel.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/slack-logo.png
  humanURL: https://slack.com
  baseURL: https://slack.com//api//mpim.mark
  tags: Messaging
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/mpimmark-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/mpimmark-post-openapi.md
- name: Slack Update Group Users
  x-api-slug: slack
  description: Update the list of users for a User Group
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/slack-logo.png
  humanURL: https://slack.com
  baseURL: https://slack.com//api//usergroups.users.update
  tags: Messaging,Groups
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/usergroupsusersupdate-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/usergroupsusersupdate-post-openapi.md
- name: Slack Set Conversation Topic
  x-api-slug: slack
  description: Sets the topic for a conversation.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/slack-logo.png
  humanURL: https://slack.com
  baseURL: https://slack.com//api//conversations.setTopic
  tags: Messaging,Conversations
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/conversationssettopic-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/conversationssettopic-post-openapi.md
- name: Slack Get Conversation Members
  x-api-slug: slack
  description: Retrieve members of a conversation.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/slack-logo.png
  humanURL: https://slack.com
  baseURL: https://slack.com//api//conversations.members
  tags: Messaging,Conversations
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/conversationsmembers-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/conversationsmembers-get-openapi.md
- name: Slack Open Conversation
  x-api-slug: slack
  description: Opens or resumes a direct message or multi-person direct message.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/slack-logo.png
  humanURL: https://slack.com
  baseURL: https://slack.com//api//conversations.open
  tags: Messaging,Conversations
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/conversationsopen-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/conversationsopen-post-openapi.md
- name: Slack Unpin Item
  x-api-slug: slack
  description: Un-pins an item from a channel.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/slack-logo.png
  humanURL: https://slack.com
  baseURL: https://slack.com//api//pins.remove
  tags: Messaging,Pins
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/pinsremove-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/pinsremove-post-openapi.md
- name: Slack Delete File
  x-api-slug: slack
  description: Deletes a file.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/slack-logo.png
  humanURL: https://slack.com
  baseURL: https://slack.com//api//files.delete
  tags: Messaging,Files
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/filesdelete-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/filesdelete-post-openapi.md
- name: Slack List Pins
  x-api-slug: slack
  description: Lists items pinned to a channel.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/slack-logo.png
  humanURL: https://slack.com
  baseURL: https://slack.com//api//pins.list
  tags: Messaging,Pins
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/pinslist-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/pinslist-get-openapi.md
- name: Slack Test API
  x-api-slug: slack
  description: Checks API calling code.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/slack-logo.png
  humanURL: https://slack.com
  baseURL: https://slack.com//api//api.test
  tags: Messaging
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/apitest-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/apitest-get-openapi.md
- name: Slack List Reminders
  x-api-slug: slack
  description: Lists all reminders created by or for a given user.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/slack-logo.png
  humanURL: https://slack.com
  baseURL: https://slack.com//api//reminders.list
  tags: Messaging,Reminders
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/reminderslist-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/reminderslist-get-openapi.md
- name: Slack Get Presence
  x-api-slug: slack
  description: Gets user presence information.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/slack-logo.png
  humanURL: https://slack.com
  baseURL: https://slack.com//api//users.getPresence
  tags: Messaging,Presence
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/usersgetpresence-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/usersgetpresence-get-openapi.md
- name: Slack Update Group
  x-api-slug: slack
  description: Update an existing User Group
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/slack-logo.png
  humanURL: https://slack.com
  baseURL: https://slack.com//api//usergroups.update
  tags: Messaging,Groups
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/usergroupsupdate-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/usergroupsupdate-post-openapi.md
- name: Slack Leave Conversation
  x-api-slug: slack
  description: Leaves a conversation.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/slack-logo.png
  humanURL: https://slack.com
  baseURL: https://slack.com//api//conversations.leave
  tags: Messaging,Conversations
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/conversationsleave-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/conversationsleave-post-openapi.md
- name: Slack Get File
  x-api-slug: slack
  description: Gets information about a team file.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/slack-logo.png
  humanURL: https://slack.com
  baseURL: https://slack.com//api//files.info
  tags: Messaging,Files
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/filesinfo-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/filesinfo-get-openapi.md
- name: Slack Leave Group
  x-api-slug: slack
  description: Leaves a private channel.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/slack-logo.png
  humanURL: https://slack.com
  baseURL: https://slack.com//api//groups.leave
  tags: Messaging,Groups
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/groupsleave-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/groupsleave-post-openapi.md
- name: Slack App Permissions
  x-api-slug: slack
  description: Returns list of permissions this app has on a team.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/slack-logo.png
  humanURL: https://slack.com
  baseURL: https://slack.com//api//apps.permissions.info
  tags: Messaging,Permissions
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/appspermissionsinfo-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/appspermissionsinfo-get-openapi.md
- name: Slack Create Group
  x-api-slug: slack
  description: Create a User Group
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/slack-logo.png
  humanURL: https://slack.com
  baseURL: https://slack.com//api//usergroups.create
  tags: Messaging,Groups
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/usergroupscreate-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/usergroupscreate-post-openapi.md
- name: Slack Create Child Group
  x-api-slug: slack
  description: Clones and archives a private channel.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/slack-logo.png
  humanURL: https://slack.com
  baseURL: https://slack.com//api//groups.createChild
  tags: Messaging,Groups, archives
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/groupscreatechild-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/groupscreatechild-post-openapi.md
- name: Slack Mark Channel
  x-api-slug: slack
  description: Sets the read cursor in a channel.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/slack-logo.png
  humanURL: https://slack.com
  baseURL: https://slack.com//api//channels.mark
  tags: Messaging,Channels
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/channelsmark-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/channelsmark-post-openapi.md
- name: Slack Delete Photo
  x-api-slug: slack
  description: Delete the user profile photo
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/slack-logo.png
  humanURL: https://slack.com
  baseURL: https://slack.com//api//users.deletePhoto
  tags: Messaging,Photos
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/usersdeletephoto-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/usersdeletephoto-post-openapi.md
- name: Slack Set User Profile Photo
  x-api-slug: slack
  description: Set the user profile photo
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/slack-logo.png
  humanURL: https://slack.com
  baseURL: https://slack.com//api//users.setPhoto
  tags: Messaging,Users
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/userssetphoto-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/userssetphoto-post-openapi.md
- name: Slack Share Public URL
  x-api-slug: slack
  description: Enables a file for public/external sharing.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/slack-logo.png
  humanURL: https://slack.com
  baseURL: https://slack.com//api//files.sharedPublicURL
  tags: Messaging,Files
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/filessharedpublicurl-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/filessharedpublicurl-post-openapi.md
- name: Slack Remove User From Conversation
  x-api-slug: slack
  description: Removes a user from a conversation.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/slack-logo.png
  humanURL: https://slack.com
  baseURL: https://slack.com//api//conversations.kick
  tags: Messaging,Conversations
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/conversationskick-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/conversationskick-post-openapi.md
- name: Slack Sent Ephemeral lMessage
  x-api-slug: slack
  description: Sends an ephemeral message to a user in a channel.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/slack-logo.png
  humanURL: https://slack.com
  baseURL: https://slack.com//api//chat.postEphemeral
  tags: Messages
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/chatpostephemeral-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/chatpostephemeral-post-openapi.md
- name: Slack Rename Conversation
  x-api-slug: slack
  description: Renames a conversation.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/slack-logo.png
  humanURL: https://slack.com
  baseURL: https://slack.com//api//conversations.rename
  tags: Messaging,Conversations
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/conversationsrename-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/conversationsrename-post-openapi.md
- name: Slack Migration Exchange
  x-api-slug: slack
  description: For Enterprise Grid workspaces, map local user IDs to global user IDs
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/slack-logo.png
  humanURL: https://slack.com
  baseURL: https://slack.com//api//migration.exchange
  tags: Messaging
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/migrationexchange-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/migrationexchange-get-openapi.md
- name: Slack Enable Group
  x-api-slug: slack
  description: Enable a User Group
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/slack-logo.png
  humanURL: https://slack.com
  baseURL: https://slack.com//api//usergroups.enable
  tags: Messaging,Groups
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/usergroupsenable-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/usergroupsenable-post-openapi.md
- name: Slack End Do Not Disturb Snooze
  x-api-slug: slack
  description: Turns on Do Not Disturb mode for the current user, or changes its duration.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/slack-logo.png
  humanURL: https://slack.com
  baseURL: https://slack.com//api//dnd.setSnooze
  tags: Messaging,Do Not Disturb
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/dndsetsnooze-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/dndsetsnooze-post-openapi.md
- name: Slack Update Message
  x-api-slug: slack
  description: Updates a message.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/slack-logo.png
  humanURL: https://slack.com
  baseURL: https://slack.com//api//chat.update
  tags: Messages
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/chatupdate-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/chatupdate-post-openapi.md
- name: Slack Get Multiparty Direct Message History
  x-api-slug: slack
  description: Fetches history of messages and events from a multiparty direct message.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/slack-logo.png
  humanURL: https://slack.com
  baseURL: https://slack.com//api//mpim.history
  tags: Messaging
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/mpimhistory-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/mpimhistory-get-openapi.md
- name: Slack Request App Permissions
  x-api-slug: slack
  description: Allows an app to request additional scopes
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/slack-logo.png
  humanURL: https://slack.com
  baseURL: https://slack.com//api//apps.permissions.request
  tags: Messaging,Permissions
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/appspermissionsrequest-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/appspermissionsrequest-get-openapi.md
- name: Slack Start Real Time Messaging Files
  x-api-slug: slack
  description: Searches for files matching a query.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/slack-logo.png
  humanURL: https://slack.com
  baseURL: https://slack.com//api//search.files
  tags: Messaging,Real Time
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/searchfiles-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/searchfiles-get-openapi.md
- name: Slack Get User Identity
  x-api-slug: slack
  description: Get a user's identity.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/slack-logo.png
  humanURL: https://slack.com
  baseURL: https://slack.com//api//users.identity
  tags: Messaging,Users
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/usersidentity-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/usersidentity-get-openapi.md
- name: Slack Get Logs
  x-api-slug: slack
  description: Gets the access logs for the current team.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/slack-logo.png
  humanURL: https://slack.com
  baseURL: https://slack.com//api//team.accessLogs
  tags: Messaging,Logs
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/teamaccesslogs-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/teamaccesslogs-get-openapi.md
- name: Slack Invite User To Group
  x-api-slug: slack
  description: Invites a user to a private channel.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/slack-logo.png
  humanURL: https://slack.com
  baseURL: https://slack.com//api//groups.invite
  tags: Messaging,Groups
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/groupsinvite-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/groupsinvite-post-openapi.md
- name: Slack Unarchive Channel
  x-api-slug: slack
  description: Unarchives a channel.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/slack-logo.png
  humanURL: https://slack.com
  baseURL: https://slack.com//api//channels.unarchive
  tags: Messaging,Channels, Archives
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/channelsunarchive-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/channelsunarchive-post-openapi.md
- name: Slack Connect Real Time Messaging
  x-api-slug: slack
  description: Starts a Real Time Messaging session.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/slack-logo.png
  humanURL: https://slack.com
  baseURL: https://slack.com//api//rtm.connect
  tags: Messaging,Real Time
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/rtmconnect-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/rtmconnect-get-openapi.md
- name: Slack Get Team
  x-api-slug: slack
  description: Gets information about the current team.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/slack-logo.png
  humanURL: https://slack.com
  baseURL: https://slack.com//api//team.info
  tags: Messaging,Teams
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/teaminfo-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/teaminfo-get-openapi.md
- name: Slack Get Conversation History
  x-api-slug: slack
  description: Fetches a conversation's history of messages and events.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/slack-logo.png
  humanURL: https://slack.com
  baseURL: https://slack.com//api//conversations.history
  tags: Messaging,Conversations
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/conversationshistory-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/conversationshistory-get-openapi.md
- name: Slack Create Channel
  x-api-slug: slack
  description: Creates a channel.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/slack-logo.png
  humanURL: https://slack.com
  baseURL: https://slack.com//api//channels.create
  tags: Messaging,Channels
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/channelscreate-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/channelscreate-post-openapi.md
- name: Slack Reply to Messages
  x-api-slug: slack
  description: Retrieve a thread of messages posted to a direct message conversation
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/slack-logo.png
  humanURL: https://slack.com
  baseURL: https://slack.com//api//im.replies
  tags: Messaging
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/imreplies-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/imreplies-get-openapi.md
- name: Slack Create Group
  x-api-slug: slack
  description: Creates a private channel.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/slack-logo.png
  humanURL: https://slack.com
  baseURL: https://slack.com//api//groups.create
  tags: Messaging,Groups
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/groupscreate-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/groupscreate-post-openapi.md
- name: Slack Add Reminders
  x-api-slug: slack
  description: Creates a reminder.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/slack-logo.png
  humanURL: https://slack.com
  baseURL: https://slack.com//api//reminders.add
  tags: Messaging,Reminders
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/remindersadd-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/remindersadd-post-openapi.md
- name: Slack Set Conversation Purpose
  x-api-slug: slack
  description: Sets the purpose for a conversation.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/slack-logo.png
  humanURL: https://slack.com
  baseURL: https://slack.com//api//conversations.setPurpose
  tags: Messaging,Conversations
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/conversationssetpurpose-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/conversationssetpurpose-post-openapi.md
- name: Slack Join Channel
  x-api-slug: slack
  description: Joins a channel, creating it if needed.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/slack-logo.png
  humanURL: https://slack.com
  baseURL: https://slack.com//api//channels.join
  tags: Messaging,Channels
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/channelsjoin-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/channelsjoin-post-openapi.md
- name: Slack List Groups
  x-api-slug: slack
  description: List all User Groups for a team
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/slack-logo.png
  humanURL: https://slack.com
  baseURL: https://slack.com//api//usergroups.list
  tags: Messaging,Groups
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/usergroupslist-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/usergroupslist-get-openapi.md
- name: Slack Get User Profile
  x-api-slug: slack
  description: Retrieves a user's profile information.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/slack-logo.png
  humanURL: https://slack.com
  baseURL: https://slack.com//api//users.profile.get
  tags: Messaging,Users
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/usersprofileget-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/usersprofileget-get-openapi.md
- name: Slack Open Group
  x-api-slug: slack
  description: Opens a private channel.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/slack-logo.png
  humanURL: https://slack.com
  baseURL: https://slack.com//api//groups.open
  tags: Messaging,Groups
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/groupsopen-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/groupsopen-post-openapi.md
- name: Slack List Emojis
  x-api-slug: slack
  description: Lists custom emoji for a team.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/slack-logo.png
  humanURL: https://slack.com
  baseURL: https://slack.com//api//emoji.list
  tags: Messaging,Emoji
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/emojilist-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/emojilist-get-openapi.md
- name: Slack Get Conversation
  x-api-slug: slack
  description: Retrieve information about a conversation.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/slack-logo.png
  humanURL: https://slack.com
  baseURL: https://slack.com//api//conversations.info
  tags: Messaging,Conversations
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/conversationsinfo-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/conversationsinfo-get-openapi.md
- name: Slack Share Message
  x-api-slug: slack
  description: Share a me message into a channel.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/slack-logo.png
  humanURL: https://slack.com
  baseURL: https://slack.com//api//chat.meMessage
  tags: Messages
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/chatmemessage-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/chatmemessage-post-openapi.md
- name: Slack End Do Not Disturb Snooze
  x-api-slug: slack
  description: Ends the current user's snooze mode immediately.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/slack-logo.png
  humanURL: https://slack.com
  baseURL: https://slack.com//api//dnd.endSnooze
  tags: Messaging,Do Not Disturb
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/dndendsnooze-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/dndendsnooze-post-openapi.md
- name: Slack Group History
  x-api-slug: slack
  description: Fetches history of messages and events from a private channel.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/slack-logo.png
  humanURL: https://slack.com
  baseURL: https://slack.com//api//groups.history
  tags: Messaging,Groups
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/groupshistory-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/groupshistory-get-openapi.md
- name: Slack Search Real Time Messaging
  x-api-slug: slack
  description: Searches for messages matching a query.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/slack-logo.png
  humanURL: https://slack.com
  baseURL: https://slack.com//api//search.messages
  tags: Messaging,Real Time
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/searchmessages-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/searchmessages-get-openapi.md
- name: Slack Start Real Time Messaging
  x-api-slug: slack
  description: Starts a Real Time Messaging session.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/slack-logo.png
  humanURL: https://slack.com
  baseURL: https://slack.com//api//rtm.start
  tags: Messaging,Real Time
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/rtmstart-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/rtmstart-get-openapi.md
- name: Slack Set Channel Topic
  x-api-slug: slack
  description: Sets the topic for a channel.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/slack-logo.png
  humanURL: https://slack.com
  baseURL: https://slack.com//api//channels.setTopic
  tags: Messaging,Channels
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/channelssettopic-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/channelssettopic-post-openapi.md
- name: Slack Set Group Topic
  x-api-slug: slack
  description: Sets the topic for a private channel.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/slack-logo.png
  humanURL: https://slack.com
  baseURL: https://slack.com//api//groups.setTopic
  tags: Messaging,Groups
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/groupssettopic-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/groupssettopic-post-openapi.md
- name: Slack Open Multiparty Direct Messages
  x-api-slug: slack
  description: This method opens a multiparty direct message.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/slack-logo.png
  humanURL: https://slack.com
  baseURL: https://slack.com//api//mpim.open
  tags: Messaging
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/mpimopen-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/mpimopen-post-openapi.md
- name: Slack Remove Reaction
  x-api-slug: slack
  description: Removes a reaction from an item.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/slack-logo.png
  humanURL: https://slack.com
  baseURL: https://slack.com//api//reactions.remove
  tags: Messaging,Reactions
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/reactionsremove-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/reactionsremove-post-openapi.md
- name: Slack Delete Reminders
  x-api-slug: slack
  description: Deletes a reminder.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/slack-logo.png
  humanURL: https://slack.com
  baseURL: https://slack.com//api//reminders.delete
  tags: Messaging,Reminders
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/remindersdelete-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/remindersdelete-post-openapi.md
- name: Slack Disable Group
  x-api-slug: slack
  description: Disable an existing User Group
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/slack-logo.png
  humanURL: https://slack.com
  baseURL: https://slack.com//api//usergroups.disable
  tags: Messaging,Groups
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/usergroupsdisable-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/usergroupsdisable-post-openapi.md
- name: Slack Add File Comments
  x-api-slug: slack
  description: Add a comment to an existing file.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/slack-logo.png
  humanURL: https://slack.com
  baseURL: https://slack.com//api//files.comments.add
  tags: Messaging,Files,Comments
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/filescommentsadd-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/filescommentsadd-post-openapi.md
- name: Slack List Messages
  x-api-slug: slack
  description: Lists direct message channels for the calling user.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/slack-logo.png
  humanURL: https://slack.com
  baseURL: https://slack.com//api//im.list
  tags: Messaging
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/imlist-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/imlist-get-openapi.md
- name: Slack Set Channel Purpose
  x-api-slug: slack
  description: Sets the purpose for a channel.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/slack-logo.png
  humanURL: https://slack.com
  baseURL: https://slack.com//api//channels.setPurpose
  tags: Messaging,Channels
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/channelssetpurpose-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/channelssetpurpose-post-openapi.md
- name: Slack Reply to Multiparty Direct Messages
  x-api-slug: slack
  description: Retrieve a thread of messages posted to a direct message conversation
    from a multiparty direct message.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/slack-logo.png
  humanURL: https://slack.com
  baseURL: https://slack.com//api//mpim.replies
  tags: Messaging
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/mpimreplies-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/mpimreplies-get-openapi.md
- name: Slack Open Dialog
  x-api-slug: slack
  description: Open a dialog with a user
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/slack-logo.png
  humanURL: https://slack.com
  baseURL: https://slack.com//api//dialog.open
  tags: Messaging,Conversations
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/dialogopen-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/dialogopen-get-openapi.md
- name: Slack Get Do Not Disturb Status
  x-api-slug: slack
  description: Retrieves the Do Not Disturb status for users on a team.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/slack-logo.png
  humanURL: https://slack.com
  baseURL: https://slack.com//api//dnd.teamInfo
  tags: Messaging,Do Not Disturb
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/dndteaminfo-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/dndteaminfo-get-openapi.md
- name: Slack List Team Users
  x-api-slug: slack
  description: Lists all users in a Slack team.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/slack-logo.png
  humanURL: https://slack.com
  baseURL: https://slack.com//api//users.list
  tags: Messaging,Users
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/userslist-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/userslist-get-openapi.md
- name: Slack Invite User To Conversation
  x-api-slug: slack
  description: Invites users to a channel.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/slack-logo.png
  humanURL: https://slack.com
  baseURL: https://slack.com//api//conversations.invite
  tags: Messaging,Conversations
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/conversationsinvite-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/conversationsinvite-post-openapi.md
- name: Slack Test Auth
  x-api-slug: slack
  description: Checks authentication & identity.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/slack-logo.png
  humanURL: https://slack.com
  baseURL: https://slack.com//api//auth.test
  tags: Messaging,Authentication
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/authtest-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/authtest-get-openapi.md
- name: Slack List Channels
  x-api-slug: slack
  description: Lists all channels in a Slack team.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/slack-logo.png
  humanURL: https://slack.com
  baseURL: https://slack.com//api//channels.list
  tags: Messaging,Channels
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/channelslist-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/channelslist-get-openapi.md
- name: Slack Set Group Purpose
  x-api-slug: slack
  description: Sets the purpose for a private channel.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/slack-logo.png
  humanURL: https://slack.com
  baseURL: https://slack.com//api//groups.setPurpose
  tags: Messaging,Groups
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/groupssetpurpose-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/groupssetpurpose-post-openapi.md
- name: Slack Invite Channel User
  x-api-slug: slack
  description: Invites a user to a channel.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/slack-logo.png
  humanURL: https://slack.com
  baseURL: https://slack.com//api//channels.invite
  tags: Messaging,Channels
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/channelsinvite-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/channelsinvite-post-openapi.md
- name: Slack Oauth Access
  x-api-slug: slack
  description: Exchanges a temporary OAuth code for an API token.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/slack-logo.png
  humanURL: https://slack.com
  baseURL: https://slack.com//api//oauth.access
  tags: Messaging,OAuth
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/oauthaccess-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/oauthaccess-get-openapi.md
- name: Slack List Multiparty Direct Messages
  x-api-slug: slack
  description: Lists multiparty direct message channels for the calling user.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/slack-logo.png
  humanURL: https://slack.com
  baseURL: https://slack.com//api//mpim.list
  tags: Messaging
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/mpimlist-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/mpimlist-get-openapi.md
- name: Slack Unarchive Group
  x-api-slug: slack
  description: Unarchives a private channel.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/slack-logo.png
  humanURL: https://slack.com
  baseURL: https://slack.com//api//groups.unarchive
  tags: Messaging,Groups, Archives
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/groupsunarchive-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/groupsunarchive-post-openapi.md
- name: Slack Get Channel Thread
  x-api-slug: slack
  description: Retrieve a thread of messages posted to a channel
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/slack-logo.png
  humanURL: https://slack.com
  baseURL: https://slack.com//api//channels.replies
  tags: Messaging,Channels
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/channelsreplies-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/channelsreplies-get-openapi.md
- name: Slack Send Channel Message
  x-api-slug: slack
  description: Sends a message to a channel.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/slack-logo.png
  humanURL: https://slack.com
  baseURL: https://slack.com//api//chat.postMessage
  tags: Messages
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/chatpostmessage-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/chatpostmessage-post-openapi.md
- name: Slack Make User Inactive
  x-api-slug: slack
  description: Marks a user as active.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/slack-logo.png
  humanURL: https://slack.com
  baseURL: https://slack.com//api//users.setActive
  tags: Messaging,Users
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/userssetactive-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/userssetactive-post-openapi.md
- name: Slack Archive Conversation
  x-api-slug: slack
  description: Archives a conversation.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/slack-logo.png
  humanURL: https://slack.com
  baseURL: https://slack.com//api//conversations.archive
  tags: Messaging,Conversations, Archives
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/conversationsarchive-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/conversationsarchive-post-openapi.md
- name: Slack Get Team Profile
  x-api-slug: slack
  description: Retrieve a team's profile.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/slack-logo.png
  humanURL: https://slack.com
  baseURL: https://slack.com//api//team.profile.get
  tags: Messaging,Teams
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/teamprofileget-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/teamprofileget-get-openapi.md
- name: Slack Archive Group
  x-api-slug: slack
  description: Archives a private channel.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/slack-logo.png
  humanURL: https://slack.com
  baseURL: https://slack.com//api//groups.archive
  tags: Messaging,Groups,Archives
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/groupsarchive-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/groupsarchive-post-openapi.md
- name: Slack Reply Conversation
  x-api-slug: slack
  description: Retrieve a thread of messages posted to a conversation
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/slack-logo.png
  humanURL: https://slack.com
  baseURL: https://slack.com//api//conversations.replies
  tags: Messaging,Conversations
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/conversationsreplies-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/conversationsreplies-get-openapi.md
- name: Slack Remove Star from Item
  x-api-slug: slack
  description: Removes a star from an item.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/slack-logo.png
  humanURL: https://slack.com
  baseURL: https://slack.com//api//stars.remove
  tags: Messaging,Stars
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/starsremove-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/starsremove-post-openapi.md
- name: Slack
  x-api-slug: slack
  description: Slack is a team communication application providing services such as
    real-time messaging, archiving, and to search for modern teams. It offers one-on-one
    messaging, private groups, persistent chat rooms, and direct messaging as well
    as group chats organized by topic. All content inside Slack is searchable from
    one search box and it integrates with a number of third-party services, including
    Google Docs, Dropbox, Heroku, Crashlytics, GitHub, and Zendesk.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/slack-logo.png
  humanURL: https://slack.com
  baseURL: https://slack.com//api
  tags: Slack
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/slack/master/_listings/slack/openapi.md
x-common:
- type: x-application-gallery
  url: https://slack.com/apps
- type: x-blog
  url: http://slackhq.com/
- type: x-blog
  url: https://medium.com/slack-developer-blog
- type: x-blog-rss
  url: http://slackhq.com/rss
- type: x-blog-rss
  url: https://medium.com/feed/slack-developer-blog
- type: x-branding
  url: https://slack.com/brand-guidelines
- type: x-buttons
  url: https://api.slack.com/docs/slack-button
- type: x-c-sharp-sdk
  url: https://api.slack.com/web
- type: x-change-log
  url: https://api.slack.com/changelog
- type: x-developer
  url: https://api.slack.com/
- type: x-faq
  url: https://api.slack.com/faq
- type: x-getting-started
  url: https://slack.com/getting-started
- type: x-github
  url: https://github.com/slackhq
- type: x-incoming-webhooks
  url: https://api.slack.com/incoming-webhooks
- type: x-oauth-overview
  url: https://api.slack.com/docs/oauth
- type: x-oauth-scopes
  url: https://api.slack.com/docs/oauth-scopes
- type: x-outgoing-webhooks
  url: https://api.slack.com/outgoing-webhooks
- type: x-presence
  url: https://api.slack.com/docs/presence
- type: x-pricing
  url: https://slack.com/pricing
- type: x-privacy
  url: https://slack.com/privacy-policy
- type: x-rate-limits
  url: https://api.slack.com/docs/rate-limits
- type: x-real-time-messaging-api
  url: https://api.slack.com/rtm
- type: x-road-map
  url: https://api.slack.com/roadmap
- type: x-security
  url: https://slack.com/security
- type: x-status
  url: https://status.slack.com/
- type: x-support
  url: https://get.slack.help/hc/en-us
- type: x-terms-of-service
  url: https://slack.com/terms-of-service
- type: x-transparency-report
  url: https://slack.com/transparency-report
- type: x-twitter
  url: https://twitter.com/slackapi
- type: x-website
  url: https://slack.com
include: []
maintainers:
- FN: Kin Lane
  x-twitter: apievangelist
  email: info@apievangelist.com
---