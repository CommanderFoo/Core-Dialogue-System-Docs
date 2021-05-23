# Dialogue Conversation

Below are all the properties that are on the `Dialogue_Conversation` script.

| Property Name | Description |
| ------------- | ----------- |
| `id` | The ID for this conversation.  This **must** be unique. |
| `name` | The name of the character.  This will show up in the speaker element. |
| `dialogue_trigger` | The dialogue trigger for this character.  It's important that the dialogue trigger is a child of the character as the system will look at the parent element and attach the indicator to it. |
| `repeat_dialogue` | Turn off if you do not want the character to repeat their dialogue. |
| `disable_player_look` | Disables the player look when the dialogue is active. |
| `disable_player_movement` | Disables the player movement when the dialogue is active. |
| `disable_player_mount` | Disables the player mount while the dialogue is active. |
| `disable_player_crouch` | Disables the player crouch while the dialogue is active. |
| `disable_player_jump` | Disables the player jump while the dialogue is active. |
| `enable_ui_interact` | If enabled, the player can interact with UI elements. |
| `enable_ui_cursor` | If enabled, the player will be able to see and use their cursor. |
| `hide_reticle` | If enabled, then the reticle will be hidden while the dialogue is active. |
| `call_event` | The event to call when this conversation becomes active. |
| `show_indicator` | If enabled, then an indicator above the characters head will show to the player as a visual way to let them know they can interact with this character. |
| `indicator_offset` | The offset of the indicator. |
| `indicator_template` | The indicator template to use for this character. |
| `random` | If enabled, then it will pick a random entry while respecting conditions. |