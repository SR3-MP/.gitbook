# button\_get\_value

<mark style="color:purple;">**`Client`**</mark>

Return how much a button is pressed, useful to return the pressed amount of left or right trigger as an example. In the case of a "standard" button, it's recommended to use this functions instead:

* [button\_is\_pressed](button\_is\_pressed.md)
* [button\_just\_pressed](button\_just\_pressed.md)

{% tabs %}
{% tab title="Definition" %}
```lua
local retval --[[ number ]] = input.button_get_value(buttonname --[[ string ]])
```

```lua
local retval --[[ number ]] = input.button_get_value(buttonid --[[ integer ]])
```
{% endtab %}

{% tab title="Example" %}
**Using a button name:**

```lua
local value = input.button_get_value("LEFT_TRIGGER")

-- Value will be between 0 and 1.
print(value)
```

**Using a button id:**

```lua
local value = input.button_get_value(6)

-- Value will be between 0 and 1.
print(value)
```
{% endtab %}
{% endtabs %}
