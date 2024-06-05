# button\_just\_pressed

<mark style="color:purple;">**`Client`**</mark>

Return true or false when a specific button has just been pressed on a controller.

{% tabs %}
{% tab title="Definition" %}
```lua
local retval --[[ boolean ]] = input.button_just_pressed(buttonname --[[ string ]])
```

```lua
local retval --[[ boolean ]] = input.button_just_pressed(buttonid --[[ integer ]])
```
{% endtab %}

{% tab title="Example" %}
**Using a button name:**

```lua
if input.button_just_pressed("BUTTON_SOUTH") then

    print("'A' button has just been pressed on your controller")
end
```

**Using a button id:**

```lua
if input.button_just_pressed(0) then

    print("'A' button has just been pressed on your controller")
end
```
{% endtab %}
{% endtabs %}
