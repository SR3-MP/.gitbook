# trigger\_on\_client

<mark style="color:purple;">**`Server`**</mark>

Trigger a specific event registered on the client from the server.

{% tabs %}
{% tab title="Definition" %}
```lua
event.trigger_on_client(name --[[ string ]], client --[[ integer ]], ...)
```
{% endtab %}

{% tab title="Example" %}
**Server**

<pre class="language-lua"><code class="lang-lua">-- We're sending "Hello World !" to the every connected clients.
<strong>event.trigger_on_client("myresource:say_msg", -1, "Hello world !")
</strong></code></pre>

**Client**

<pre class="language-lua"><code class="lang-lua"><strong>event.register("myresource:say_msg")
</strong><strong>event.add_handler("myresource:say_msg", function(_msg)
</strong><strong>
</strong><strong>    print(_msg) -- "Hello world !" will be printed in the client console.
</strong><strong>end)
</strong></code></pre>
{% endtab %}
{% endtabs %}

{% hint style="warning" %}
You can only trigger events registered in your own LUA scripts/resources, internal events starting with **"core:"** cannot be called from script.
{% endhint %}

{% hint style="info" %}
You can pass optional parameters, and later use them in function handler(s).

The second parameter is always the client id you want to send the event, if passed **-1** it will be trigger on every clients.
{% endhint %}

{% hint style="warning" %}
Currently only data of type **integer**, **number**, **boolean** and **string** can be passed as parameters. If you want to pass more complexe data (like a table), it's recommended passing data as a **JSON** string.
{% endhint %}
