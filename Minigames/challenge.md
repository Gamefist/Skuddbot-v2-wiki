# Challenge

## Introduction
Challenge is a minigame where users can challenge each other to a one on one battle. The winner is chosen at random and is rewarded with experience.

## Game flow
### Starting a fight
A challenge is started by either challenging another user to a fight or by starting an open fight.

#### Inviting another user
To invite another user, the user types the command `!challenge <mention>`. Where `<mention>` is replaced with a mention of another user.
This mention may be any user, except bots and the user themselves. This fight can only be accepted by the invited user.

#### Starting a open fight
To start a open fight, the user types the command `!challenge open`. This fight can be accepted by any user, except the user themselves.

### Accepting a fight
A fight can be accepted in 2 ways. When a fight is accepted it will immediately start, the results are revealed after 5 seconds.

#### Using commands
A user can accept a fight by using the `!challenge <mention>` command, where they mention a user that has either invited them or has a open challenge standing out.

#### Using reactions
A user can accept a fight by clicking the ![](https://i.imgur.com/yp4rWf2.png) reaction, on a challenge that either is for them or is a open challenge.

### Canceling a fight
The user that has started a fight can cancel their fight using the `!challenge cancel` command.

### Post Game
After 5 seconds after the fight has been accepted, the results are revealed and the rewards are awarded.

## Stats
| Stats             | Technical name                | Tracks                                                   | Awarded                                                     |
|-------------------|-------------------------------|----------------------------------------------------------|-------------------------------------------------------------|
| Wins              | `CHALLENGE_WINS`              | The amount of challenges the users has won.              | When the user wins a challenge.                             |
| Losses            | `CHALLENGE_LOSSES`            | The amount of challenges the user has lost.              | When the user loses a challenge.                            |
| Winstreak         | `CHALLENGE_WINSTREAK`         | The amount of wins the user has gotten in a row.         | When the user wins a challenge, resets to 0 when they lose. |
| Longest Winstreak | `CHALLENGE_LONGEST_WINSTREAK` | The largest amount of wins the user has gotten in a row. | When they get a new longest winstreak.                      |

## Rewards
This game gives out the following rewards:
| Action                           | Reward                               |
|----------------------------------|--------------------------------------|
| Winning the game                 | +100xp, +1 win                       |
| Winning multiple games in a row. | +50xp (multiplied by amount of wins) |
| New highest winstreak            | Longest challenge winstreak updated  |

## Cooldown
This game has a 1 minute cooldown period, this applies to both users in the game and starts when the game ends. Users on cooldown may not start a new game, but they may still accept another.

## Commands
The command for challenge is `!challenge`.
This command also listens to the following aliases:  
* `!duel`
* `!fight`
* `!1v1`

#### Command parameters
| Parameter | Type         | Description                                                                                        | Required |
|-----------|--------------|----------------------------------------------------------------------------------------------------|----------|
| Mention   | User Mention | Defines which user needs to be challenged, accepts when there's a eligleble challenge outstanding. | Yes      |
| **OR**    |              |                                                                                                    |          |
| `open`    | Keyword      | When the open keyword is provided, a open challenge will be started.                               | Yes      |
| **OR**    |              |                                                                                                    |          |
| `cancel`  | Keyword      | When the cancel keyword is provided, the user's outstanding challenge will be cancelled.           | Yes      |

#### Command examples
| Example                         | Action                                                                                          | Response                                                      |
|---------------------------------|-------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| `!challenge @MyNameIsDave#0123` | The specified user will be challenged or when there's a eligable challenge it will be accepted. | A new challenge or a fight is started                         |
| `!challenge open`               | A new open challenge is started.                                                                | A new open challenge.                                         |
| `!challenge cancel`             | If there's one, the outstanding challenge is cancelled.                                         | ![](https://i.imgur.com/rEFJP65.png) reaction on the message. |
{% hint style="info" %}
Reactions can be clicked to get a more detailed response.
{% endhint %}

#### Permission requirements
This command requires no permissions.
{% hint style="info" %}
For more information about permissions, view the [Permissions](/Systems/permissions.md) article.
{% endhint %}