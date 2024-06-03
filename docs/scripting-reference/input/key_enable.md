# key\_enable

Enable (or re-enable) a specific key.

{% tabs %}
{% tab title="Definition" %}
```lua
input.key_enable(keyname --[[ string ]])
```

```lua
input.key_enable(keycode --[[ integer ]])
```
{% endtab %}

{% tab title="Example" %}
**Using a keyname:**

```lua
input.key_enable("F2")
```

**Using a keycode:**

```lua
input.key_enable(60)
```
{% endtab %}
{% endtabs %}

{% hint style="warning" %}
This function doesn't need to be called every frame.
{% endhint %}
