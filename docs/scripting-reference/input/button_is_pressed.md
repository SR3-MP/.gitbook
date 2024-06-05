# button\_is\_pressed

<mark style="color:purple;">**`Client`**</mark>

Return true or false when a specific button is currently pressed on a controller.

{% tabs %}
{% tab title="Definition" %}
```lua
local retval --[[ boolean ]] = input.button_is_pressed(buttonname --[[ string ]])
```

```lua
local retval --[[ boolean ]] = input.button_is_pressed(buttonid --[[ integer ]])
```
{% endtab %}

{% tab title="Example" %}
**Using a button name:**

```lua
if input.button_is_pressed("BUTTON_SOUTH") then

    print("You're currently pressing 'A' button on your controller")
end
```

**Using a button id:**

```lua
if input.button_is_pressed(0) then

    print("You're currently pressing 'A' button on your controller")
end
```
{% endtab %}
{% endtabs %}
