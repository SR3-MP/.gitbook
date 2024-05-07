# 💬 Chat

## Server

### <mark style="color:purple;">register\_command</mark>

{% code fullWidth="false" %}
```lua
chat.register_command(_name, _handler)
```
{% endcode %}

Example:

{% code fullWidth="false" %}
```lua
chat.register_command("test", function(_client_id, _args)

    -- This message is showing in the server console.
    print("Command 'test' has been called by " .._client_id.. " with args ".._args)
end)
```
{% endcode %}

### <mark style="color:purple;">send\_message</mark>

```lua
chat.send_message(_client_id, _str)
```

Example:

```lua
chat.register_command("test", function(_client_id, _args)

    -- This message is showing on the client chatbox.
    chat.send_message(_client_id, "Command 'test' has been sent back to src client !")
end)
```
