# play\_one\_shot

<mark style="color:purple;">**`Client`**</mark>

Play a short clip with a specific group and clip name.

{% tabs %}
{% tab title="Definition" %}
```lua
local playid --[[ integer ]] = audio.play_one_shot(group --[[ string ]], clip --[[ string ]], delay --[[ integer ]])
```
{% endtab %}

{% tab title="Example" %}
```lua
-- Play a random mission completion sound.
audio.play_one_shot("UI_Music", "Mission_Completion")
```
{% endtab %}
{% endtabs %}
