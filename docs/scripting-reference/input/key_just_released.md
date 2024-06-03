# key\_just\_released

<mark style="color:purple;">**`Client`**</mark>

Check if an input has just been released.

{% tabs %}
{% tab title="Definition" %}
<pre class="language-lua"><code class="lang-lua"><strong>input.key_just_released(keyname --[[ string ]])
</strong></code></pre>

```lua
input.key_just_released(keycode --[[ integer ]])
```
{% endtab %}

{% tab title="Example" %}
**Using a keyname:**

```lua
if input.key_just_released("F2") then

    print("F2 has just been released!")
end
```

**Using a keycode:**

```lua
if input.key_just_released(60) then

    print("F2 has just been released!")
end
```
{% endtab %}
{% endtabs %}

{% hint style="info" %}
Key codes/names list available [here](../../game-reference/key-codes.md).
{% endhint %}
