# key\_just\_pressed

<mark style="color:purple;">**`Client`**</mark>

Check if an input has just been pressed once.

{% tabs %}
{% tab title="Definition" %}
<pre class="language-lua"><code class="lang-lua"><strong>input.key_just_pressed(keyname --[[ string ]])
</strong></code></pre>

```lua
input.key_just_pressed(keycode --[[ integer ]])
```
{% endtab %}

{% tab title="Example" %}
**Using a keyname:**

```lua
if input.key_just_pressed("F2") then

    print("F2 has just been pressed!")
end
```

**Using a keycode:**

```lua
if input.key_just_pressed(60) then

    print("F2 has just been pressed!")
end
```
{% endtab %}
{% endtabs %}

{% hint style="info" %}
Key codes/names list available [here](../../game-reference/key-codes.md).
{% endhint %}
