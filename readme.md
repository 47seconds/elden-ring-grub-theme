# Elden Ring GRUB Theme

Can't find an **Elden Ring** GRUB theme for my bootloader, so I build one on my own. This theme features the Grace at Roundtable Hold.

<div align="center">
  <img src="screenshot.png" alt="Elden Ring GRUB Theme" width="800">
</div>

## Features

- **Immersive Background**: High-quality Elden Ring splash screen.
- **Minimal Layout**: Focuses on simplicity and legibility.
- **Plug & Play**: Just run the install script and reboot.
- **Cross-Distro Compatible**: Works with both Debian- and Arch-based systems.

## Installation

### Prerequisites

- GRUB2 must be installed.
- Root privileges are required to apply changes.

### Clone the Repository

```bash
git clone https://github.com/47seconds/elden-ring-grub-theme.git
cd elden-ring-grub-theme
````

### Automatic Installation

Run the included installer:

```bash
sudo ./install.sh
```

### Manual Installation

#### Step 1: Copy Theme to GRUB Directory

```bash
sudo mkdir -p /boot/grub/themes
sudo cp -r elden-ring-grub-theme /boot/grub/themes/
```

#### Step 2: Configure GRUB to Use the Theme

Edit `/etc/default/grub` and add or modify the line:

```plaintext
GRUB_THEME="/boot/grub/themes/elden-ring-grub-theme/theme.txt"
```

#### Step 3: Update GRUB

* On **Debian/Ubuntu**:

  ```bash
  sudo update-grub
  ```

* On **Arch/Manjaro**:

  ```bash
  sudo grub-mkconfig -o /boot/grub/grub.cfg
  ```

#### Step 4: Reboot

```bash
sudo reboot
```

Enjoy your Elden Ring boot experience.

## Customization

You can tweak the following by editing `theme.txt` inside the theme folder:

* **Font & Size**
* **Menu Spacing**
* **Color Scheme**
* **Background Image** (`background.png`)

## Troubleshooting

* **Theme not applied?**

  * Make sure `GRUB_THEME` points to the correct path.
  * Run the correct update command based on your distro.

* **No `/boot/grub/themes`?**

  ```bash
  sudo mkdir -p /boot/grub/themes
  ```

* **Secure Boot Issues?**

  * Try disabling Secure Boot in your BIOS/UEFI if theme fails to apply.

## License

This project is licensed under the MIT License. See the LICENSE file for more details.