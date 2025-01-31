## News
Added non-compact theme variant, old Lounge theme renamed to Lounge-compact.  
Added dynamic background for gnome desktop [(repository)](https://github.com/monday15/lounge-backgrounds). Fedora/Ubuntu users will get Lounge-backgrounds package with updates (recommended dependency).

## Info
Simple and clean gtk theme, based on original Adwaita.  
Supported desktop environments: gnome 3.28+, xfce 4.12+.  
Theme also provides Lounge-aux icon theme - auxiliary set of symbolic icons for better user experience.
 
## Installation
**Fedora** users can install theme via copr:  
`sudo dnf copr enable monday15/lounge`  
`sudo dnf install lounge-gtk-theme`  
or  
`sudo dnf install lounge-gtk-theme-xfce-sway` for xfce/sway users.

> Fedora users will get Lounge-aux-icon-theme as a weak dependency with Adwaita as a main icon theme, for other icon themes - build theme with custom icon-theme option.
---

**Ubuntu** (18.04+) users can install theme via ppa:  
`sudo add-apt-repository ppa:monday15/lounge`  
`sudo apt install lounge-gtk-theme`  
or  
`sudo apt install lounge-gtk-theme-xfce-sway` for xfce/sway users.

> Ubuntu users will get Lounge-aux-icon-theme as a weak dependency with 'Yaru, Humanity, Adwaita' as a main icon theme (if Yaru is not installed Lounge-aux will inherit Humanity, etc), for other icon themes - build theme with custom icon-theme option.
---

Requirements:  
`gtk3` (3.22+)   
`meson` (0.45+)  
`sassc`  
`gtk-murrine-engine` (`gtk2-engines-murrine` for debian/ubuntu).

- Download and decompress source tarball (or clone repository);
- Build theme:  
`meson build` 
 
  Additional options are availiable, to use them add `-D` before option name and set value after: `-Doption='value'`, quotes needed only if value has multiple words separated by space. For example,  
`meson build -Dshell-font='Liberation Sans' -Dicon-theme=Suru -Dgtk2-solid-menu=true`  
builds gnome-shell theme with Liberation Sans font, Lounge-aux icon theme that will inherit icons from Suru icon theme and with gtk2 theme fixes for Xfce desktop.

  Option | Description
  --- | ---
  gtk2-solid-menu | Use solid border for menus in gtk2 theme - highly recommended option for Xfce/Sway users, but looks bad in GNOME. [Xfce screenshot with comparison](https://user-images.githubusercontent.com/42862490/54489243-230b9280-48cc-11e9-9191-7912a4ef328f.png), can be true or false (default: false)
  icon-theme | Specify main icon theme for Lounge-aux (default: Adwaita)
  icons | Install Lounge-aux, can be true or false (default: true)
  shell-font | Specify font for gnome-shell theme (default: Roboto)

- Install theme:  
`sudo ninja -C build install`

## Flatpak
Flatpak apps support available via Flathub:  
`flatpak remote-add --if-not-exists flathub https://dl.flathub.org/repo/flathub.flatpakrepo`  
`flatpak install flathub org.gtk.Gtk3theme.Lounge`  
`flatpak install flathub org.gtk.Gtk3theme.Lounge-night`

## Updating
**Attention! Updating from version ≤ 1.16 to version ≥ 1.17 requires comlete removal of theme files before installation** (folders `/usr/share/themes/Lounge` and `/usr/share/themes/Lounge-night`, icons folder doesn't require removal).

In other cases, use regular installation instructions, old files will be overwritten with a new ones.

## Removing
Remove installation folders:  
`/usr/share/themes/Lounge`  
`/usr/share/themes/Lounge-night`  
`/usr/share/icons/Lounge-aux`

## Licence
GPLv3+, see LICENSE file.  
Original themes/styles copyrights are in COPYRIGHT file.

## Bugs
Report bugs to [issues page](https://github.com/monday15/lounge-gtk-theme/issues).

## Thanks
Allan Day, dcbaker, Emmanuele Bassi, horst3180, nana-4, NicoHood, Sam Hewitt, Thibault Saunier, tista500, vinceliuice, ZMA, all people in copyright file, Gnome developers and maintainers, Fedora developers and maintainers, Greybird theme developers, Meson developers, Yaru theme developers.

## Links
[Adwaita gtk2 theme](https://gitlab.gnome.org/GNOME/gnome-themes-extra), [Adwaita gtk3 theme](https://gitlab.gnome.org/GNOME/gtk), [gnome-shell theme](https://gitlab.gnome.org/GNOME/gnome-shell), [Materia theme](https://github.com/nana-4/materia-theme), [Yaru theme](https://github.com/ubuntu/yaru).  
List of applications (their original css styles used in the theme): [Gedit](https://gitlab.gnome.org/GNOME/gedit), [Nautilus](https://gitlab.gnome.org/GNOME/nautilus).

## Screenshots
![auxdiff](https://user-images.githubusercontent.com/42862490/50310672-82702700-04c4-11e9-9e3c-e806dcc942eb.png)

![lounge-screenshot](https://user-images.githubusercontent.com/42862490/61176961-95bf1d00-a5e3-11e9-9d83-e9c992e4d1ab.png)
