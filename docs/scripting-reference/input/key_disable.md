# key\_disable

<mark style="color:purple;">**`Client`**</mark>

Disable/enable a specific key.

{% tabs %}
{% tab title="Definition" %}
```lua
input.key_disable(keyname --[[ string ]], disabled --[[ boolean ]])
```

```lua
input.key_disable(keycode --[[ integer ]], disabled --[[ boolean ]])
```
{% endtab %}

{% tab title="Example" %}
**Using a keyname:**

```lua
input.key_disable("F2", true)
```

**Using a keycode:**

```lua
input.key_disable(60, true)
```
{% endtab %}
{% endtabs %}

{% hint style="warning" %}
This function doesn't need to be called every frame.
{% endhint %}
