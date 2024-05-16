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

    print("F2 key has just been pressed!")
end
```

***

### <mark style="color:purple;">key\_just\_released</mark>

Check if a specific input has just been released.

```lua
input.key_just_released(keyname --[[ string ]])
```

| Name    | Type   | Description         |
| ------- | ------ | ------------------- |
| keyname | string | A specific key name |

Example:

```lua
if input.key_just_released("F2") then

    print("F2 key has been released!")
end
```

***
