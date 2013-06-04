marathon
========

**marathon** is a minimal bash based launcher for Linux that tries to be smart about running or focusing apps. Just call `marathon SomeApplication`, and:

* if *SomeApplication* is not running, marathon will **run** it
* else marathon will just **focus** it

That way, after binding your favorite apps to a few easily-accessible keyboard shortcuts, you can access them with a single keypress and forget about alt-tabbing or clicking on stuff in your dock / selector.

Installation
------------

- **Mac OSX is not supported, sorry**. But rejoice, you'll be well served with Automator or Alfred, see [this guide](http://superuser.com/questions/245711/starting-application-with-custom-keyboard-shortcut) for example.  

- **Linux**:
    1. Install `wmctrl` from your package manager.
    2. Drop the script somewhere (e.g. `~/.scripts/marathon`) and link it to somewhere in your `$PATH`, e.g. `sudo ln -s ~/.scripts/marathon /usr/local/sbin/marathon`
    3. Bind `marathon command` to some keyboard shortcut:
        * GNOME → System Settings → *Keyboard* section → *Shortcut* tab → *Custom Shortcuts*. Mine look like:  
        ![GNOME Keyboard Settings screenshot](gnome-keyboard-settings-screenshot.png)
        * LXDE → your `lxde-rc.xml`

Todo
----

[Bug Reports](https://github.com/ronjouch/marathon/issues) and [Pull Requests](https://github.com/ronjouch/marathon/pulls) are welcome via GitHub. Help very much needed especially in these areas:

* Test and fix for other *nixes (currently only tested under Ubuntu).
* Proper handling of WM_CLASSES, currently it just assumes the class will contain the executable name. Works for all my apps though.
* (Maybe) use xdotool, it looks simpler.
* (Maybe) if app runs and focused, then minimize it.

License and contact
-------------------

Licensed under the BSD license, 2012-2013, [ronan@jouchet.fr](mailto:ronan@jouchet.fr) / [@ronjouch](https://twitter.com/ronjouch)