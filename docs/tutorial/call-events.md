# 9. Call Events

Call events are a way for you to hook into the system to a specific conversation, conversation entry, or player choice so that you can do something when it is the current active item in the dialogue tree.

A use for call events would be to connect other parts of your code up so that you can perform some action based on which part of the dialogue is active.  So as an example, let's say you are talking to a guard standing next to a closed gate, when you trigger the conversation you want the gate to open.  The `call_event` property will be executed so that you can hook up your code to open the gate for the player.

In the example below, we will setup a call event for the conversation, the conversation entry, and one player choice.  All we will do is write out some text to the Event Log to show what was active.

!!! note
	A conversation `call_event` will be active the same time as the first conversation entry picked as they run at the same time.

<iframe width="560" height="315" src="https://www.youtube.com/embed/LqrUepgmYD8" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

```Lua
Events.Connect("conversation_called", function(conversation)
	print(conversation:get_name())
end)

Events.Connect("greeted", function(entry)
	print(entry:get_text())
end)

Events.Connect("cookies", function(choice)
	print(choice:get_text())
end)
```