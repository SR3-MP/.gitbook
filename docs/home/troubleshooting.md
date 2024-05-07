# 🧰 Troubleshooting

Below you will find a list of the common issues you can encounter when installing or using SR3MP.

## Why launching the mod is starting the vanilla game instead ?

It can be caused by multiple reasons, but the most common is probably because there are missing files in your installation.

First, try to reinstall SR3MP, if the problem persist, you can also try to disable your antivirus, sometimes Windows Defender or other antivirus can flag some files related to the mod, this is a false positive because antiviruses doesn't know about the files signature.

If the issue still persist, you can also try to install the mod manually, using the [manual download](https://sr3mp.net/index.php?page=download\&file=SR3MP-Release.rar).

## Why I'm experiencing a blackscreen when entering the main menu ?

It can be caused by your system choosing the wrong GPU, if you have an iGPU, in some cases Windows decide to use it instead of your dedicated graphics card. You can try to force the program to use your dedicated GPU.

Some topics about this issue can be found on the internet, if you don't know how to do that, it's recommended to join our [official discord server](https://discord.com/invite/QBQwQQbVFf), we will try our best to help you.

## Why the download speed is so slow during the installation ?

First, make sure this is not an issue on your side, check your internet, if your connection is correct and you keep experiencing slow download, it's probably because you're living in a distant region from the server, like **Canada** or **Australia**.

Our download server is located in **Europe**, so the speed quickly become really slow in other regions. Your best choice is to use the [manual download](https://sr3mp.net/index.php?page=download\&file=SR3MP-Release.rar).

## Why am I experiencing vehicles engine sound glitch/delay ?

This bug is an issue of the game itself, it's a known issue that we will eventually try to fix in the future, as we are speaking, it's not a priority during the Alpha stage of the mod.

As a workaround, you can fix this bug by going to the control panel of your GPU (**Nvidia Panel**, **AMD Adrenalin** or **Intel Arc Control Software**), and follow this step-by-step guide below:

{% tabs %}
{% tab title="Nvidia" %}
1. Open your **Nvidia Control Panel**
2. Go to **Manage 3D Settings**
3. Go to **Program Settings**
4. Select **Saints Row: The Third Remastered (SRTTR.exe)** executable
5. Scroll down until you see **Low Latency Mode**
6. Set it to **Ultra**
7. Restart your game
{% endtab %}

{% tab title="AMD" %}
Not available yet.
{% endtab %}

{% tab title="Intel" %}
Not available yet.
{% endtab %}
{% endtabs %}
