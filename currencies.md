# Currencies

## Introduction
Skuddbot features a currency system, with support for multiple currencies. At the moment we have only one, but there are definetly more to come!

## Available Currencies
| Currency name | Technical Name | Used for              | Leaderboard? | Editable? |
|---------------|----------------|-----------------------|--------------|-----------|
| Skuddbux      | `SKUDDBUX`     | Betting in minigames. | Yes          | Yes       |
## Commmands
The command for viewing and editing an users currencies is `!currency`.

### Command parameters
| Parameter          | Type             | Description                                                                                                                                                                             | Required?    |
|--------------------|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------|
| User ID / Mention  | Number / Mention | Speciefies what user you want to view/edit, defaults to yourself.                                                                                                                       | When editing |
| Currency           | String           | This parameter takes a technical name of a currency. This specifies the currency you want to edit. Parameter is automatically set to upper case and dashes are replaced by underscores. | When editing |
| Add / Remove / Set | String           | This parameter can be `add`, `remove` or `set`. This specifies what operation you want to carry out on the specified currency                                                           | When editing |
| Amount             | Number           | This parameter specifies with what amount you want to carry out the specified operation.                                                                                                | When editing |

### Command examples
| Example                                        | Description                                                     | Response                                         |
|------------------------------------------------|-----------------------------------------------------------------|--------------------------------------------------|
| `!currency`                                    | Simplest form, this shows your own currency balances.           | Embed with your currency balances.               |
| `!currency @MyNameIsDave#0001`                 | This shows the currencies of user MyNameIsDave#0001.            | Embed with currencies of user MyNameIsDave#0001. |
| `!currency @MyNameIsDave#0001 SKUDDBUX add 10` | This adds 10 to the currency balance of user MyNameIsDave#0001. | :white_check_mark: reaction to the message.      |


