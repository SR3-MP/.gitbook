# trigger

<mark style="color:purple;">**`Client`**</mark> <mark style="color:purple;">**`Server`**</mark>

Trigger a specific event using it's name.

{% tabs %}
{% tab title="Definition" %}
<pre class="language-lua"><code class="lang-lua"><strong>event.trigger(name --[[ string ]], ...)
</strong></code></pre>
{% endtab %}

{% tab title="Example" %}
```lua
event.trigger("myresource:say_msg", "Hello world !")
```
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
