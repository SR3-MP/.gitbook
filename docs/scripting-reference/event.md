# 🕢 Event

## Client

Events handler is a powerful way of calling function from external LUA scripts or simply add a listener to an existant internal events, useful for handling game loop/game logic.

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
</strong><strong>event.add_handler("myresource:say_msg", function(msg --[[ This parameter is not necessary if you don't pass any data in the event.call() method ]])
</strong>
    print("Msg: "..msg)
end)
</code></pre>

***

### <mark style="color:purple;">call</mark>

Call a specific event using it's name.

{% hint style="warning" %}
You can only call event registered in your LUA scripts, internal events starting with **core:** cannot be called from script.
{% endhint %}

{% hint style="info" %}
You can pass optional parameters, and later use them in function handler(s).
{% endhint %}

<pre class="language-lua"><code class="lang-lua"><strong>event.call(name --[[ string ]], ...)
</strong></code></pre>

| Name | Type   | Description |
| ---- | ------ | ----------- |
| name | string | Event name  |

Example:

```lua
event.call("myresource:say_msg", "Hello world !")
```

***
