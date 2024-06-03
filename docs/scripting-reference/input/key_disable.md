# key\_disable

Disable a specific key.

{% tabs %}
{% tab title="Definition" %}
```lua
input.key_disable(keyname --[[ string ]])
```

```lua
input.key_disable(keycode --[[ integer ]])
```
{% endtab %}

{% tab title="Example" %}
**Using a keyname:**

```lua
input.key_disable("F2")
```

**Using a keycode:**

```lua
input.key_disable(60)
```
{% endtab %}
{% endtabs %}

{% hint style="warning" %}
This function doesn't need to be called every frame.
{% endhint %}
