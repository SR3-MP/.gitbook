# controller\_is\_connected

<mark style="color:purple;">**`Client`**</mark>

Return true if a controller is connected, false otherwise.

{% tabs %}
{% tab title="Definition" %}
```lua
local retval --[[ boolean ]] = input.controller_is_connected()
```
{% endtab %}

{% tab title="Example" %}
```lua
if input.controller_is_connected() then

    -- Do something with the controller axis/buttons...
end
```
{% endtab %}
{% endtabs %}
