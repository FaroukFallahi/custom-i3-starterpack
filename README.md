## Why i3?
i3 is (arguably) the most easiest tiling window manager to learn and configure. 
And i3 has a really good documentation, including example command and troubleshooting.
The community is also quite large. You will easily get more customization examples.
So, I really recommend You to start from i3 if You want learn Linux customization.
After You can handle i3, You can try more advanced window managers. 
i3 is my first tiling window manager by the way :relaxed: <br />

## Why Not i3-gaps?
As I previously said, I prefer to use packages those are available on main repository.
As far as I know i3-gaps package is only available on Arch, Void, Solus, and Alpine repository.
And do You know? Airblader the i3-gaps developer himself doesn't use gaps!
My whole life is a lie :confounded: <br />


## Installation
- **First, install i3 of course** <br />
`sudo apt-get install i3` <br />
It will give You i3-wm, dunst, i3lock, i3status, flameshot and suckless-tools.
If i3-wm, dunst, i3lock, i3status, flameshot and suckless-tools are not installed automatically, just install them manually. <br />
`sudo apt-get install i3-wm dunst i3lock i3status flameshot suckless-tools axel curl wget` <br />

- **Then install some additional packages to make your desktop enjoyable** <br />
`sudo apt-get install compton hsetroot rxvt-unicode xsel rofi fonts-noto fonts-mplus xsettingsd lxappearance scrot viewnior`

- **Installing oh-my-zsh** <br>
`sudo apt-get install -y zsh && sh -c "$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"`

- **Extra from snap 😬** <br>
  - `sudo snap install brave`
  - `sudo snap install alacritty --classic`
  - `sudo snap install code --classic`
  
## Explanations of Additional Packages
- Compton is a compositor to provide some desktop effects like shadow, transparency, fade, and transiton. 
- Hsetroot is a wallpaper handler. i3 has no wallpaper handler by default.
- URxvt is a lightweight terminal emulator, part of *i3-sensible-terminal*.
- Xsel is a program to access X clipboard. We need it to make copy-paste in URxvt available. Hit Alt+C to copy, and Alt+V to paste. 
- Rofi is a program launcher, similar with dmenu but with more options.
- Noto Sans and M+ are my favourite fonts used in my configuration.
- Xsettingsd is a simple settings daemon to load fontconfig and some other options. Without this, fonts would look rasterized in some applications.
- LXAppearance is used for changing GTK theme icons, fonts, and some other preferences.
- Scrot is for taking screenshoot. I use it in my configuration for Print Screen button.
I set my Print Screen button to take screenshoot using scrot, then automatically open it using Viewnior image viewer. <br />

## Copying Configurations
`git clone https://github.com/addy-dclxvi/i3-starterpack.git` <br />

Or if You don't have git package installed, and have no willing to install it. 
Just use download as zip button on the top-right of this page, then extract it.
After that, Open *i3-starterpack* folder. Then copy the configurations to your home.
I mean if it's on *i3-starterpack/.config/i3/config*, copy it to *~/.config/i3/*.
If the folder doesn't exist on your home, just make it.
Do the same with all of the files inside *i3-starterpack* folder.
My dotfiles contains font, so refresh your fontconfig cache `fc-cache -fv` after You copy the font. <br />

**Note :** You can deploy this repository recursively using 
`git clone https://github.com/addy-dclxvi/i3-starterpack.git && cp -a i3-starterpack/. ~`
but I recommend You to copy the configuration files one by one to make yourself have more control.

## Inspect and Edit The Configurations Files
- **~/.config/i3/config** <br />
This is the main configuration file of i3 window manager. Contains keybinding, autostart, colors, and window rules.
I suggest You to leave it default for now. I will explain it later. <br />
- **~/.config/i3status/config** <br />
![i3bar](https://raw.githubusercontent.com/addy-dclxvi/i3-starterpack/master/preview-i3bar.jpg) <br />
This is the statusline configuration for i3bar, bottom right part of i3bar. I set it to load many module by default.
It looks like christmast tree. So, I suggest You to disable some module You don't need. <br />
