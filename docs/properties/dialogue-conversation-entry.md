# Dialogue Conversation Entry

Here are all the properties for the `Dialogue_Conversation_Entry` script.

| Property Name | Description |
| ------------- | ----------- |
| `id` | The ID for this conversation. This **must** be unique. |
| `text` | The text to display in the dialogue. |
| `condition` | Any conditions for this entry. See Conditions section. |
| `call_event` | The event to call when this entry becomes active. |
| `width_override` | Override the width of the dialogue just for this entry. |
| `height_override` | Override the height of the dialogue just for this entry. |
| `random` | If enabled, then it will pick a random entry and respect conditions. |
| `disable_letter_animation` | If enabled, then the letter animation for this dialogue will be disabled. |
| `animation_stance` | The animation stance for this NPC. |
| `animation_stance_playback_rate` | The playback rate of the stance animation. |
| `animation_stance_loop` | If true then the animation stance will loop. |
| `animation` | The animation to play for this NPC. |
| `animation_loop` | If true then the animation will loop or go back to it's stance animation. |
| `animation_playback_rate` | The playback rate of the animation. |
| `thinking_time` | If greater than 0, then the entry will be delayed in showing, giving an effect of thinking for the NPC. |

!!! tip
	It's not a good idea to use an animation stance and animation for the NPC, as the animation will override the stance.
