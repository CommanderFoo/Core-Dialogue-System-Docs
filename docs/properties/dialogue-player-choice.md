# Dialogue Player Choice

Here are all the properties for the `Dialogue_Player_Choice` script.

| Property Name | Description |
| ------------- | ----------- |
| `id` | The ID for this conversation.  This **must** be unique. |
| `text` | The text to display in the dialogue. |
| `condition` | Any conditions for this choice.  See Conditions section. |
| `call_event` | The event to call when this choice becomes active. |
| `width_override` | Override width of the dialogue for this entry.  Only applies from 1 choice entry.  So overriding the width on the first choice is all that needs to be done if you have multiple choices. |
| `height_override` | Override the height of the dialogue just for this entry. |
| `animation_stance` | The animation stance for this NPC. |
| `animation_stance_playback_rate` | The playback rate of the stance animation. |
| `animation_stance_loop` | If true then the animation stance will loop. |
| `animation` | The animation to play for this NPC. |
| `animation_loop` | If true then the animation will loop or go back to it's stance animation. |
| `animation_playback_rate` | The playback rate of the animation. |

!!! tip
	It's not a good idea to use an animation stance and animation for the NPC, as the animation will override the stance.