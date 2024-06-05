# joy\_get\_value

<mark style="color:purple;">**`Client`**</mark>

Return the current axis values of a stick. (Values are between -1 to 1)

{% tabs %}
{% tab title="Definition" %}
```lua
local retval --[[ vector2 ]] = input.joy_get_value(joyid --[[ integer ]])
```
{% endtab %}

{% tab title="Example" %}
```lua
local value = input.joy_get_value(0)

-- Printing the X and Y axis of the left stick.
print(value.x)
print(value.y)
```
{% endtab %}
{% endtabs %}

{% hint style="info" %}
`joyid`parameter can take 2 different values:\
0 = Left Stick

1 = Right Stick
{% endhint %}
