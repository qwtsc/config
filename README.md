## manjaro setting
```
sudo pacman -Syy
sudo pacman-mirrors -i -c China -m rank
sudo pacman -Syyu
```
* add archlinuxcn to /etc/pacman.conf (installing google-chrome need it)
```
[archlinuxcn]
Server = https://mirrors.tuna.tsinghua.edu.cn/archlinuxcn/$arch
```
`sudo pacman -Syy && sudo pacman -S archlinuxcn-keyring`
* install fonts and fctix
```
sudo pacman -S fcitx-im
sudo pacman -S fcitx-configtool
sudo pacman -S fcitx-googlepinyin
yay -S fcitx-sogoupinyin
sudo pacman -S ttf-roboto noto-fonts ttf-dejavu
sudo pacman -S noto-fonts-cjk adoube-source-han-sans-cn-fonts adobe-source-han-serif-cn-fonts
```
* add the following lines to /etc/enviroment, add `exec --no-startup-id fcitx` into i3 config
```
GTK_IM_MODULE=fcitx
QT_IM_MODULE=fcitx
XMODIFIERS="@im=fcitx"
```

## fish config
* change the terminal to alacritty by setting mod+Return to alacritty
* change the shell to fish by `chsh -s (which fish)` then reboot
* move to fish config
* install oh-my-fish `curl -L https://get.oh-my.sh | fish`
* install omf theme `omf install tomita`
* config fish to be in vi mode by adding these two line into ~/.config/fish/config.fish
```
function fish_mode_prompt; end
fish_vi_key_bindings
```
* I think its fine to use fish now.

## i3 config
* key-binding go back to vi style plz. note mod4+h has already assigned, so remove the previous setting.
* add polybar following the wiki in archlinux and copy the jonhoo's polybar config
* install albert by pacman and bind F1 to wakeup albert
* install v2ray by pacman and enable it, note the example configure file is in /etc/v2ray/config.json
* albert and v2ray need auto-start by setting exec-always albert and blah blah
* install rdesktop for windows remote connection

## vim and tmux
* clone my config and make soft ln to clone one.
* install vim-Plug by `curl -fLo ~/.vim/autoload/plug.vim --create-dirs https://raw.githubusercontent.com/junegunn/vim-plug/master/plug.vim`
* install tmux and ohmytmux

## Language
* install jre and jdk by pacman, `sudo pacman -S jre-openjdk jdk-openjdk`
* install go by pacman
* install rust by cli from official website and add ~/.cargo/bin and ~/.cargo/env into PATH env.

## Chrome-plugin
* OmegaSwitchy - make all transports through v2ray
* vimium - don't touch mouse again
* darkreader and just Black - save my eyes

## Choice need twice thinking
* is the JetBrains app a must-have in my dev box?
* GDB is not user-friendly in my opinion, find alternatives?
* find a good app to read code, I mean vim is fantastic dealing with writing, but reading umm.
* I don't think I need wps, rdesktop can help me connect the desktop with windows, and word ppt excel can still be used by this approach. Intenet saves my life.
* Now start my journey with manjaro-i3wm, lol!



