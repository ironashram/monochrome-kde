# Monochrome KDE
<div align="center">
    <img src="preview.jpg" align="center" alt="Preview of Monochrome KDE theme" />
</div>

## :information_source: About
A dark theme for the KDE Plasma desktop environment inspired by black and white photography.

The complete theme consists of the following components:
- Aurorae Theme
- Konsole Colour Scheme
- Kvantum Theme
- Plasma Colour Scheme
- Plasma Desktop Theme
- Plasma Look and Feel
- Plasma Splash Screen
- SDDM Theme
- Yakuake Skin

## :floppy_disk: Install Instructions
At the time of writing there are no Linux distribution packages available. Install the complete theme manually using `git clone` or the provided install [script](install.sh). See [instructions](#install-script) below. This method works on all Linux distributions.

Individual theme components can also be downloaded from [KDE Store](https://store.kde.org)/[OpenDesktop.org](https://www.opendesktop.org) or using [Plasma System Settings](https://userbase.kde.org/System_Settings).

| **Name**              | **Preview**                                 | **KDE Store** (tar.gz)                           |
|:----------------------|:-------------------------------------------:|:------------------------------------------------:|
| Aurorae Theme         | [🖼️](screenshots/aurorae/preview.png)       | [:floppy_disk:](https://store.kde.org/p/1279082) |
| Konsole Colour Scheme | [🖼️](screenshots/konsole/preview.png)       | [:floppy_disk:](https://store.kde.org/p/1279087) |
| Kvantum Theme         | [🖼️](screenshots/kvantum/preview.png)       | [:floppy_disk:](https://store.kde.org/p/1279088) |
| Plasma Colour Scheme  | [🖼️](screenshots/color-schemes/preview.png) | [:floppy_disk:](https://store.kde.org/p/1279083) |
| Plasma Desktop Theme  | [🖼️](screenshots/plasma/preview.png)        | [:floppy_disk:](https://store.kde.org/p/1279077) |
| Plasma Look and Feel  | [🖼️](screenshots/plasma/preview.png)        | [:floppy_disk:](https://store.kde.org/p/1361190) |
| Plasma Splash Screen  | [🖼️](screenshots/plasma/splash.png)         | [:floppy_disk:](https://store.kde.org/p/1361190) |
| SDDM Theme            | [🖼️](screenshots/sddm/preview.png)          | [:floppy_disk:](https://store.kde.org/p/1361190) |
| Yakuake Skin          | [🖼️](screenshots/yakuake/preview.png)       | [:floppy_disk:](https://store.kde.org/p/1279089) |

### Install Script
The installation script will automatically download the latest version from the repository and copy the required files to the default location `/usr/share`.

**Note**: Script requires the [`wget`](https://www.gnu.org/software/wget/) command. Install it using system's package manager if not present.

#### Install
```
$ bash install.sh --install
```

#### Uninstall
```
$ bash install.sh --uninstall
```

#### Options
| **Option**         | **Description**                                   |
| ---                | ---                                               |
| `-i`,`--install`   | Install theme in default location (`/usr/share`). |
| `-u`,`--uninstall` | Uninstall theme.                                  |
| `-h`,`--help`      | Display help message including available options. |

## :bulb: Recommendations
For a better visual experience apply the following modifications and settings.

### Application Style
Download and install the [Kvantum theme engine](https://github.com/tsujan/Kvantum/tree/master/Kvantum).

Start **Kvantum Manager** > **Change/Delete Theme** > select theme **Monochrome** > **Use this theme**.

### Window Decorations
Change the default window border size in **System Settings** > **Application Style** > **Window Decorations** > un-check the option **Use theme's default window border size** > select **Tiny** from the drop-down > **Apply**.

### Icons
Download and install the [Papirus icon theme](https://github.com/PapirusDevelopmentTeam/papirus-icon-theme).

#### Folder Icon Colour (optional)
The folder colour can be changed using [papirus-folders](https://github.com/PapirusDevelopmentTeam/papirus-folders).

```
$ papirus-folders -C grey
```

### Desktop Effects
Enable **Blur** in **System Settings** > **Workspace Behaviour** > **Desktop Effetcs**.

### Login Screen (SDDM)
Change the login screen theme in **System Settings** > **Startup and Shutdown** > **Login Screen (SDDM)** > select theme **Monochrome** > **Apply**.

#### Background
Chooce either a background image or the pre-defined solid colour; `#1e1e20`

#### Fonts (optional)
Change default font for **SDDM** in the `/usr/share/sddm/themes/monochrome/theme.conf` configuration file.

### GTK2/3/4 Theme (optional)
Manually copy the included GTK2/3/4 theme from `./gtk` directory to the user theme directory.

```
$ cp gtk/Monochrome/ ~/.local/share/themes/
```

#### Note
The GTK2/3/4 theme is pre-build of the official [breeze-gtk](https://github.com/KDE/breeze-gtk.git) theme with the Monochrome KDE colour scheme.

To manually build and install the theme make sure all build dependencies are met and perform the build process.

```
$ git clone https://github.com/KDE/breeze-gtk.git
$ cd breeze-gtk/src/
$ cmake ./
$ sh build_theme.sh -c Monochrome -t ~/.local/share/themes/Monochrome
```

Enable the new GTK theme in **System Settings** > **Appearance** > **Application Style** > **Configure GNOME/GTK Application Style...** > select **Monochrome** from the drop-down list > **Apply**.

### Plymouth Boot Splash Screen (optional)
Download and install the [Monochrome Plymouth](https://gitlab.com/pwyde/monochrome-plymouth) theme.

## :heart: Credits
Some graphical elements and artwork in this project is based on other popular themes for the KDE Plasma desktop.

- **Breeze** Plasma theme by [KDE Visual Design Group](https://www.kde.org/plasma-desktop)
- **Materia KDE** Plasma theme by [Papirus Development Team](https://github.com/PapirusDevelopmentTeam/materia-kde)
- **Arc KDE** Plasma theme by [Papirus Development Team](https://github.com/PapirusDevelopmentTeam/arc-kde)
- **Papirus** icon theme by [Papirus Development Team](https://github.com/PapirusDevelopmentTeam/papirus-icon-theme)
- **Darkine KDE** SDDM theme by [Rokin](https://github.com/Rokin05/darkine-kde)

### Honorary Mention
Special credits go to [**Alexey Varfolomeev**](https://github.com/varlesh) for his work on [**Materia KDE**](https://github.com/PapirusDevelopmentTeam/materia-kde) which this theme is based on.

## :page_with_curl: Licenses
This project is licensed under the **GNU General Public License v3.0**. See the [LICENSE](LICENSE) file for more information. Graphical elements and artwork based on other projects are licensed under the following:

- **Materia KDE**: GPLv3
  - **Aurorae Theme**: GPLv3
  - **Kvantum Theme**: GPLv3
  - **Plasma Desktop Theme**: GPLv3
- **Arc KDE**: GPLv3
  - **Kvantum Theme**: GPLv3
  - **Plasma Desktop Theme**: CCPL:by-sa
  - **Plasma Splash Screen**: GPLv3
- **Papirus Icon Theme**: GPLv3
- **Breeze**: LGPL
- **Darkine**: GPLv3
  - **SDDM Theme**: CC-BY-SA

## :ballot_box_with_check: Todo
A list of features and/or components that will be added in the future.

- [x] Aurorae Theme
- [ ] Add GTK2/3 theme based on [breeze-gtk](https://cgit.kde.org/breeze-gtk.git/).
- [x] Konsole Colour Scheme
  - [x] Change colours to match theme better.
- [x] Kvantum Theme
  - [x] Create alternative theme with more transparency and blur.
- [x] SDDM Theme
  - [x] Change colours to match theme better.
  - [x] Add custom font support.
  - [x] Change font colour in all elements if possible.
- [x] Plasma Colour Scheme
- [x] Plasma Desktop Theme
  - [ ] Create a solid theme version.
- [x] Plasma Look and Feel Theme
- [x] Plasma Splash Screen
  - [x] Re-design due to issue with progress bar.
  - [ ] ~~Replace busy widget spinner with a working progress bar.~~
- [x] [Plymouth Theme](https://gitlab.com/pwyde/monochrome-plymouth)
- [x] Yakuake Skin
