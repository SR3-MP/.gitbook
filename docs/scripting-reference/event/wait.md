# wait

<mark style="color:purple;">**`Client`**</mark> <mark style="color:purple;">**`Server`**</mark>

Used to wait/yield the current event handler. (In milliseconds)

{% tabs %}
{% tab title="Definition" %}
```lua
event.wait(ms --[[ integer ]])
```
{% endtab %}

{% tab title="Example" %}
```lua
event.wait(1000) -- Wait for 1 sec.
```
{% endtab %}
{% endtabs %}

{% hint style="danger" %}
This cannot be used only to wait an event running on a per frame logic. Currently only **core:on\_gameplay\_render** and **core:on\_gameplay\_simulate** can be waited using this function.
{% endhint %}
