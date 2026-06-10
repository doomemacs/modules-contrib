# Doom Emacs Community Modules

![Latest release](https://img.shields.io/github/tag/doomemacs/modules-contrib.svg?style=flat-square&label=release&color=58839b)
![Minimum supported version of Doom](https://img.shields.io/badge/Doom-v2.2.0+-blue.svg?style=flat-square)
![Minimum supported versions of Emacs](https://img.shields.io/badge/Emacs-v29.1+-blueviolet.svg?style=flat-square&logo=GNU%20Emacs&logoColor=white) &nbsp; 
[![Discord Server](https://img.shields.io/discord/406534637242810369?color=738adb&label=Discord&logo=discord&logoColor=white&style=flat-square)](https://doomemacs.org/discord)
[![Github Discussions](https://img.shields.io/github/discussions/doomemacs/community?style=flat-square&color=9cf&label=Discuss&logo=Github)](https://doomemacs.org/discuss)

</div>

This repository houses modules for [Doom Emacs](https://doomemacs.org) submitted
and maintained by its community, and seconds as a staging ground for official
modules. Unlike [Doom's official module
library](https://git.doomemacs.org/modules), the criteria here is more relaxed
and subject to less quality control by Doom's author, less cohesion with the
official modules, but in exchange may support a broader range of features and
use-cases.

> [!IMPORTANT]
> Each module possesses their own documentation, accessible within Doom via `M-x
> doom/help-modules` (or `M-x +lookup/documentation` while your cursor is on a
> module's name in `$DOOMDIR/init.el`).


# Install

Doom core v3.0 is not released yet, so this module library must be cloned and
activated manually.

1.  Clone this repository locally:
    
    ```sh
    $ cd ~/.config/doom   # assuming your $DOOMDIR lives here
    $ mkdir -p sources
    $ git clone https://github.com/doomemacs/modules-contrib sources/doom++
    ```

2.  Add the path to its `modules/` sub-directory to `doom-modules-load-path` in
    `$DOOMDIR/init.el`:
    
    ```elisp
    ;;; in $DOOMDIR/init.el
    (add-to-list 'doom-module-load-path (expand-file-name "sources/doom++/modules" doom-user-dir) t)
    ```
    
    NOTE: Order dictates priority in `doom-module-load-path`.

3.  Activate modules contained in this library like normal. For example, to
    enable a (hypothetical) `:editor meow` module:
    
    ```elisp
    (doom! ...
           :editor
           meow
           ...)
    ```

4.  Run `$ doom sync` and restart Emacs.


# Update

`doom upgrade` will not currently update your module library, so it must be
pulled manually before hand:

```sh
$ git pull -C ~/.config/doom/sources/doom++
$ doom upgrade
```
