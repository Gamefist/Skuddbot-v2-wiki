# User settings

## Introduction
Skuddbot features an user settings system. This allows to change parts of Skuddbot to their liking, and tailor their own experience with the bot.
Settings are saved on a per-server-basis, so it is possible for users to have settings set to different values in different servers.

## Available settings
| Setting Name                                    | Technical Name       | Short Description                                       | Value Type | Default Value |
|-------------------------------------------------|----------------------|---------------------------------------------------------|------------|---------------|
| [Level up notification](#level-up-notification) | `LEVEL_UP_NOTIFY`    | Defines how you are notified about level ups.           | String     | REACTION      |
| [Tracking enabled](#track-me)                   | `TRACK_ME`           | Defines if the bot will track your statistics.          | Boolean    | true          |
| [Profile private](#profile-private)             | `PROFILE_PRIVATE`    | Defines if your profile is private.                     | Boolean    | false         |
| [Mention me](#mention-me)                       | `MENTION_ME`         | Defines if you are mentioned in useless commands.       | Boolean    | false         |
| [~~Minigame reminders~~](#minigame-reminders)   | `MINIGAME_REMINDERS` | Defines if you are reminded about outstanding minigames | Boolean    | true          |

## Setting details
### Level up notification
Level up notification defines how a user is notified about a level up, this setting is restricted to the following values:
| Value      | Notification behaviour                         |
|------------|------------------------------------------------|
| `REACTION` | You are notified by reaction about a level up. |
| `MESSAGE`  | You are notified by message about a level up.  |
| `DM`       | You are notified in DM's about a level up.     |
| `NONE`     | You are not notified about level ups.          |
{% hint style="info" %}
Reactions can be clicked to view a detailed message.  
Server owners can disable the `MESSAGE` notification setting, for more information about the [allow message level up notification server setting] view the [Server Settings](server-settings.md) article.
{% endhint %}

### Tracking enabled
This setting defines if Skuddbot tracks you. This includes all stats and currencies. If this is set to false, all progress will be paused, until this is turned back to true. You will still continue to show on leaderboards, regardless of what this setting is set to.

### Profile private
This setting defines if others are able to see your stats and currencies. When set to true, only you and people with Server Admin permissions can ask the bot for your stats. If you ask for your stats/profile, other people can still see it.
{% hint style="info" %}
For more information about permissions, view the [Permissions](/Systems/permissions.md) article.
{% endhint %}

### Mention me
This setting defines if you are mentioned in useless commands, these are commands like `!hug` and `!punch`.
{% hint style="info" %}
For more information about useless commands, view the [Useless Commands](/Commands/useless-commands.md) article.
{% endhint%}

### Mingame reminders
{% hint style="danger" %}
This setting is still under development and not in use yet.
{% endhint %}

## Command
The command for viewing and editing your settings is: `!usersettings`.   
This command also listens to the following aliasses: 
- `!usettings`

#### Command parameters
| Parameter | Type   | Description                                       | Required? |
|-----------|--------|---------------------------------------------------|-----------|
| Setting   | String | This defines the setting you want to view/edit.   | No        |
| Value     | Any    | This is the new value the setting will be set to. | No        |

#### Command examples
| Example                         | Action                                                     | Response                                                     |
|---------------------------------|------------------------------------------------------------|--------------------------------------------------------------|
| `!usersettings`                 | Simplest form, shows all settings and their current value. | A table with all settings and their current value.           |
| `!usersettings MENTION_ME`      | Views more detailed information about MENTION_ME setting.  | A list of detailed infromation about the MENTION_ME setting. |
| `!usersettings MENTION_ME true` | Updates the setting MENTION_ME to true.                    | ✅ reaction to the message.                                   |
{% hint style="info" %}
Reactions can be clicked to get a more detailed response.
{% endhint %}

#### Permission requirements
This command requires no permissions.
{% hint style="info" %}
For more information about permissions, view the [Permissions](/Systems/permissions.md) article.
{% endhint %}
