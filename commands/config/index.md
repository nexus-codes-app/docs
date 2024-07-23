---
layout: default
title: Config
parent: Commands
nav_order: 2
---

# `/config`

## `/config channel`
Open the configuration modal on the specified channel. The 'remove' option may also be set to true to remove the specified channel's logging entirely.

Each server may have as many logging channels as they'd like, all that needs to happen is they be configured.

![configChannelSample](/assets/images/commands/configChannelSample.png)

### Included Events
Included Events is a comma-separated list of events from [this documented list](https://apollo.swvn.io/events/). If left empty, **all** events will be included by default.

### Excluded Events
Excluded Events is a comma-separated list of events from [this documented list](https://apollo.swvn.io/events/). As an example, this may be used in conjunction with an empty 'Included Events' to omit specific events from a given channel

### Ignored Users
Ignored Users is a comma-separated list of discord user IDs that should not be logged in this channel. (In the case of moderative actions, the executor of the action is what is checked against this list)

### Ignored Channels
Ignored Channels is a comma-separated list of channels in which actions should be ignored.

## `/config list`
Shows all configured channels along with their parameters. At this time it formats in YAML for readability.

![configListSample](/assets/images/commands/configListSample.png)