# 10. Conditions

Conditions provide you with an inline way of performing a condition check for the entry or choice. For example, if you didn't want a choice to show up to the player if they already had some cookies, we can do a resource check and hide the choice from the player.

Conditions can be used to check a few different things and can really add a little more depth to the dialogues for players.

In the video below we will setup a resource check condition so when the player asks if the NPC has any cookies, the NPC will either respond with a message telling the player they already have some, or a message to tell the player they don't have any left to sell.

<iframe width="560" height="315" src="https://www.youtube.com/embed/BqoWeqU1ZCE" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

In the video there are 2 things to note.

1. **A replacement variable being used.**

	`{resource=cookie,true,true}`

	This is a replacement variable that will show the amount of cookies the play has in the dialogue text. The 2 `true` parameters are to handle 2 things automatically for us.

	- Write out the name of the resource.
	- Handle the plural for us so that cases such as "You have 1 Cookie" and "You have 100 Cookies" where "s" is added automatically so it reads better for the player.

2. **Condition Syntax.**

	`resource=cookie;>=1`

	This is the condition part. What we are doing here is telling the system to look at the resource `cookie` and return true if the the player has greater than or equal to 1 cookie. The system will look at this condition, and if is true, then the conversation entry will be displayed instead of the other one.

	This is an easy no code solution and allows quick iteration of your dialogue entries without needing to write any Lua code.

Server Script

```lua
Game.playerJoinedEvent:Connect(function(player)
	player:SetResource("cookie", 0) -- Set the cookie amount when the player joins
end)
```
