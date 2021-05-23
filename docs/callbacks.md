# Callbacks

Callbacks are for the more experienced creator because the return value can be based on many conditions depending on what you want to achieve.

For example, you can use callbacks to determine if an NPC should display certain choices to the player.  Maybe you have an NPC that sells special weapons, but you only want to list weapons that are for that players level.  This is where callbacks become really useful and make the dialogues appear more dynamic.

To use the callback system, you need to require the `Dialogue_System` into your script by dropping it on as a custom property.

```
local Dialogue_System = require(script:GetCustomProperty("Dialogue_System"))
```

The next part is to hook up your callback so the system knows about it.  It's important to make sure that the callback name matches the value in the condition of the conversation entry / choice.

So for example if the player choice condition for an item an NPC sells would be `function=can_show_epic_sword`.

```lua
Dialogue_System.register_callback("can_show_epic_sword", function()
	if(local_player:GetResource("level") >= 10) then
		return true
	end

	return false
end)
```

In the example above, we return true if the players level is greater than or equal to 10, if it is, then the NPC will display the player choice allowing them to purchase the Epic Sword.

If for some reason you need to remove a callback, then you can unregister it like so...

```lua
Dialogue_System.unregister_callback("can_show_epic_sword")
```

!!! tip
	Take a look at the NPC `Nya` in the `Advanced Example` to show you how it can be used to display a different dialogue entry every time the player comes back to speak to them.