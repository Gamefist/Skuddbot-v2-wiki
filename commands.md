# Commands

### !serversettings <a id="h.uh0mvukv4axj"></a>

NOTE: This command requires admin access.

The settings command allows you to alter the way Skuddbot works on your server. It’s simple to use:

| !serversettings | Lists all available settings. |
| :--- | :--- |
| !serversettings &lt;setting&gt; | Prints out more information about the specified setting. |
| !serversettings &lt;setting&gt; &lt;value&gt; | Changes the specified setting to the specified value. |

#### Settings explanation <a id="h.edewfyz7gjcq"></a>

The settings below are in my opinion not so straightforward as the other ones. If a setting is not listed it should be straightforward enough, unless you’re stupid, but you can just ask me then.

**XP\_BASE and XP\_MULTIPLIER**

Please refer to [XP system](https://docs.google.com/document/d/e/2PACX-1vRybBTqggx_4rXkHyPkpEJlhBq9F8hbhvhOAZuhL2ROs7ZOIcGzQdltDqipKiF9rWBytHt3jYISJZy8/pub?embedded=true#h.jtwkvf1zvwyn) in this manual.

**TWITCH\_CHANNEL**

This value will hold the Twitch Channel where users should be granted XP for your server. In order to set this, you’ll need to link your Twitch Account to Skuddbot by typing !twitch, once you’ve done that, you can set this value. \(See [SkuddSync](https://docs.google.com/document/d/e/2PACX-1vRybBTqggx_4rXkHyPkpEJlhBq9F8hbhvhOAZuhL2ROs7ZOIcGzQdltDqipKiF9rWBytHt3jYISJZy8/pub?embedded=true#h.ip8qjii8uyi6)\)

**WELCOME\_MESSAGE and GOODBYE\_MESSAGE**

This is pretty much what it says, but there are a few variables you can put in this message:

$user changes to the username/mention of the user that joins/leaves.

$guild changes to the name of your server.

$nl specifies a new line.

**ADMIN\_ROLE**

This is the name of the Role that should be able to access the admin commands of Skuddbot. When you see in this manual that something requires “admin access” this is what I refer to. Please be aware: This is case sensitive!

Commands that require admin access:

* !serversettings

**ROLE\_ON\_JOIN**

This role will be assigned to anyone that joins the server! Make sure this role is below the highest role that skuddbot has assigned to him in your roles panel!

**WELCOME\_GOODBYE\_CHAN**

This channel is where the Welcome and Goodbye messages will be posted, this will default to the general channel.

**STREAM\_LIVE**

This defines if the stream is live and analytics should be kept, this is a back up for when the automated way fails, you shouldn’t need to touch this.

**ALLOW\_ANALYTICS**

This defines if analytics should be made, if you do not like analytics you can turn it off.

**ALLOW\_REWARDS**

This defines if people should gain rewards from analytics, for now these are static, a way to customize them will come soon. But you can turn them off.

### !game <a id="h.rhuawrrh3jpa"></a>

This just changes the “playing” status of Skuddbot. Currently only available to a few people, and those who have access, know that they have access. No, you won’t get access.

### !xp &lt;mention/twitch username&gt; <a id="h.vfvnftmdthf1"></a>

Does pretty much what you would expect it to do, show your current XP amount, level and level progress. When you mention a person it shows that user’s level and progress, when you specify a Twitch username it searches for that user, when it finds it it shows that, otherwise it will default to YOUR XP.

### !xplb <a id="h.1yvgy36dxggu"></a>

Shows the current top 10 of the users with the most XP on the server it’s used on.

### !twitch <a id="h.1ww7hxx43nzu"></a>

This will allow you to link your Twitch account to Skuddbot, just type the command to get started, Skuddbot will help you through this process. \(Refer to: [SkuddSync](https://docs.google.com/document/d/e/2PACX-1vRybBTqggx_4rXkHyPkpEJlhBq9F8hbhvhOAZuhL2ROs7ZOIcGzQdltDqipKiF9rWBytHt3jYISJZy8/pub?embedded=true#h.ip8qjii8uyi6)\)

### !dumpdata <a id="h.tf79ulwj751x"></a>

Currently disabled, was originally used to create a .json dump of all users, will come back later though.

### !about <a id="h.e4kk1iitw3k"></a>

Just shows some information about Skuddbot. This information is global.

### !flip \(works on Twitch too\) <a id="h.7ittytol9aep"></a>

 \(╯°□°）╯︵ buıɥʇǝɯos dıןɟ ɐuuɐʍ noʎ pɹɐɥ os ǝbɐɹ noʎ uǝɥʍ ɹoɟ

### !addmsg &lt;type&gt; &lt;message&gt; \(pm only\) <a id="h.resfs65x7l48"></a>

 For awesome people: Add messages to the pool of playing, error or alive messages.

### !setping &lt;message&gt; \(pm only\) <a id="h.vocu53v3ul5a"></a>

For awesome people: Set the response of the bot that they will get when they do !ping

## !usersettings <a id="h.zby4s6408ibm"></a>

This command will allow you to change your personal settings in Skuddbot. It works like this:

| !usersettings | Lists all available settings. |
| :--- | :--- |
| !usersettings &lt;setting&gt; | Prints out more information about the specified setting. |
| !usersettings &lt;setting&gt; &lt;value&gt; | Changes the specified setting to the specified value. |

####  Settings explanation: <a id="h.jm2f8rad905f"></a>

The settings below are in my opinion not so straightforward as the other ones. If a setting is not listed it should be straightforward enough, unless you’re stupid, but you can just ask me then.

 **TRACK\_ME**

Turn this off if you do not wanna be tracked by Skuddbot, this will PAUSE progress   and will not delete it. Currently this only affects XP and Analytics, but no other tracking is done. Commands will still work. Can also be changed using !toggletracking on Twitch.

