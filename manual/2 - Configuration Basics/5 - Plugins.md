---
sitemap: false
---
Plugins are an important method of customisation for Cuberite. There are many different first and third-party plugins available.

Cubrite plugins are written in Lua, and interact with the server through an [extensive API](http://api-docs.cuberite.org/). They are designed to be easy to write for anyone with basic programming experience, so if existing plugins don't fill your need you can easily write your own plugins. If you want to learn how to write your own plugins, check out [the guide](http://api-docs.cuberite.org/Writing-a-Cuberite-plugin.html).

Cuberite has a [plugin repository](https://forum.cuberite.org/forum-2.html) where you can upload your plugins publicly and download plugins others have released.

#### Activating a plugin

After downloading a plugin, you need to put it in the ***Plugins/*** directory. You should then edit the ***[Plugins]*** sections of the ***settings.ini*** file and add a plugin entry there. Below is an example of adding a plugin called ***MyNewPlugin***.

```
[Plugins]  
Plugin=Core  
Plugin=TransApi  
Plugin=MyNewPlugin  
;Plugin=MyDisabledPlugin
```

#### Writing a plugin

To get started with writing Cuberite plugins, read this [article](http://api-docs.cuberite.org/Writing-a-Cuberite-plugin.html). Cuberite Plugins are written with the Lua programming language. Cuberite has a well-documented [API](http://api-docs.cuberite.org/).

#### You're good to go!

If you have read this far, you should now have enough knowledge to operate a Cuberite server. The rest of this book covers more features and further configuration options in greater depth.
