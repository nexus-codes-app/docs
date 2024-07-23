---
layout: default
title: Log Lookup
parent: Log
grand_parent: Commands
---
# `/log lookup`

The `/log lookup` command is used in conjunction with a log identifier (either from [`/log search`](https://apollo.swvn.io/commands/log/search.html) or the footer of a logged event's embed) to retrieve a logged event from the database, along with pertinent information relating to it. Different events will return different information, for example messageDeleteBulk will follow up with a text file of the deleted messages' content.