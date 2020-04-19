# Server settings
## Introduction
Skuddbot featurs an server settings. This allows server owners to change parts of Skuddbot to their liking and tailor their own Skuddbot experience for their server. 

## Available settings
| Setting name                                                          | Technical name            | Short description                                                                  | Value type                | Default value |
|-----------------------------------------------------------------------|---------------------------|------------------------------------------------------------------------------------|---------------------------|---------------|
| [Minimun experience gained](#gaining-experience)                      | `XP_MIN`                  | Defines the minimum amount of experience gained per message.                       | Number                    | 10            |
| [Maximum experience gained](#gaining-experience)                      | `XP_MAX`                  | Defines the maximum amount of experience gained per message.                       | Number                    | 15            |
| [~~Minimun experience gained on twitch~~](#gaining-experience)        | `XP_MIN_TWITCH`           | Defines the minimum amount of experience gained per message on Twitch.             | Number                    | 10            |
| [~~Maximum experience gained on twitch~~](#gaining-experience)        | `XP_MAX_TWITCH`           | Defines the maximum amount of experience gained per message on Twitch.             | Number                    | 15            |
| [Experience base value](#leveling-curve)                              | `XP_BASE`                 | Defines how much experience an user needs to level up from level one to level two. | Number                    | 1500          |
| [Experience multiplier](#leveling-curve)                              | `XP_MULTIPLIER`           | Defines how steep the experience leveling curve is.                                | Number with decimal place | 1.2           |
| [~~Twitch channel~~](#twitch-channel)                                 | `TWITCH_CHANNEL`          | Defines what Twitch channel the bot is in.                                         | String                    | null          |
| [Welcome message](#welcome-and-goodbye-messages)                      | `WELCOME_MESSAGE`         | Defines the message that will be posted when a user joins the server.              | String                    | null          |
| [Goodbye message](#welcome-and-goodbye-messages)                      | `GOODBYE_MESSAGE`         | Defines the message that will be posted when a user leaves the server.             | String                    | null          |
| [Welcome and goodbye messages channel](#welcome-and-goodbye-messages) | `WELCOME_GOODBYE_CHANNEL` | Defines the channel where the welcome and goodbye messages will be posted.         | Number (of: channel ID)   | -1            |
| [Grant role on join](#granting-role-on-join)                          | `ROLE_ON_JOIN`            | Defines what role will be given to users that join the server.                     | String (of: role name)    | null          |

## Setting details
### Experience settings
#### Gaining experience
The settings `XP_MIN` and `XP_MAX` control the amount of experience a user gains per message, a random amount is picked between these values and added to the users experience total. The `XP_MIN_TWITCH` and `XP_MAX_TWITCH` settings do the same thing but for Twitch.
{% hint style="warning" %}
Twitch support is currently under development.
{% endhint %}

#### Leveling curve
The settings`XP_BASE` and `XP_MULTIPLIER` control the leveling curve. These two values are put into a formula to calculate how much experience a user needs to level up.
{% hint style="info" %}
For more information about experience, please view the [Experience](/Systems/experience.md) article.
{% endhint %}

### Twitch channel
This defines what Twitch channel the bot is in. It will track stats there for the server this setting applies to.
{% hint style="warning" %}
Twitch support is currently under development.
{% endhint %}

### Welcome and goodbye messages
The `WELCOME_MESSAGE` and `GOODBYE_MESSAGE` settings control the message format of their respective event. These formats can contain 2 variables:  
* `$name` - Will be replaced by the name of the user that joins or leaves the server.
* `$server` - Will be replaced by the name of the server that is joined/left.

`WELCOME_GOODBYE_CHANNEL` takes a ID of a channel for these messages to be posted in, this setting must be set in order for the welcome and goodbye messages to work.
{% hint style="info" %}
For more information about getting ID's of things in discord, please view [Turning on developer mode](/getting-started.md#turning-on-developer-mode) in the [Getting started](/getting-started.md) article.
{% endhint %}

### Granting role on join
The `ROLE_ON_JOIN` setting takes the name of a role, this role will then be given to users when they join the server.
{% hint style="danger" %}
* Make sure the role name is typed exactly as it is set in Discord. This setting is case sensitive.
* Make sure the role you are trying to give is below the highest role Skuddbot has in the hierarchy.
{% endhint %}


