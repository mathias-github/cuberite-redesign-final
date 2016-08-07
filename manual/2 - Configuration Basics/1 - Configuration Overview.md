---
sitemap: false
---
Cuberite can be configured by editing various configuration files. Below is a list of all configuration files:

##### settings.ini
> The main configuration file, which contains server-wide configuration variables.

##### webadmin.ini
> Allows you to tweak the web admin interface, which is available at ***http://localhost:8080*** or ***http://<Server IP address>:8080*** by default.

##### <World name>/world.ini
> This file configures world-specific aspects. This is where you choose your game mode. See [GameMode](#gamemode). Note that each world has its own ***world.ini*** file, each stored in ***<World name>/world.ini***.

##### monsters.ini
> Allows you to tweak monster behaviour.

##### motd.txt
> The Message of the Day, which is shown to players upon joining your server.

##### crafting.txt, brewing.txt, furnace.txt
> These three files allow you to tweak crafting, brewing, and furnace recipes.

##### plugins/...
> Many plugins have their own configuration files. For instance, the WorldEdit config is ***plugins/WorldEdit/config.cfg***

##### items.ini
> Edit item IDs. You probably shouldn't edit this file unless you know what you're doing.

<aside class="infobox">
	In all ***.ini*** files, lines starting with ***;*** are comments, and in all ***.txt*** files, lines starting with ***#*** are comments.
</aside>

#### Permissions
Permissions allow different players to access different commands and features. Each plugin has its own permissions. Setting up player permissions is most easily done via the web admin. You can also use the ***rank <playername>*** command from the server console. To see the command and permissions list for the default commands, which are provided by the Core plugin, see the [Core Plugin readme](https://github.com/cuberite/Core/blob/master/README.md).
