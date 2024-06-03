# add\_handler

<mark style="color:purple;">**`Client`**</mark> <mark style="color:purple;">**`Server`**</mark>

Add an handler function to a specific event.

{% tabs %}
{% tab title="Definition" %}
```lua
event.add_handler(name --[[ string ]], handler -- [[ func ]])
```
{% endtab %}

{% tab title="Example" %}
<pre class="language-lua"><code class="lang-lua"><strong>event.register("myresource:say_msg")
</strong><strong>event.add_handler("myresource:say_msg", function(msg)
</strong>
    print("Msg: "..msg)
end)
</code></pre>
{% endtab %}
{% endtabs %}

{% hint style="info" %}
You need to register an event at least once to be able to add an handler. Calling [register](register.md) function multiples time will simply do nothing if the event is already registered.
{% endhint %}
