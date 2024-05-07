# 💬 Chat

## Server

### register\_command

```lua
chat.register_command(_name, _handler)
```

Example:

```lua
chat.register_command("test", function(_client_id, _args)

    print("Command 'test' has been called by " .._client_id.. " with args ".._args)
end)
```
