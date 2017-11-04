**Context ID**: The ID of the place a message was sent. UserID for PMs, Group or Channel ID for groups, channels, and supergroups. Something to note is that it is thought that Channel IDs can collide with User and Chat IDs, so we add -100 to ChannelIDs to ensure we do not have this issue.

**DateUpdated**: This is used to address the issue of the exporter only 'seeing' a snapshot of the state, and to store historical data. When, for example, a user changes their name, the old User will be kept, and the new User with updated details will have a newer DateUpdated. For this reason, DateUpdated and UserID together form the primary key of the User table.