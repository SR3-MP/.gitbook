# key\_down

<mark style="color:purple;">**`Client`**</mark>

Check if an input is currently pressed.

{% tabs %}
{% tab title="Definition" %}
```lua
input.key_down(keyname --[[ string ]])
```

```lua
input.key_down(keycode --[[ integer ]])
```
{% endtab %}

{% tab title="Example" %}
**Using a keyname:**

```lua
if input.key_down("F2") then

    print("F2 is currently pressed!")
end
```

**Using a keycode:**

```lua
if input.key_down(60) then

    print("F2 is currently pressed!")
end
```
{% endtab %}
{% endtabs %}

{% hint style="info" %}
Key codes/names list available [here](../../game-reference/key-codes.md).
{% endhint %}
