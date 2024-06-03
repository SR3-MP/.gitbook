# Chat

### <mark style="color:purple;">register\_command</mark>

Register a command on the server, connected players will be able to call it from the chat box.

{% code fullWidth="false" %}
```lua
chat.register_command(name --[[ string ]], handler --[[ func ]])
```
{% endcode %}

Example:

{% code fullWidth="false" %}
```lua
chat.register_command("test", function(src, args)

    -- This message is showing in the server console.
    print("Command 'test' has been called by " ..src.. " with args "..args)
end)
```
{% endcode %}

***

### <mark style="color:purple;">send\_message</mark>

Send a message to a specific player.

```lua
chat.send_message(src --[[ integer ]], msg --[[ string ]])
```

Example:

```lua
chat.register_command("test", function(src, args)

    -- This message is showing on the client chatbox.
    chat.send_message(src, "Command 'test' has been sent back to src player !")
end)
```

***

### <mark style="color:purple;">broadcast\_message</mark>

Send a message to all connected players.

```lua
chat.broadcast_message(msg --[[ string ]])
```

Example:

```lua
chat.register_command("test", function(src, args)

    -- This message is showing on all the clients chatbox.
    chat.broadcast_message("Command 'test' has been sent to all connected players !")
end)
```

***
