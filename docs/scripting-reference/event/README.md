# event

Events handler is a powerful way of calling function from other LUA resources, add a listener to an existant internal events, useful for handling game loop/game logic or trigger an event on server.

Internal client events list:

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
