# 🕢 Event

## Client

Events handler is a powerful way of calling stuff from other LUA scripts or simply add a listener to an existant internal events, useful for handling game loop/game logic.

A list of already existant events:

<table><thead><tr><th width="262">Name</th><th>Description</th></tr></thead><tbody><tr><td>core:on_gameplay_enter</td><td>Called right after you enter the game.</td></tr><tr><td>core:on_gameplay_render</td><td>Called every frame (Mostly used to handle UI)</td></tr><tr><td>core:on_gameplay_simulate</td><td>Called every frame (Mostly used to handle physics, entities spawning, ...)</td></tr></tbody></table>

### <mark style="color:purple;">register</mark>

Register an event, to be able to call it later using call function.

```lua
event.register(name --[[ string ]])
```

| Name | Type   | Description |
| ---- | ------ | ----------- |
| name | string | Event name  |

Example:

```lua
event.register("myresource:say_msg")
```

***

### <mark style="color:purple;">add\_handler</mark>

Add an handler function to a specific event.

```lua
event.add_handler(name --[[ string ]], handler -- [[ func ]])
```

| Name    | Type   | Description          |
| ------- | ------ | -------------------- |
| name    | string | Event name           |
| handler | func   | The function handler |

Example:

<pre class="language-lua"><code class="lang-lua"><strong>event.register("myresource:say_msg") -- NOTE: Only required if not already registered.
</strong><strong>event.add_handler("myresource:say_msg", function()
</strong>
    print("Hello world !")
end)
</code></pre>

***

### <mark style="color:purple;">call</mark>

Call a specific event using it's name.

{% hint style="warning" %}
You can only call event registered in your LUA scripts, internal events starting with **core:** cannot be called from script.
{% endhint %}

<pre class="language-lua"><code class="lang-lua"><strong>event.call(name --[[ string ]])
</strong></code></pre>

| Name | Type   | Description |
| ---- | ------ | ----------- |
| name | string | Event name  |

Example:

```lua
event.call("myresource:say_msg")
```

***
