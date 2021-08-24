# Conditions

Conditions allow for you to do various checks and call callback functions to determine if the entry or player choice should appear. This is very useful for beginners as they don't need to write code to handle checking of certain types. However, the system does support an advanced feature called `function conditions` for the more experienced creator.

!!! note
	You can use up to 2 types in a condition.

	`resource=coin;>=100,resource=shop_pass;==1`

## Resource

This condition type allows you to check specific resources to see if the player has a certain amount.

For example, if your NPC has an item they sell, but you only want this to show up if the player has 100 Gold, then we can write a resource condition like this.

`resource=gold;>=100`

This tells the system that we want to check the `Gold` resource, and to see if the value is greater than or equal to the amount the player has.

Here are the condition checkers that the system supports.

| Operator | Description |
| ------------- | ----------- |
| `==` | If the resource is equal to the value return true. Example: `resource=gold;==500`. If the Gold resource is equal to 500 return true. |
| `>=` | If the resource is greater than or equal to the value return true. Example: `resource=gold;>=1`. If the gold resource is >= than or equal to 1 then return true. This is a way to check if a player has this resource. |
| `<=` | If the resource is less than or equal to the value return true. Example: `resource=gold;<=50` |

## Function

This condition is the callback function used for this entry / choice. This is a more advanced feature that will require some Lua knowledge, as you will need to register a callback that returns either `true` or `false`.

`function=check_something`

## Name

This condition type can be used if you want to check the players name is a match.

For example if you only want to show a dialogue / choice to a specific player, then you can set the condition like so.

`name=CommanderFoo`

If the player name matches the condition, then the dialogue entry / choice will show.

## ID

This condition type can be used if you want to check the players ID is a match.

For example if you only want to show a dialogue / choice for a specific player ID, then you can set the condition like so.

`id=d8sddjhdsa8dsadhsady8saff`

If the player ID matches the condition, then the dialogue entry / choice will show.

## Played

This condition type can be used if you want to check the `played` attribute of an entry.

For example if you only want a dialogue entry to appear once, then you can check to see if it has been played.

`played=true` or `played=false`
