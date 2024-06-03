# register

<mark style="color:purple;">**`Client`**</mark> <mark style="color:purple;">**`Server`**</mark>

Register an event, to be able to trigger it later using [trigger](register.md#trigger) function.

{% tabs %}
{% tab title="Definition" %}
```lua
event.register(name --[[ string ]])
```
{% endtab %}

{% tab title="Example" %}
```lua
event.register("myresource:say_msg")
```
{% endtab %}
{% endtabs %}

{% hint style="info" %}
Trying to register an event with the same name multiple times will simply do nothing.
{% endhint %}
