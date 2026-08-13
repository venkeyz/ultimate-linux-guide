---
title: RPC
icon: brand-discord
order: -6
---
There are two methods of getting RPC onto Steam Hardware,

* [The Decky Plugin](https://github.com/andrewburgess/steamdeck-discord-status) which requires Discord opened
* [Steam Presence](https://github.com/JustTemmie/steam-presence) which uses Steam's API to get now playing data and can be ran on another pc

<details>
<summary>Decky Plugin (easier to setup)</summary>

You can install the Decky Plugin by having [Decky Loader](https://decky.xyz/) installed and installing it from the plugin store.

</details>

<details>
<summary>Steam Presence</summary>

> [!IMPORTANT]
> You wil need a Steam Account that is verifed (spent 5 USD/EUR, not sure about others)

You can get Steam Presence via [this GitHub repo](https://github.com/JustTemmie/steam-presence)

The installation steps depends on your OS

<details>
<summary>Windows</summary>

> [!IMPORTANT]
> You will need atleast Python 3.8

Open a Terminal/Powershell window (i've only tested this in powershell but it should work on command prompt) and git clone the steam presence repo with
```powershell
git clone https://github.com/JustTemmie/steam-presence
cd steam-presence
```

Once in there, create a config.json file and put one of these examples into it
<details>
<summary>Minimal</summary>

```json
{
    "STEAM_API_KEY": "STEAM_API_KEY",
    "USER_IDS": "USER_ID"
}
```

</details>

<details>
<summary>Full Features</summary>

```json
{
    "STEAM_API_KEY": "STEAM_API_KEY",
    "USER_IDS": "USER_ID",

    "DISCORD_APPLICATION_ID": "869994714093465680",

    "FETCH_STEAM_RICH_PRESENCE": true,
    "FETCH_STEAM_REVIEWS": false,
    "ADD_STEAM_STORE_BUTTON": false,

    "WEB_SCRAPE": false,
    
    "COVER_ART": {
        "STEAM_GRID_DB": {
            "ENABLED": false,
            "STEAM_GRID_API_KEY": "STEAM_GRID_API_KEY"
        },
        "USE_STEAM_STORE_FALLBACK": true
    },

    "LOCAL_GAMES": {
      "ENABLED": false,
      "LOCAL_DISCORD_APPLICATION_ID": "1062648118375616594",
      "GAMES": [
          "processName1",
          "processName2",
          "processName3",
          "so on"
      ]
    },

    "GAME_OVERWRITE": {
        "ENABLED": false,
        "NAME": "Breath of the wild, now on steam!",
        "SECONDS_SINCE_START": 0
    },

    "CUSTOM_ICON": {
        "ENABLED": false,
        "URL": "https://raw.githubusercontent.com/JustTemmie/steam-presence/main/readmeimages/defaulticon.png",
        "TEXT": "Steam Presence on Discord"
    },

    "BLACKLIST": [
    	"game1",
    	"game2",
    	"game3"
    ],

    "WHITELIST": []
}
```

</details>

No matter which one you use you will need an API key. You can get one from https://steamcommunity.com/dev/apikey

more soon

</details>

<details>
<summary>MacOS</summary>

> [!IMPORTANT]
> You will need atleast Python 3.8

macos can be done via the linux guide, if anything different comes i'll update this section

</details>

<details>
<summary>Linux</summary>

> [!WARNING]
> Running this on the Steam Deck requires Discord opened which causes battery life to be halved

> [!IMPORTANT]
> You will need atleast Python 3.8

<details>
<summary>NixOS Users</summary>

this repo contains a nix flake but i dont know how to do anything with that so you can just follow https://github.com/JustTemmie/steam-presence#nixnixos

</details>

Linux users can install Steam Presence by using one of these steps

<details>
<summary>Automatic</summary>

```bash
git clone https://github.com/JustTemmie/steam-presence
cd steam-presence
./installer.sh
```

i dont really know how this works if anyone finds out please make a pull request

</details>

<details>
<summary>Manual</summary>

pretty sure you can follow the normal windows instructions

</summary>