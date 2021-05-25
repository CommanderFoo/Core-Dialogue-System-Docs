# Call Events

Call events is a way for you to use the `Events` API to connect to an event.  This is useful if you need to do perform something when a player opens a dialogue, or an entry is displayed.

The `call_event` property supports infinite parameters that will be passed to your handler, the first parameter passed to your handler is the object for either `Conversation`, `Entry`, or `Choice`.

So for example, the `call_event` property can be set like so where the first part of the string is the event name.

```
my_event;hello,1,2,3
```

So in this case the string `my_event` is the event that will be broadcasted too, and anything after the semi colon is the parameters that will be passed to your handler.

Example:

```
Events.Connect("my_event", function(obj, str, a, b, c)
	print(str, a, b, c)
end)
```

!!! tip
	This a good way to do something for specific entries in the NPCs conversation tree.  For example, you could play a certain animation for one of the entries.