# Currencies

## Introduction
Skuddbot features a currency system, with support for multiple currencies. Currencies can be spent, gained or lost by users.
At the moment we have only one, but there are definetly more to come! 

## Available currencies
| Currency name | Technical Name | Used for              | Leaderboard? | Editable? |
|---------------|----------------|-----------------------|--------------|-----------|
| Skuddbux      | `SKUDDBUX`     | Betting in minigames. | Yes          | Yes       |
## Commmands
### View and edit
The command for viewing and editing an users currencies is `!currency`.   
This command also listens to the following aliasses:
- `!currencies`
- `!wallet`
- `!skuddbux`
- `!bux`
- `!balance`
- `!bal`

#### Command parameters
| Parameter          | Type             | Description                                                                                                                                                                             | Required?    |
|--------------------|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------|
| User ID / Mention  | Number / Mention | Specifies what user you want to view/edit, defaults to yourself.                                                                                                                        | When editing |
| Currency           | String           | This parameter takes a technical name of a currency. This specifies the currency you want to edit. Parameter is automatically set to upper case and dashes are replaced by underscores. | When editing |
| Add / Remove / Set | String           | This parameter can be `add`, `remove` or `set`. This specifies what operation you want to carry out on the specified currency                                                           | When editing |
| Amount             | Number           | This parameter specifies with what amount you want to carry out the specified operation.                                                                                                | When editing |
#### Command examples
| Example                                           | Action                                                          | Response                                         |
|---------------------------------------------------|-----------------------------------------------------------------|--------------------------------------------------|
| `!currency`                                       | Simplest form, shows your own currencies.                       | Embed with your currencies.                      |
| `!currency @MyNameIsDave#0001`                    | Shows the currencies of user MyNameIsDave#0001.                 | Embed with currencies of user MyNameIsDave#0001. |
| `!currency @MyNameIsDave#0001 SKUDDBUX add 10`    | Adds 10 to the SKUDDBUX balance of user MyNameIsDave#0001.      | ✅ reaction to the message.                       |
| `!currency @MyNameIsDave#0001 SKUDDBUX remove 10` | Removes 10 from the SKUDDBUX balance of user MyNameIsDave#0001. | ✅ reaction to the message.                       |
| `!currency @MyNameIsDave#0001 SKUDDBUX set 10`    | Sets the SKUDDBUX balance of user MyNameIsDave#0001 to 10.      | ✅ reaction to the message.                       |
> Reactions can be clicked to get a more detailed response.

#### Permission Requirements
| Operation                                                              | Required permissions    |
|------------------------------------------------------------------------|-------------------------|
| Viewing your own currencies.                                           | No permissions required |
| Viewing someone else's currencies.                                     | No permissions required |
| Viewing someone else's currencies, who has made their profile private. | Server Admin            |
| Editing your own, or someone else's currencies.                        | Server Admin            |
> For more information on permissions, view the [Permissions](/Systems/permissions.md) article.  
> For more information about making your profile private, view the [profile private user setting](user-settings.md#profile-private) in the [User Settings](user-settings.md) article.






