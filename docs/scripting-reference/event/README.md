# event

Events handler is a powerful way of calling function from other LUA resources, add a listener to an existant internal events, useful for handling game loop/game logic or trigger an event on server.

Internal events list:

<details>

<summary>core:on_gameplay_enter</summary>

Called right after you enter the game.

Example:

```lua
event.add_handler("core:on_gameplay_enter", function()

    print("You just spawned into the game !")
end)
```

</details>

<details>

<summary>core:on_gameplay_render</summary>

Called every frame (Mostly used to handle UI)

Example:

```lua
event.add_handler("core:on_gameplay_render", function()

    print("Called every frame !")
end)
```

</details>

<details>

<summary>core:on_gameplay_simulate</summary>

Called every frame (Mostly used to handle physics, entities spawning, ...)

Example:

```lua
event.add_handler("core:on_gameplay_simulate", function()

    -- WARNING: You cannot draw ui functions here !
    print("Called every frame !")
end)
```

</details>

***

### <mark style="color:purple;">trigger\_on\_server</mark>

Trigger a specific event registered on the server side.

{% hint style="warning" %}
You can only trigger events registered in your own LUA scripts/resources, internal events starting with **"core:"** cannot be called from script.
{% endhint %}

{% hint style="info" %}
You can pass optional parameters, and later use them in function handler(s).
{% endhint %}

{% hint style="warning" %}
Currently only data of type **integer**, **number**, **boolean** and **string** can be passed as parameters. If you want to pass more complexe data (like a table), it's recommended passing data as a JSON string.
{% endhint %}

```lua
event.trigger_on_server(name --[[ string ]], ...)
```

Example:

<pre class="language-lua"><code class="lang-lua"><strong>-- client.lua
</strong><strong>event.trigger_on_server("myresource:say_msg", "Hello world !") -- We're sending "Hello World !" to the server.
</strong><strong>
</strong><strong>-- server.lua
</strong><strong>event.register("myresource:say_msg")
</strong><strong>event.add_handler("myresource:say_msg", function(_msg)
</strong><strong>
</strong><strong>    print(_msg) -- "Hello world !" will be printed in the server console.
</strong><strong>end)
</strong></code></pre>
