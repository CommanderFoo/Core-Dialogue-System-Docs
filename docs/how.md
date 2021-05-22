# How it Works

The `Dialogue System` works on a hierarchy structure system.  The reason for this is so that it was far more friendly to work with, more easy to visualise the structure of a conversation for a character, and quicker iteration to customise / edit the dialogue.

You can setup a conversation with a character and player in a few mins.   There is no need to edit Lua files, or write out dialogue branches in code, or have lots of properties with dialogue that is hard to visualise.

The key things to take away from this is there are 3 data container scripts that you will be dropping into the hierarchy.  

 - `Dialogue_Conversation`

	This data container script is the entry point for a character.  It's a good habit to rename this script to the name of the character the dialogue will be for.  You only need one of these per character.

 -  `Dialogue_Conversation_Entry`

	This data container script is the entry for the character.  Meaning, this is what the character will say to the player.  You can nest these and also have branching dialogue in no time at all.  `Dialogue_Player_Choice` data containers can also become childs of this container.

 -  `Dialogue_Player_Choice`

	This data container script is the player choice that will appear in the dialogue for the player to pick.  These can also be nested and become childs of `Dialogue_Conversation_Entry`.

The `Dialogue System` at runtime will traverse the data containers and build up a tree.  While doing so the system will look at any callbacks and conditions setup for each item in the tree.