# 🕢 Event

## Client

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

<pre class="language-lua"><code class="lang-lua"><strong>event.call(name --[[ string ]])
</strong></code></pre>

| Name | Type   | Description |
| ---- | ------ | ----------- |
| name | string | Event name  |

Example:

```lua
event.call("myresource:say_msg")
-- NOTE: If no registered event with this name exist, it will simply do nothing.
```

***
