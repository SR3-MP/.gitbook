# Input

To use the functions below, you will need to know about the corresponding **keycodes**/**keynames**. A list is available [here](../../game-reference/key-codes.md).

{% hint style="info" %}
Most functions below comport two different definitions, one taking a **keyname**, and an other taking a **keycode**, use the one that suit your need.
{% endhint %}

### <mark style="color:purple;">key\_down</mark>

Check if an input is currently pressed.

```lua
input.key_down(keyname --[[ string ]])
input.key_down(keycode --[[ integer ]])
```

Example:

```lua
-- Using a keyname
if input.key_down("F2") then

    print("F2 is currently pressed!")
end

-- Using a keycode
if input.key_down(60) then

    print("F2 is currently pressed!")
end
```

***

### <mark style="color:purple;">key\_just\_pressed</mark>

Check if an input has just been pressed once.

```lua
input.key_just_pressed(keyname --[[ string ]])
input.key_just_pressed(keycode --[[ integer ]])
```

Example:

```lua
-- Using a keyname
if input.key_just_pressed("F2") then

    print("F2 key has just been pressed!")
end

-- Using a keycode
if input.key_just_pressed(60) then

    print("F2 key has just been pressed!")
end
```

***

### <mark style="color:purple;">key\_just\_released</mark>

Check if a specific input has just been released.

```lua
input.key_just_released(keyname --[[ string ]])
input.key_just_released(keycode --[[ integer ]])
```

Example:

```lua
-- Using a keyname
if input.key_just_released("F2") then

    print("F2 key has been released!")
end

-- Using a keycode
if input.key_just_released(60) then

    print("F2 key has been released!")
end
```

***

### <mark style="color:purple;">key\_disable</mark>

Disable a specific key.

```lua
input.key_disable(keyname --[[ string ]])
input.key_disable(keycode --[[ integer ]])
```

Example:

```lua
-- Using a keyname
input.key_disable("F2")

-- Using a keycode
input.key_disable(60)
```

***

### <mark style="color:purple;">key\_enable</mark>

Enable (or re-enable) a specific key.

```lua
input.key_enable(keyname --[[ string ]])
input.key_enable(keycode --[[ integer ]])
```

Example:

```lua
-- Using a keyname
input.key_enable("F2")

-- Using a keycode
input.key_enable(60)
```

***
