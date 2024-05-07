# 💬 Chat

## Server

### <mark style="color:purple;">register\_command</mark>

{% code fullWidth="false" %}
```lua
chat.register_command(name --[[ string ]], handler --[[ func ]])
```
{% endcode %}

| Name    | Type   | Description          |
| ------- | ------ | -------------------- |
| name    | string | Command name         |
| handler | func   | The function handler |

Example:

{% code fullWidth="false" %}
```lua
chat.register_command("test", function(src, args)

    -- This message is showing in the server console.
    print("Command 'test' has been called by " ..src.. " with args "..args)
end)
```
{% endcode %}

### <mark style="color:purple;">send\_message</mark>

```lua
chat.send_message(src --[[ integer ]], msg --[[ string ]])
```

| Name | Type    | Description      |
| ---- | ------- | ---------------- |
| src  | integer | Player source id |
| msg  | string  | Message to send  |

Example:

```lua
chat.register_command("test", function(src, args)

    -- This message is showing on the client chatbox.
    chat.send_message(src, "Command 'test' has been sent back to src client !")
end)
```
