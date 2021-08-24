# 11. Condition Functions

Condition functions are callbacks for the system to look at to see if an entry or choice can be used / appear. These can be quite powerful and add a lot more depth to the conversation between an NPC and the player.

As an example, we could use a callback to check if the NPC has an item in stock. If the item is in stock, then we display the dialogue entry, otherwise the system will look for the next entry to display instead.

In the video below, we will change the behaviour of the NPC so that if the NPC has a special item in stock, the choice for the player to purchase it will show up, otherwise it will not.

!!! warn
	To be able to use the callback system, we need to require the `Dialogue_System` API so we can register a callback. The video below shows you how to do this by dropping the `Dialogue_System` script as a custom property onto the `Example` script.

<iframe width="560" height="315" src="https://www.youtube.com/embed/XByeDuCG2cY" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

The return back of the callback determines if the choice should show or not.

```lua hl_lines="24 25 26"
-- Require Dialogue_System

local Dialogue_System = require(script:GetCustomProperty("Dialogue_System"))

-- Call events

Events.Connect("conversation_called", function(conversation)
	print(conversation:get_name())
end)

Events.Connect("greeted", function(entry)
	print(entry:get_text())
end)

Events.Connect("cookies", function(choice)
	print(choice:get_text())
end)

-- Callback functions

-- Return false to hide the choice
-- Return true to show the choice

Dialogue_System.register_callback("has_special_item", function()
	return true
end)
```
