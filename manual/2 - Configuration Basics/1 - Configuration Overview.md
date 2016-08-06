---
sitemap: false
---
Cuberite can be configured by editing various configuration files. Below is a list of all configuration files:

<dl>
	<dt>settings.ini</dt>
	<dd>
		The main configuration file, which contains server-wide configuration variables.
	</dd>
	<dt>webadmin.ini</dt>
	<dd>
		Allows you to tweak the web admin interface, which is available at <code>http://localhost:8080</code> or <code>http://&lt;Server IP address&gt;:8080</code> by default.
	</dd>
	<dt>&lt;World name&gt;/world.ini</dt>
	<dd>
		This file configures world-specific aspects. This is where you choose your game mode. See {{3.3 - GameMode}}.
		Note that each world has its own <code>world.ini</code> file, each stored in <code>&lt;World name&gt;/world.ini</code>.
	</dd>
	<dt>monsters.ini</dt>
	<dd>
		Allows you to tweak monster behaviour.
	</dd>
	<dt>motd.txt</dt>
	<dd>
		The Message of the Day, which is shown to players upon joining your server.
	</dd>
	<dt>crafting.txt, brewing.txt, furnace.txt</dt>
	<dd>
		These three files allow you to tweak crafting, brewing, and furnace recipes.
	</dd>
	<dt>plugins/...</dt>
	<dd>
		Many plugins have their own configuration files. For instance, the WorldEdit config is <code>plugins/WorldEdit/config.cfg</code>
	</dd>
	<dt>items.ini</dt>
	<dd>
		Edit item IDs. You probably shouldn't edit this file unless you know what you're doing.
	</dd>
</dl>

<aside class="infobox">
	In all <code>.ini</code> files, lines starting with <code>;</code> are comments, and in all <code>.txt</code> files, lines starting with <code>#</code> are comments.
</aside>

#### Permissions
Permissions allow different players to access different commands and features. Each plugin has its own permissions. Setting up player permissions is most easily done via the web admin. You can also use the <code>rank &lt;playername&gt;</code> command from the server console. To see the command and permissions list for the default commands, which are provided by the Core plugin, see the [Core Plugin readme](https://github.com/cuberite/Core/blob/master/README.md).
