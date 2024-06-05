# tutorial\_start

<mark style="color:purple;">**`Client`**</mark>

Create a tutorial notification message on screen.

{% tabs %}
{% tab title="Definition" %}
```lua
hud.tutorial_start(title --[[ string ]], desc --[[ string ]], delay --[[ integer ]], infinite_display --[[ boolean ]])
```
{% endtab %}

{% tab title="Example" %}
Tutorial will close automatically after \~5 seconds (The default behaviour when `infinite_display` is set to `false`):

```lua
hud.tutorial_start("Vehicle", "You can enter vehicle by pressing {ACTION_IMG}", 0, false)
```

Tutorial will remain on screen until we call [tutorial\_end](tutorial\_end.md):

```lua
local tutorial_open = false
local timer = 0

event.add_handler("core:on_gameplay_enter", function()
    
    -- Create and display the tutorial message.
    hud.tutorial_start("Vehicle", "You can enter vehicle by pressing {ACTION_IMG}", 0, true)

    -- Set the timer to 0.
    timer = 0

    -- Inform that the tutorial has been created.
    tutorial_open = true
end)

event.add_handler("core:on_gameplay_render", function(_delta_time)

    -- If a tutorial is currently opened...
    if tutorial_open then
        
        -- Increment the timer with the delta time.
        timer = timer + _delta_time

        -- When the timer pass 10 seconds...
        if timer >= 10.0 then

            -- Close the tutorial created above.
            hud.tutorial_end()
            
            -- Inform that the tutorial is now closed.
            tutorial_open = false
        end
    end
end)
```

<figure><img src="../../.gitbook/assets/image (4).png" alt=""><figcaption></figcaption></figure>
{% endtab %}
{% endtabs %}

{% hint style="warning" %}
`delay`parameter represent how much time it takes to show the message on screen. if you want to actually display for X seconds on screen, set the parameter`infinite_display`to`true`, add a delay to your code, and when you're done, use [tutorial\_end ](tutorial\_end.md)function.
{% endhint %}
