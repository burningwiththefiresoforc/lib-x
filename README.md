# Lib-x
![GitHub Issues or Pull Requests](https://img.shields.io/github/issues/Benex254/FastAnime)
![GitHub License](https://img.shields.io/github/license/Benex254/lib-x)
![GitHub file size in bytes](https://img.shields.io/github/size/Benex254/lib-x/lib-x)
![GitHub Release](https://img.shields.io/github/v/release/Benex254/lib-x)
![GitHub commit activity](https://img.shields.io/github/commit-activity/m/Benex254/lib-x)

A TUI wrapper over the calibredb

[lib-x-all.webm](https://github.com/user-attachments/assets/58690f9f-b239-4c84-9175-f17b8c6d2293)
# Fork Notes
- The aim of this fork is to optimize the script somewhat and fix some of the functionality that seemed broken. I have only tested this with rofi and fzf + kitty, Calibre 8.5, Debian 13. The original version of this script was limited by a very large number of jq and calibredb calls, but with preprocessing the main limitation will be library size. It is close to instantaneous navigating through a library of 600+ books on my old laptop after the initial loading phase.  
-If you're getting parse errors with jq, it may be because of the Wikidata plugin which prints some debug stuff into the calibredb outputs. Disabling it will not work, it either has to be removed or the line that prints "Urlfixer initialized" commented out in the urlfixer.py script within the plugin zip archive.

# Installation
![Linux/BSD](https://img.shields.io/badge/-Linux/BSD-red.svg?style=for-the-badge&logo=linux)
![Arch Linux](https://img.shields.io/badge/-Arch_Linux-black.svg?style=for-the-badge&logo=archlinux)
![MacOS](https://img.shields.io/badge/-MacOS-lightblue.svg?style=for-the-badge&logo=apple)

```bash
curl -sL https://raw.githubusercontent.com/Benexl/lib-x/refs/heads/master/lib-x -o ~/.local/bin/lib-x && chmod +x ~/.local/bin/lib-x
```

# Dependencies

**Required:**

- [calibre](https://calibre-ebook.com/) - for the database
- [jq](https://jqlang.github.io/jq/)- to pass the json data
- [fzf](https://github.com/junegunn/fzf) - for the main ui
  
**optional:**
- [yazi](https://github.com/charmbracelet/gum) - better file explorer
- [gum](https://github.com/charmbracelet/gum) - for an even better ui
- less
- dunst or some other notification daemon

# Usage

```bash
# launch the ui
lib-x 

# edit your config
lib-x -e

# search for a specific book with calibre search syntax
lib-x --search tag:programming
```

# Other Terminal Browsers I Made
[yt-x](https://github.com/Benexl/yt-x) - browse youtube and other yt-dlp sites from the terminal

[fastanime](https://github.com/Benexl/FastAnime) - browse anime from the terminal


# Receiving Support
You can find me here incase you need any help setting it up or just want to hang with the community.
<p align="center">
<a href="https://discord.gg/HBEmAwvbHV">
<img src="https://invidget.switchblade.xyz/C4rhMA4mmK">
</a>
</p>

# supporting the project
Give the project a star and consider contributing directly to the code

[![ko-fi](https://ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/Y8Y8ZAA7N)
