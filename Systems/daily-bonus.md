# Daily bonus
## Introduction
Users can claim a bonus of experience and currency each day. Bonuses scale exponentially if an user can upkeep their streak for claiming their bonus every day.

## Claiming a bonus
To claim a bonus, a user simply runs the command `!dailybonus`.
This command also listens to he following aliases:
* `!claim`
* `!db`

## Bonus amount
### Bonus scaling
The bonuses scale exponentially. If a user can build up a streak of claiming their bonus every day, they will gain more rewards over time.
There is a system to cap the scaling at a certain day. When the cap is reached, a user can still claim their bonus every day, but the amount won't grow anymore. The user is however still allowed to grow their streak, and this is also recorded in the stats.

The bonus amount is calculated using the following formula:
![](https://i.imgur.com/ZRjexJ3.png)

### Controlling bonus amounts
Server owners can control the amounts of bonuses their users can claim every day. The following things can be customized with the `!serversettings` command:
* Currency base amount
* Experience base amount
* Bonus multiplier
* Bonus multiplier cap
{% hint style="info" %}
For more infomation about [controlling bonus amounts](/Features/server-settings.md#daily-bonus), view the [Server settings](/Features/server-settings.md) article.
{% endhint %}

## Timer reset
A user can claim their bonus once a day. However the system does not make use of a 24 hour timer, but all users will be reset at once. The timer resets at 12AM UTC.
{% hint style="info" %}
To see what the current time in UTC is, please go to [timeanddate.com](https://www.timeanddate.com/worldclock/timezone/utc). 
{% endhint %}

## Streaks
### Continuing and building a streak
To upkeep a streak, a user must claim their bonus on consecutive days. 

### Losing a streak
A streak is lost, when a user has a unclaimed bonus when the timer resets.

### Viewing a streak
Streaks are recorded in the stats of a user, and can be viewed using the `!stats` command.
{% hint style="info" %}
For more information about stats, view the [stats](/Features/stats.md) article.
{% endhint %}
