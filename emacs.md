# Emacs

[Emacs](https://www.gnu.org/software/emacs/) is a family of text editors that are characterized by their extensibility. The manual for the most widely used variant, GNU Emacs, describes it as the extensible, customizable, self-documenting, real-time display editor.

Development of the first Emacs began in the mid-1970s, and work on its direct descendant, GNU Emacs, continues actively as of 2017.

### TLDR: 

```text
brew install emacs --with-cocoa --with-gnutls --with-rsvg --with-imagemagick
cd ~ && mv .emacs.d .emacs.d.bak && mv .emacs .emacs.bak
git clone https://github.com/syl20bnr/spacemacs ~/.emacs.d
emacs --insecure
```

## Installation

There are many Emacs clients on macOS. The recommended version on macOS is Emacs Mac Port, but others are good as well.

### [Emacs Mac port](https://bitbucket.org/mituharu/emacs-mac/overview) \(Recommended\)

Many useful features are built with Emacs Mac Port, e.g. environment variables, full screen, visual enhancements and so on.

Link the Homebrew tap first.

```text
brew tap railwaycat/emacsmacport
```

* Method 1: Install with `brew cask`.

  ```text
  brew cask install emacs-mac
  ```

  There are three available versions, `emacs-mac`, `emacs-mac-official-icon`, `emacs-mac-spacemacs-icon`.

* Method 2: Build from source with Homebrew.

  ```text
  brew install emacs-mac [options]
  brew linkapps emacs-mac
  ```

Click here to see available options: 1. `--with-dbus`, Build with d-bus support  
 2. `--with-modules`, Build with dynamic modules support  
 3. `--with-xml2`, Build with libxml2 support  
 4. `--with-ctags`, Don't remove the ctags executable that emacs provides  
 5. `--with-no-title-bars`, Build with a patch for no title bars on frames \(--HEAD is not supported\)  
 6. `--with-natural-title-bar`, Build with a patch for title bar color inferred by your theme \(--HEAD is not supported\). More info is provided [here](https://github.com/railwaycat/homebrew-emacsmacport/wiki/Natural-Title-Bar)  
 7. `--with-official-icon`, Using official Emacs icon  
 8. `--with-modern-icon`, Using a modern style Emacs icon by @tpanum  
 9. `--with-spacemacs-icon`, Using the spacemacs Emacs icon by Nasser Alshammari  
 10. `--with-icon-for-documents`, Using official icon for documents which default open with Emacs  


### [Emacs plus](https://github.com/d12frosted/homebrew-emacs-plus#emacs-plus)

```text
brew tap d12frosted/emacs-plus
brew install emacs-plus [options]
brew linkapps emacs-plus
```

Click here to see available options: 1. `--with-24bit-color`: Experimental: build with 24 bit color support  
 2. `--with-ctags`: Don't remove the ctags executable that Emacs provides  
 3. `--with-dbus`: Build with dbus support  
 4. `--with-mailutils`: Build with mailutils support  
 5. `--with-natural-title-bar`: Experimental: use a title bar colour inferred by your theme  
 6. `--with-no-title-bars`: Experimental: build with a patch for no title bars on frames \(--HEAD has this built-in via undecorated flag\)  
 7. `--with-x11`: Experimental: build with x11 support  
 8. `--without-cocoa`: Build a non-Cocoa version of Emacs  
 9. `--without-gnutls`: Build without gnutls support  
 10. `--without-imagemagick@6`: Build without imagemagick@6 support  
 11. `--without-librsvg`: Build without librsvg support  
 12. `--without-libxml2`: Build without libxml2 support  
 13. `--without-modules`: Build without dynamic modules support  
 14. `--without-multicolor-fonts`: Build without a patch that enables multicolor font support  
 15. `--without-spacemacs-icon`: Build without Spacemacs icon by Nasser Alshammari  
 16. `--HEAD`: Install HEAD version  


> **Note**: You might want to install [exec-path-from-shell](https://github.com/purcell/exec-path-from-shell) if you are using Emacs plus. It takes care of your environment variables.
>
> **Note**: to have the title bar match your theme background color, consider using instead: `brew install emacs-plus --HEAD --with-natural-title-bars`

## Spacemacs

[Spacemacs](https://github.com/syl20bnr/spacemacs/blob/master/README.md) is a new way to experience Emacs -- a sophisticated and polished set-up focused on ergonomics, mnemonics and consistency.

Spacemacs can be used naturally by both Emacs and Vim users -- you can even mix the two editing styles. Switching easily between input styles makes Spacemacs a great tool for pair-programming.

### Installation

1. If you have an existing Emacs configuration, back it up first:

   ```bash
   cd ~
   mv .emacs.d .emacs.d.bak
   mv .emacs .emacs.bak
   ```

   Don't forget to backup and _remove_ `~/.emacs` file otherwise Spacemacs **WILL NOT** load since that file prevents Emacs from loading the proper initialization file.

2. Clone the repository:

   ```bash
   git clone https://github.com/syl20bnr/spacemacs ~/.emacs.d
   ```

   `master` is the stable branch and it is _immutable_, **DO NOT** make any modification to it or you will break the update mechanism. If you want to fork Spacemacs safely use the `develop` branch where you handle the update manually.

3. \(Optional\) Install the [Source Code Pro](https://github.com/adobe-fonts/source-code-pro) font.

   If you are running in terminal you'll also need to change font settings of your terminal.

4. Launch Emacs. Spacemacs will automatically install the packages it requires. If you get an error regarding package downloads then you may try to disable the HTTPS protocol by starting Emacs with

   ```bash
   emacs --insecure
   ```

   Or you can set the `dotspacemacs-elpa-https` to `nil` in your dotfile to remove the need to start Emacs with `--insecure` argument. You may wish to clear out your `.emacs.d/elpa` directory before doing this, so that any corrupted packages you may have downloaded will be re-installed.

5. Restart Emacs to complete the installation.

## Purcell's Emacs configuration

This is [Purcell's](https://github.com/purcell/emacs.d) emacs configuration tree, continually used and tweaked since 2000, and it may be a good starting point for other Emacs users, especially those who are web developers. These days it's somewhat geared towards macOS, but it is known to also work on Linux and Windows.

### Installation

To install, clone this repository to `~/.emacs.d`, i.e. ensure that the `init.el` contained in this repository ends up at `~/.emacs.d/init.el`:

```text
git clone https://github.com/purcell/emacs.d.git ~/.emacs.d
```

Upon starting up Emacs for the first time, further third-party packages will be automatically downloaded and installed. If you encounter any errors at that stage, try restarting Emacs, and possibly running `M-x package-refresh-contents` before doing so.

## Doom Emacs

[Doom](https://github.com/hlissner/doom-emacs) is a configuration for GNU Emacs written by a stubborn, shell-dwelling, and melodramatic ex-vimmer. It wasn't originally intended for public use, but can be considered a hacker's starter kit.

### Installation

```text
git clone https://github.com/hlissner/doom-emacs ~/.emacs.d
cd ~/.emacs.d
cp init.example.el init.el  # maybe edit init.el
make install
```

Don't forget to run `make` every time you modify `init.el`!

Visit the wiki for [a more detailed guide on installing, customizing and grokking Doom](https://github.com/hlissner/doom-emacs/wiki).

