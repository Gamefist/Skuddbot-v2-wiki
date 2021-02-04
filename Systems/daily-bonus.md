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
For more information about [controlling bonus amounts](/Features/server-settings.md#daily-bonus), view the [Server settings](/Features/server-settings.md) article.
{% endhint %}

### Weekly bonus
When a user has reached their cap, their bonus will no longer increase. But when they have hit their cap, they will be eligible for a weekly bonus. Once a week (every 7th day), the user will receive double their normal bonus. 
The user does not need to do anything to get the bonus, if it is the 7th day and the user claims their daily bonus, the weekly bonus is automatically applied.

#### Ineligble for weekly bonus
A user can be ineligble for the weekly bonus, this is due to a cooldown on the weekly bonus, this can happen when the user has missed a day of claiming. The cooldown is 7 days.

## Cutoff point and offset
You can claim your bonus once per day. By default, a day is from midnight UTC until 23:59:59 UTC. This means the cutoff is, by default, at midnight UTC.

### Offset
A user can offset their cutoff point by 12 hours in either direction (-12 and +12). This is done using the `TIMEZONE` user setting.
{% hint style="success" %}
To figure out what your offset is, you can use the list of timezones on [timeanddate.com](https://www.timeanddate.com/time/zones/). Find your timezone in the table and see your offset in the right-most colum.
{% endhint %}
{% hint style="warning" %}
* Half hour offsets are not supported.
* When setting your offset using the `!usersettings` command, enter negative numbers as `-12` and positive numbers as `12` (no plus sign).
{% endhint %}
{% hint style="info" %}
For more information about user settings, view the [User settings](/Features/user-settings.md) article.
{% endhint %}

## Streaks
### Continuing and building a streak
To upkeep a streak, a user must claim their bonus on consecutive days, before the cutoff point.

### Losing a streak
Users can lose their streak when they do not claim their streaks on consecutive day. A penalty of 5 days is incurred for every day the user has missed.

### Viewing a streak
Streaks are recorded in the stats of a user, and can be viewed using the `!stats` command.
{% hint style="info" %}
For more information about stats, view the [stats](/Features/stats.md) article.
{% endhint %}
