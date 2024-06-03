# trigger\_on\_server

<mark style="color:purple;">**`Client`**</mark>

Trigger a specific event registered on the server from the client.

{% tabs %}
{% tab title="Definition" %}
```lua
event.trigger_on_server(name --[[ string ]], ...)
```
{% endtab %}

{% tab title="Example" %}
**Client**

<pre class="language-lua"><code class="lang-lua"><strong>event.trigger_on_server("myresource:say_msg", "Hello world !") -- We're sending "Hello World !" to the server.
</strong></code></pre>

**Server**

<pre class="language-lua"><code class="lang-lua"><strong>event.register("myresource:say_msg")
</strong><strong>event.add_handler("myresource:say_msg", function(_msg)
</strong><strong>
</strong><strong>    print(_msg) -- "Hello world !" will be printed in the server console.
</strong><strong>end)
</strong></code></pre>
{% endtab %}
{% endtabs %}

{% hint style="warning" %}
You can only trigger events registered in your own LUA scripts/resources, internal events starting with **"core:"** cannot be called from script.
{% endhint %}

{% hint style="info" %}
You can pass optional parameters, and later use them in function handler(s).
{% endhint %}

{% hint style="warning" %}
Currently only data of type **integer**, **number**, **boolean** and **string** can be passed as parameters. If you want to pass more complexe data (like a table), it's recommended passing data as a **JSON** string.
{% endhint %}
