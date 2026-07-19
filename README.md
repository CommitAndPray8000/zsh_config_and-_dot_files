# Zsh Config & Dotfiles

My personal Zsh configuration and dotfiles, including [Starship](https://starship.rs/) prompt setup and a set of quality-of-life CLI tools.

## Prerequisites

### 1. A terminal with graphical capabilities

Any modern terminal works — e.g. **Kitty**, **Alacritty**, or **Konsole** (default on KDE).

```bash
# Kitty (Arch-based)
sudo pacman -S kitty
# Kitty (fedora-based)
sudo dnf install kitty
# Kitty (debian/ubuntu-based)
sudo apt install kitty
```

### 2. Zsh

```bash
# Arch-based
sudo pacman -S zsh
# Kitty (fedora-based)
sudo dnf install zsh
# Kitty (debian/ubuntu-based)
sudo apt install zsh util-linux-user 

```
> util-linux-user provides the chsh on fedora.

Set Zsh as your default shell:

```bash
chsh -s $(which zsh)
```

### 3. Supporting tools

| Tool | Purpose | Install (Arch-based) |
|------|---------|----------------------|
| [fzf](https://github.com/junegunn/fzf) | Fuzzy finding within file contents | `sudo pacman -S fzf` |
| [zoxide](https://github.com/ajeetdsouza/zoxide) | Smarter directory jumping / history tracking | `sudo pacman -S zoxide` |
| [bat](https://github.com/sharkdp/bat) | A better `cat` with syntax highlighting | `sudo pacman -S bat` |
| [Starship](https://starship.rs/) | Fast, customizable shell prompt | `curl -sS https://starship.rs/install.sh \| sh` |

> On other distros, substitute your package manager (`apt`, `dnf`, `zypper`, etc.) — package names are usually the same.

## Installation

### 1. Clone the repository

```bash
git clone https://github.com/CommitAndPray8000/zsh_config_and-_dot_files
```

### 2. Set up `zshenv`

Open the system-wide Zsh environment file:

```bash
sudo nano /etc/zsh/zshenv
```

Copy the contents of this repo's `zshenv` file (the one **without** the leading dot) into it, then save and exit:

- **nano:** `Ctrl + O` → `Enter` (save) → `Ctrl + X` (exit)

### 3. Set up the config directory

> Replace `username` with your actual username throughout.

Create the Zsh config folder:

```bash
mkdir -p /home/username/.config/zsh
```

Copy all remaining files from the cloned repo — **including** dotfiles (files starting with `.`) but **excluding** the plain `zshenv` file you already handled above — into that folder:

```bash
cp -r /path/to/cloned/repo/.[!.]* /path/to/cloned/repo/* /home/username/.config/zsh/
```

### 4. Load the config

```bash
cd /home/username/.config/zsh
source .zshrc
```
Then: — open a new terminal session (or run `exec zsh`) to see the changes take effect.

### 5. Go to the starship website
and pick preset from
```bash
https://starship.rs/presets/
```
Now run the command for the preset you have chosen.
In my case 
```bash
starship preset jetpack -o ~/.config/starship.toml
```
### Voilla You are done. 
