# iTerm2

[iTerm2](http://www.iterm2.com/) is an open source replacement for Apple's Terminal. It's highly customizable and comes with a lot of useful features.

## Installation

You can get the app from [iTerm2 downloads page](http://www.iterm2.com/downloads.html). Once downloaded, drag and drop the **iTerm** application file into your **Applications** folder.

> **Note**: Instead of downloading and installing iTerm2 manually, you can use [Homebrew](http://sourabhbajaj.com/mac-setup/Homebrew/) `brew cask install iterm2`

## Customization

### Colors and Font Settings

Here are some suggested settings you can change or set, **they are all optional**.

* Set hot-key to open and close the terminal to `command + option + i`
* Go to profiles -&gt; Default -&gt; Terminal -&gt; Check silence bell to disable the terminal session from making any sound
* Download [one of iTerm2 color schemes](https://github.com/mbadolato/iTerm2-Color-Schemes/tree/master/schemes) and then set these to your default profile colors
* Change the cursor text and cursor color to yellow make it more visible
* Change the font to 14pt Source Code Pro Lite. Source Code Pro can be downloaded from [project's github repository](https://github.com/adobe-fonts/source-code-pro/releases/latest).

  > **Note**: Instead of downloading and installing Source Code Pro manually, you can use [Homebrew](https://sourabhbajaj.com/mac-setup/Homebrew/) `brew tap caskroom/fonts && brew cask install font-source-code-pro`

* If you're using BASH instead of ZSH you can add `export CLICOLOR=1` line to your `~/.bash_profile` file for nice coloring of listings

### Addons

Floating window : https://stackoverflow.com/a/44109348/4349318

### MacOS shortcuts

{% embed url="https://ursooperduper.github.io/cheatsheets/iterm/" %}

You might be familiar with shortcuts to skip a word \(⌥\) or go to start/end of the line \(⌘\). iTerm is could note be set up to work with any shortcuts by default but here's how you set them up:

open up iTerm2 preferences \(⌘,\) -&gt; Profiles -&gt; Keys -&gt; Click on + icon \(add new Keyboard shortcut\).

