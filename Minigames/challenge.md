# Challenge

{% hint style="info" %}
This article is incomplete. It will be completed as soon as possible.
{% endhint %}

## Introduction
Challenge is a minigame where users can challenge each other to a one on one battle. The winner is chosen at random and is rewarded with experience.

## Game flow
### Starting a fight
A challenge is started by either challinging another user to a fight or by starting an open fight.

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

### Cancelling a fight
The user that has started a fight can cancel their fight using the `!challenge cancel` command.

### Post Game
After 5 seconds after the fight has been accepted, the results are revealed and the rewards are awarded.

## Stats
| Stats             | Technical name                | Tracks                                                   | Awarded                                                     |
|-------------------|-------------------------------|----------------------------------------------------------|-------------------------------------------------------------|
| Wins              | `CHALLENGE_WINS`              | The amount of challenges the users has won.              | When the user wins a challenge.                             |
| Losses            | `CHALLENGE_LOSSES`            | The amount of challenges the user has lost.              | When the user loses a challenge.                            |
| Winstreak         | `CHALLENGE_WINSTREAK`         | The amount of wins the user has gotten in a row.         | When the user wins a challenge, resets to 0 when they lose. |
| Longest Winstreak | `CHALLENGE_LONGEST_WINSTREAK` | The largest amount of wins the user has gotten in a row. | When they get a new highest winstreak.                      |

## Rewards

## Cooldown

## Commands
#### Command parameters

#### Command examples

#### Permission requirements