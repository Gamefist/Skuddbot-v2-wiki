# Free for All

{% hint style="warning" %}
This page contains features that are currently released in **BETA** they may or may not work, and may change at any time!
{% endhint %}

## Introduction
Free for All is a minigame where multiple users can battle, but only one will emerge victorious!

## Game flow
### Starting a game
A game is started with the `!freeforall` command. The user starting the game will be the host of the game.
A new game will be created and is put into what is known as the "outstanding" phase. There can only be one outstanding game per server.
{% hint style="info" %}
The [command](#command) section contains more details about the command.
{% endhint %}

### Entering the game
When a game is outstanding, a user can enter the game in 2 ways, without a bet or with a bet. Entering without a bet may be done by clicking the ![](https://i.imgur.com/o8SZQlF.png) reaction. When the user wants to enter with their default bet as bet they click the ![](https://i.imgur.com/rgDJ0uw.png) reaction. To match the highest current bet, the user clicks the ![](https://i.imgur.com/LqZbyj6.png) reaction. When a user wants to bet a different amount they use the command: `!freeforall <bet>`. 
{% hint style="info" %}
* Refer for to the [Betting Shortcuts](/Minigames/betting-shortcuts.md) articles, to see what shortcuts are currently available and what you can specify as your bet.
* For more information about the betting system, view the [betting system](#betting-system) section.
{% endhint %}

### Leaving the game
#### Using reactions
A user can leave the game by removing either the ![](https://i.imgur.com/o8SZQlF.png), ![](https://i.imgur.com/rgDJ0uw.png) or ![](https://i.imgur.com/LqZbyj6.png) reaction.
It does not matter whether they betted or not. Removing of those reactions will make the user leave the game.

#### Using commands
A user can  leave the game by typing `!freeforall leave`, any placed bet will be refunded.

### Changing bets
If a user wants to change their bet, they first must leave the game and then re-join it with their new bet.

### Starting the fight
When a game is outstanding, the host of the game can start the fight by clicking the ![](https://i.imgur.com/rEFJP65.png) reaction. The Free for All must contain at least 3 entrants for it to be started. When the game is started, the results will be revealed after 5 seconds.

#### Force-starting the fight
Users with the server admin permission can force-start the fight, this is done by adding the ![](https://i.imgur.com/UUpPhCO.png) reaction to the message. When forcefully starting a Free for All the entrants requirement is lowered from 3 to 2.
The fight will be marked as started by admin.
{% hint style="info" %}
For more information about permissions, view the [Permissions](/Systems/permissions.md) article.
{% endhint %}

### Post-game
The fight of Free for All is simulated in the background, meaning users actually kill each other, from this the bot also generates a kill feed. The kill feed can be viewed by clicking the ![](https://i.imgur.com/7fUiBDQ.png) reaction. To view the rewards breakdown, click the ![](https://i.imgur.com/BlfMxg2.png) reaction.

## Stats
| Stat                 | Technical name    | Tracks                                                          | Awarded                                            |
|----------------------|-------------------|-----------------------------------------------------------------|----------------------------------------------------|
| Wins                 | `FFA_WINS`        | The amount of times the user has won a Free for All             | When the user wins the Free for All                |
| Losses               | `FFA_LOSSES`      | The amount of times the user has been killed in a Free for All. | When the user gets killed in the Free for All      |
| Highest entrants win | `FFA_HIGHEST_WIN` | The highest amount of entrants in a game the user has won.      | When the user achieves a new highest entrants win. |
| Kills                | `FFA_KILLS`       | The amount of kills the user has gotten in a Free for All.      | When the user kills someone in a Free for All      |
| Bets won             | `FFA_BETS_WON`    | The amount of bets the user has won.                            | When the user wins a bet.                          |
| Bets lost            | `FFA_BETS_LOST`   | The amount of bets the user has lost.                           | When the user loses a bet.                         |
{% hint style="info" %}
* For more information about stats, view the [stats](/Features/stats.md) article.
* For more information about the betting system, view the [betting system](#betting-system) section.
{% endhint %}

## Rewards
This game gives out the following rewards:
| Action                                       | Reward                           |
|----------------------------------------------|----------------------------------|
| Killing a user                               | +50xp, +10 Skuddbux, +1 FFA kill |
| Winning the game                             | +100xp, +50 Skuddbux, +1 FFA win |
| Winning the game with a new highest entrants | FFA highest entrants updated     |

## Betting system
When a user enters a Free for All, they can place an optional bet. They are betting on themselves winning. When a user wins, and has placed a bet, they will win the amount of the bets from other entrants, and their own bet will double. When the winner hasn't betted, their will be no bets payed out.
Stats on winning/losing bets are being tracked.
{% hint style="info" %}
* For information on how to place bets, view the [entering the game](#entering-the-game) section.
* For more information on stats, view the [stats](#stats) section.
{% endhint %}

### Jackpot
When the user that wins, hasn't betted, all bets will be added to the Jackpot.
{% hint style="info" %}
For more information about the jackpot, view the [jackpot](/Systems/jackpot.md) article.
{% endhint %}

## Reminders and Auto-starting
Every 6 hours the host will be reminded of a outstanding game via a DM, but only if the following conditions are met:
* The game has atleast 3 entrants,.
* The host has their minigames reminders enabled.

The game will auto-start if:
* The entrants, since the last reminder, haven't increased.
* The game has been outstanding for at least 12 hours.

When the fight is auto-started, the fight is marked as auto-started by bot.
{% hint style="info" %}
For more information about enabling [minigame reminders](/Features/user-settings.md#minigame-reminders), view the [user settings](/Features/user-settings.md) article.
{% endhint %}

## Cooldown
This game has a 5 minute cooldown period, this applies to all entrants of the game and starts when the game ends. Users on cooldown may not start a game, but they may still enter it.

## Commands
The command for Free for All is `!freeforall`.
This command also listens to the following alias: `!ffa`.

#### Command parameters
| Parameter | Type    | Description                                                      | Required? |
|-----------|---------|------------------------------------------------------------------|-----------|
| Bet       | Number  | Defines the bet the user wants to place.                         | No        |
| **OR**    |         |                                                                  |           |
| `leave`   | Keyword | When the leave keyword is provided the user will leave the game. | Yes       |{% hint style="info" %}
Refer for to the [Betting Shortcuts](/Minigames/betting-shortcuts.md) articles, to see what shortcuts are currently available and what you can specify as your bet.
{% endhint %}


#### Command examples
| Example                          | Action                                                                      | Response                                                  |
|----------------------------------|-----------------------------------------------------------------------------|-----------------------------------------------------------|
| `!freeforall`                    | The user will be entered into the game with their default bet as their bet. | The message is deleted and the game message updated.      |
| `!freeforall 0`                  | The user will be entered into the game with no bet.                         | The message is deleted and the game message updated.      |
| `!freeforall 100`                | The user will be entered into the game with 100 Skuddbux as their bet.      | The message is deleted and the game message updated.      |
| `!freeforall <betting shortcut>` | The user will be entered into the game with the specified bet.              | The message is deleted and the game message updated.      |
| `!freeforall leave`              | The user leaves the game.                                                   | Confirmation of game leaving and game message is updated. |
{% hint style="info" %}
* When there's no current game active, using a command to enter the game will automatically create a new game.
* Reactions can be clicked to get a more detailed response.
{% endhint %}

#### Permission requirements
This command requires no permissions.
{% hint style="info" %}
For more information about permissions, view the [Permissions](/Systems/permissions.md) article.
{% endhint %}
