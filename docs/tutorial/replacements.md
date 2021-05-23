# 8. Replacements

Replacements are a way of providing you variables that you can place into your text for NPCs and choices, then at runtime the system will replace those variables.

For example, if you want your NPC to greet the player by saying "Hello CommanderFoo", we can use a name variable like so.

```
Hello {name}.
```

So let's change the first `Conversation_Entry` to include the name of the player when being greeted, and also the `Conversation_Entry` for when the player asks for cookies to also include some information about the players health by using `{hitpoints}`.

<iframe width="560" height="315" src="https://www.youtube.com/embed/1ENUFlVxkKU" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>