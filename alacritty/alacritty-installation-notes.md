### Linux Comands

to make alacritty the default terminal 

installing x-terminal-emulator
```bash
 sudo update-alternatives --install /usr/bin/x-terminal-emulator x-terminal-emulator /usr/bin/local/alacritty 50
```

define has default 

```bash
sudo update-alternatives --config x-terminal-emulator
```

add alacritty to desktop icons

```bash
sudo cp target/release/alacritty /usr/local/bin # or anywhere else in $PATH
sudo cp extra/logo/alacritty-term.svg /usr/share/pixmaps/Alacritty.svg
sudo desktop-file-install extra/linux/Alacritty.desktop
sudo update-desktop-database
```