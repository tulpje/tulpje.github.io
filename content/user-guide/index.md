---
title: User Guide
---

# Invite The Bot
Tulpje can be invited to your server using the following link: [Add To Discord](https://discord.com/oauth2/authorize?client_id=1220754275530051605)

# Permissions
What permissions the bot requests and why

* **View Channels:** required to do anything with channels
* **Manage Channels:** needed to set up fronter category and notification channel
* **Manage Roles:** needed to set up member roles
* **Create/Manage Expressions:** needed to create emojis
* **Send Messages:** bot responses and front change notifications
* **Read Message History:** used to track emoji usage in messages
* **Embed Links:** some of the bot's responses are considered embed links

# Commands

## Emojis

### /emoji stats
Shows the usage stats of your servers emojis in the server

![Screenshot listing emotes in the Tulpje Example Server, only 1 emote is shown](./emoji-stats-example.png)

### /emoji maintenance
Cleans up any emoji you have since deleted from your server.
Under normal circumstances you shouldn't have to run this

![Screenshot showing the result of the command, 0 emojis were cleaned up](./emoji-maintenance-example.png)

### /emoji clone
Copy the specified emojis to this server

![Screenshot showing how to use the emoji clone command with an emoji dramatically exclaiming nooooooo](./emoji-clone-command-example.png)

![Screenshot showing the result of the emoji clone command with an emoji dramatically exclaiming nooooooo](./emoji-clone-result-example.png)

## PluralKit
To make use of any of the [PluralKit](https://pluralkit.me/) modules you have to
set it up first using `/pk setup`

### /pk setup
Configures the bot for use with your PluralKit system

![Screenshot showing how to use the pk setup command with the exmpl PluralKit system](./pk-setup-command-example.png)

![Screenshot showing the result of the pk setup command with the exmpl PluralKit system](./pk-setup-result-example.png)

### Fronter Category
Set up a category in the current server that displays the fronters for the
system specified in `/pk setup`

#### /pk fronters setup
Creates a category in your server that'll contain the list of fronters

![An image showing the command to set up the fronter list, it says "/pk fronters setup title:Fronters"](./pk-fronters-setup-command-example.png)

![An image showing the bot's response it says "Fronter category succesfully set-up!"](./pk-fronters-setup-result-example.png)

After running the command you should now have a new category:

![An image showing what the new category looks like in the discord client, it shows an empty "Fronters" category with underneath that a General category with a single channel named "#general" for example purposes](./pk-fronters-setup-category-example.png)

#### /pk fronters update
Manually updates the list of fronters in your server, in case automatic updates aren't working

![An image showing the bot's response after running /pk fronters update, it says "Fronter category updated!"](./pk-fronters-update-result-example.png)

After updating your fronters should be listed under category:

![An image showing a Fronters category, with 2 channels below it, Myriad Kit and Tester T. Testington](./pk-fronters-update-category-example.png)

#### Front Notifications
Allows you to follow systems and have notifications sent in a channel in the current
server whenever a system's fronters change

Here's an example notification:

![An example notification, it has a header stating "Switch: PluralKit Example System" and a list of mebmers: Myriad Kit, Tester T. Testington. It also shows the date 1/12/2020 3:21](./pk-notify-message-example.png)

#### /pk notify setup
Configure a channel to receive switch notifications in

![An image showing the command to set up the notification channel, it says "/pk notify setup channel:switches"](./pk-notify-setup-command-example.png)

![An image showing the bot's response it says "bot will notify you of front changes in #switches"](./pk-notify-setup-result-example.png)

#### /pk notify list
List the systems you're currently receiving switch notifications for

![An image showing the result of the command, it's a list containing one system "exmpl - PluralKit Example System"](./pk-notify-list-result-example.png)

#### /pk notify add
Add a system to receive switch notifications for

![An image showing the command to use to add a system, it says "/pk notify add id:exmpl"](./pk-notify-add-command-example.png)

![An image showing the bot's response it says "PluralKit Example System added to notification list"](./pk-notify-add-result-example.png)

#### /pk notify remove
Remove a system you no longer wanna receive switch notifications for

![An image showing the command to use to remove a system, it says "/pk notify remove id:exmpl"](./pk-notify-remove-command-example.png)

![An image showing the bot's response it says "PluralKit Example System removed from notification list"](./pk-notify-remove-result-example.png)

### System Member Roles
Creates a role for each system member in this server, and assigns them to the user
that ran `/pk setup` to allow mentioning individual system members

#### /pk roles update
Creates roles in the discord for each individual member of your system.
All of these will be assigned to you so individual members can be mentioned.
*You can optionally specify your PluralKit token to also add private members.*

> **⚠️ Warning ⚠️**<br>
> Currently there's no way to delete the created roles
> so if you end up disliking them it might take some effort to remove them

You'll get a summary after updating roles completes

![An image of a summary of role changes, it says "2 roles created, 32 deleted, 2 assigned"](./pk-roles-update-result-example.png)

Others in the server can then mention the system member

![An image of the user typing "@Myriad" and an autocomplete showing up for "@Myriad Kit (Alter)](./pk-roles-update-mention-example.png)

And you get pinged when they do

![An image of someone mentioning "@Myriad Kit (Alter)" and the user receiving a ping](./pk-roles-update-ping-example.png)


### Other Commands

* `/stats` • show bot statistics
* `/info processes` • detailed bot process stats
* `/info shards` • detailed bot shard stats
