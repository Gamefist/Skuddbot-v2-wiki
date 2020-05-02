# Free for All
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
When a game is outstanding, a user can enter the game in 2 ways, without a bet or with a bet. Entering without a bet may be done by clicking the ![](https://i.imgur.com/o8SZQlF.png) reaction. When the user wants to enter with their default bet as bet they click the ![](https://i.imgur.com/LqZbyj6.png) reaction. When a user wants to bet a different amount they use the command: `!freeforall <bet>`
{% hint style="info" %}
* For more information about the [default bet](/Features/user-settings.md#default-bet), view the [user settings](/Features/user-settings.md) article.
* For more information about the betting system, view the [betting system](#betting-system) section.
{% endhint %}

### Starting the fight
When a game is outstanding, the host of the game can start the fight by clicking the ![](https://i.imgur.com/rEFJP65.png) reaction. The Free for All must contain at least 3 entrants for it to be started. When the game is started, the results will be revealed after 5 seconds.

### Post-game
The fight of Free for All is simulated in the background, meaning users actually kill each other. The bot also generates a kill feed. The kill feed can be viewed by clicking the ![](https://i.imgur.com/7fUiBDQ.png) reaction.

## Stats
| Stat                 | Technical name    | Tracks                                                          | Awarded                                            |
|----------------------|-------------------|-----------------------------------------------------------------|----------------------------------------------------|
| Wins                 | `FFA_WINS`        | The amount of times the user has won a Free for All             | When the user wins the Free for All                |
| Losses               | `FFA_LOSSES`      | The amount of times the user has been killed in a Free for All. | When the user gets killed in the Free for All      |
| Highest entrants win | `FFA_HIGHEST_WIN` | The highest amount of entrants in a game the user has won.      | When the user achieves a new highest entrants win. |
| Kills                | `FFA_KILLS`       | The amount of kills the user has gotten in a Free for All.      | When the user kills someone in a Free for All      |
{% hint style="info" %}
For more information about stats, view the [stats](/Features/stats.md) article.
{% endhint %}

## Rewards
This game gives out the following rewards:
| Action                                       | Reward                           |
|----------------------------------------------|----------------------------------|
| Killing a user                               | +50xp, +10 Skuddbux, +1 FFA kill |
| Winning the game                             | +100xp, +50 Skuddbux, +1 FFA win |
| Winning the game with a new highest entrants | FFA highest entrants updated     |

## Betting
When a user enters a Free for All, they can place an optional bet. They are betting on themselves winning. When a user wins, and has placed a bet, they will win the amount of the bets from other entrants, and their own bet will double. When the user hasn't betted, their will be no bets payed out.
{% hint style="info" %}
For information on how to place bets, view the [entering the game](#entering-the-game) section.
{% endhint %}

## Reminders and Autostarting
Every 6 hours the host will be reminded of a outstanding game via a DM, but only if the following conditions are met:
* The game has atleast 3 entrants,.
* The host has their minigames reminders enabled.

The game will autostart if:
* The entrants, since the last reminder, haven't increased.
* The game has been outstanding for at least 12 hours.
{% hint style="info" %}
For more information about enabling [minigame reminders](/Features/user-settings.md#minigame-reminders), view the [user settings](/Features/user-settings.md) article.
{% endhint %}

## Commands
The command for Free for All is `!freeforall`.
This command also listens to the following alias: `!ffa`.

#### Command parameter
| Parameter | Type   | Description                        | Required?                   |
|-----------|--------|------------------------------------|-----------------------------|
| Bet       | Number | Defines the bet you want to place. | When a game is outstanding. |

#### Command examples
| Example    | Game outstanding? | Action                                                                  | Response                                                      |
|------------|-------------------|-------------------------------------------------------------------------|---------------------------------------------------------------|
| `!ffa`     | No                | A new game will be started.                                             | A message with a new game of Free for All.                    |
|            | Yes               | Invalid usage: Nothing happens.                                         | ❌ reaction to the mesage.                                     |
| `!ffa 100` | No                | A new game will be started, and the host is entered with the given bet. | A message with a new game of Free for All.                    |
|            | Yes               | The user is entered into the outstanding game of Free for All.          | The Free for All message is updated, and the message deleted. |
{% hint style="info" %}
Reactions can be clicked to get a more detailed response.
{% endhint %}

#### Permission requirements
This command requires no permissions.
{% hint style="info" %}
For more information about permissions, view the [Permissions](/Systems/permissions.md) article.
{% endhint %}
