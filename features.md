# Features

### XP system <a id="h.i18ozlf4exnn"></a>

The XP system allows users to gain XP by being active in the server, currently XP is only gained by chatting, each message gains you a random amount between the set XP\_MIN and XP\_MAX \(that are set using the !serversettings command\) thresholds for that server. The bot basically rolls the dice \(RNG HYPE\) and what ever it rolls gets added to your total XP count. Then the bot quickly recalculates your level and progress to see if you have leveled up, if that may be the case the bot does a full calculation of everything and posts in the chat that you have leveled up.

Now, I know, this is not something ‘new’, but it kinda is because Skuddbot allows you to carry over your XP to your Twitch chat!

Twitch chat XP gaining works the same as Discord chat XP gaining, except, the bot doesn’t post when you have leveled up \(it still happens in the background, the bot will notify you the next time you post a message on Discord if you have leveled up with Twitch message\). XP gaining on Twitch is invisible and happens in the background. Also, Twitch chat uses different min/max thresholds which you can alter with the !serversettings command.

If users wish to see their XP they have to join your Discord server, link up their Twitch account using the !twitch command, and then type !xp in chat. If you wish a more in-depth guide of the account linking system you can refer to the [SkuddSync](https://docs.google.com/document/d/e/2PACX-1vRybBTqggx_4rXkHyPkpEJlhBq9F8hbhvhOAZuhL2ROs7ZOIcGzQdltDqipKiF9rWBytHt3jYISJZy8/pub?embedded=true#h.ip8qjii8uyi6) section in this manual.

#### XP Calulation <a id="h.c840jx50wrxm"></a>

XP and levels in Skuddbot are progressive, which means, the higher your level is, the more XP you require to advance to the next level. In order to achieve that, Skuddbot uses 2 values, a XP\_BASE and a XP\_MULTIPLIER, XP\_BASE defines how much XP is required to advance from level 1 to level 2. XP\_MULTIPLIER is the modifier that the requirement of the last level gets multiplied with to calculate the requirement to advance another level. If you would strip this bit down to a formula you would get something like this:  
![](https://www.google.com/chart?cht=tx&chf=bg,s,FFFFFF00&chco=000000&chl=X%7BP%7D_%7Bto%5C+lvl%5C+up%7D%3DX%7BP%7D_%7Bbase%5C+%7D%5Ctimes%7B%7D%5C+X%7BP%7D_%7Bmultiplier%7D%7B%5C+%7D%5E%7B%28level%5C+-%5C+1%29%7D)  


NOTE: Changing either of the XP\_BASE or XP\_MULTIPLIER will cause existing levels of users to be changed.

### SkuddSync <a id="h.ip8qjii8uyi6"></a>

SkuddSync is the System that ensures that users can link their Twitch account to their Discord account, and that their XP gets added up in real-time from both platforms. Now please note, you are not “linking” your accounts together, you are just verifying that you are indeed the owner of your account by typing a 6-character code in Skuddbot’s Twitch Channel. No OAuth2, no passwords, no tokens, just a simple 6-character code and a few clicks.  
It’s just as safe as OAuth2, the code you get is a one-time use only, and will be invalidated right after you put it in the Twitch chat. Skuddbot does NOT store your password, in fact, it can’t even access it.

This connection is different form the connection you can make with Discord and Twitch in your Discord User Settings, that connection can not be seen by Skuddbot, so we’ll need to create a different way, and that’s how SkuddSync was born.

By linking your accounts you’ll also get a nice 1000xp bonus.  
On link, Skuddbot will add up the XP from your Twitch and Discord and that total will be your new XP amount, after that we recalculate your level. For example: Level 2 \(40%\) and Level 2 \(60%\) does not become level 5. After you’ve reviewed the information, and it’s correct you can type !confirm to complete the link and activate SkuddSync, if there’s something wrong, you can type !cancel to stop the linking process and try again.

Once linked you cannot unlink! Links need to be done for each server separately, currently there is no way to carry over a link from a different server, may come in the future though.  
There is also a way to give linked users a bit “extra”, all you need to do is create a role called “Linked” \(exactly like that, capitalized properly and such\), and drag it down just above the @everyone role in the roles panel in your server settings. You can change everything about this role, change the color, permissions, whatever, but don’t change it’s name. If you don’t have this role, no roles will be assigned, Skuddbot will basically attempt to assign it, if it can’t, it will basically move on.

