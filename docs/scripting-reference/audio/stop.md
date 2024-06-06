# stop

<mark style="color:purple;">**`Client`**</mark>

Stop a playing audio clip.

{% tabs %}
{% tab title="Definition" %}
```lua
audio.stop(playid --[[ integer ]])
```
{% endtab %}

{% tab title="Example" %}
```lua
-- Play a different "mission completion" sound every 5 secs indefinitely.
event.add_handler("core:on_gameplay_render", function()

    local playid = audio.play_one_shot("UI_Music", "Mission_Completion")

    event.wait(5000)

    audio.stop(playid)
end)
```
{% endtab %}
{% endtabs %}
