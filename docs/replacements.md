# Replacements

!!! info
	If you have a replacement variable idea that you would like to see added, let me know.

The following list of replacements can be used for dialogue text and player choice text.

| Type | Description |
| ------------- | ----------- |
| `{name}` | This will be replaced by the name of the player. |
| `{id}` | This will be replaced by the ID of the player. |
| `{hitpoints}` | This will be replaced with the current hit points (aka health) of the player. |
| `{maxhitpoints}` | This will be replaced with the max hit points (aka max halth) of the player. |
| `{kills}` | This will be replaced with the total kills the player has got. |
| `{deaths}` | This will be replaced with the total deaths the player has got. |
| `{maxjumpcount}` | This will be replaced with the max jump count the player can do. |
| `{resource=RESOURCE}` | This will be replaced with the resource amount. See the Resource section below for more information. |

## <span style="color: yellow">Resources</span>
Resource replacement variables support a few additional parameters to handle displaying it to the player so it reads correct.

How many games do you see that don't handle the plural of something like "Potions", or "Coins". Reading "You have 12 Potion" is not a hard problem to solve but is often overlooked. So the resource replacement variable will handle this for you.

`resource=potion,true,true`

The 2 parameters after the type and value `resource=potion` tells the system to include the resource name, and handle the plural for you.
