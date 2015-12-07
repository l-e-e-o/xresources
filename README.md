# Xresources config
This is my .Xresources configuration.  The main purpose for this repository is for me to manage changes to my config files, but if you like it, feel free to use it.

##### Included configuratons

* urxvt

## Structure

I am using seperate config files for different applications wich are stored in the `.Xresources.d` directory and follow the scheme 

* `<application>.conf` for general configuration
* `<application>.color` for colorscheme definitions

The `.color` files are `#include`d in the `.config` files, which are `#include`d in a main `.Xresources` file.  That way you can quickly enable and disable single configurations.

## "Installation"

Clone this repository and link the `.Xresources` file and the `.Xresources.d` directory to your home folder.

```
git clone https://github.com/darkblinded/xresources.git 
ln -S xresources/xresources ~/.Xresources
ln -S xresources/xresources.d ~/.Xresources.d
```

Now you just have to set the X resources by

```
xrdb --merge ~/.Xresources
```

You may want to add this line to a autostart script so you won't need to run it manually every time the X server is restarted.

## Features

Short, possibly incomplete summary of the config's features

### urxvt

* C-Arrowkeys working
* Pseudo-transparency
* Powerline-enabled font (you may want to install [Inconsolata for Powerline](https://github.com/powerline/fonts/tree/master/Inconsolata))
* Colored manpages
* Solarizd colorscheme
