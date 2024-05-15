# ⌨️ Input

### <mark style="color:purple;">key\_just\_pressed</mark>

Check if an input has been pressed once.

```lua
input.key_just_pressed(keyname --[[ string ]])
```

| Name    | Type   | Description         |
| ------- | ------ | ------------------- |
| keyname | string | A specific key name |

Example:

```lua
if input.key_just_pressed("F2") then

    print("Hello world!")
end
```

***
