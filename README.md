> :warning: **Be aware that this repository is a work-in-progress.** Until Doom
> Emacs v3.0 is released, some links may be broken and documentation may reflect
> unreleased features and behavior.

<div align="center">

# Doom Emacs Community Modules

![Latest release](https://img.shields.io/github/tag/doomemacs/contrib-modules.svg?style=flat-square&label=release&color=58839b) ![Latest commit](https://img.shields.io/github/last-commit/doomemacs/contrib-modules/master?style=flat-square) ![Build status: master](https://img.shields.io/github/workflow/status/doomemacs/contrib-modules/CI/master?style=flat-square)

[Install](#install) • [Update](#update) • [Documentation] • [Changelog] • [Community]

</div>

# Introduction

This is a library of [Doom Emacs](https://doomemacs.org) modules submitted and
maintained by its community. Unlike [Doom's official module
library](https://git.doomemacs.org/modules), the criteria for these modules is
more relaxed and subject to fewer quality checks by Doom's author, but in
exchange cover a larger spectrum of features and use-cases.

Each module has their own documentation, accessible in Doom via `M-x
doom/help-modules` or online at https://docs.doomemacs.org/-/contrib-modules:

# Install

## Before Doom v3.0

1. Clone this repository locally:
   ```sh
   $ mkdir -p ~/.doom.d/repos/contrib-modules
   $ git clone https://github.com/doomemacs/contrib-modules ~/.doom.d/repos/contrib-modules
   ```

2. Add the path to its `modules/` directory to `doom-modules-load-path` in `$DOOMDIR/init.el`:
   ```emacs-lisp
   ;;; in $DOOMDIR/init.el
   (add-to-list 'doom-modules-load-path (expand-file-name "repos/contrib-modules/" doom-user-dir))
   ```

3. Activate modules contained in this library like normal. For example, to
   enable this library's `:editor meow` module:
   ```emacs-lisp
   (doom! ...
   
          :editor
          meow
          
          ...)
   ```

4. Run `$ doom sync` to ensure your changes take effect.

## After Doom v3.0

1. Register it as a module library from within your `doom!` block, like so:
   ```emacs-lisp
   ;;; in $DOOMDIR/init.el
   (doom! (modules :repo "doomemacs/contrib-modules")
          ...)
   ```

2. Activate modules contained in this library like normal. For example, to
   enable this library's `:editor meow` module:
   ```emacs-lisp
   (doom! (modules :repo "doomemacs/contrib-modules")
   
          :editor
          meow
          
          ...)
   ```
   
   If two libraries have the same module, the order of your `modules`
   declaration dictates precedence (from highest to lowest). The first matching
   module will be used.

3. Run `$ doom sync` to ensure your changes take effect. 


# Update

- Run `$ doom upgrade` to update Doom and your module libraries.
- Run `$ doom upgrade --modules` to only update your module libraries.
- Run `$ doom upgrade --modules doomemacs/contrib-modules` to update only one.

Module libraries can be pinned with `:pin "REF"`, where REF is a commit or a
version string (e.g. a partial version string: `v22.11` or full one:
`v22.11.02`).


# `TODO `Contribute


[Changelog]: https://docs.doomemacs.org/contrib-modules/changelog
[Community]: https://docs.doomemacs.org/-/community
[discord]: https://doomemacs.org/discord
[discourse]: https://discourse.doomemacs.org
[documentation]: https://docs.doomemacs.org/contrib-modules
