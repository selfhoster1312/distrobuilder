# How to install distrobuilder

## Installing from package

`distrobuilder` is available from the following repositories:

- [Snap Store](https://snapcraft.io/distrobuilder): `sudo snap install distrobuilder --classic`
- [Archlinux](https://archlinux.org/packages/extra/x86_64/distrobuilder/): `sudo pacman -S distrobuilder`
- [NixOS](https://search.nixos.org/packages?channel=23.05&show=distrobuilder&from=0&size=50&sort=relevance&type=packages&query=distrobuilder): `nix-shell -p distrobuilder`

**Note: `--classic` argument is [required for snap usage](troubleshoot.md#classic-confinement)**

## Installing from source

### Dependencies

To compile `distrobuilder` from source, first install the Go programming language, and some other dependencies.

#### Debian-based systems

Everything you need is packaged for Debian bookworm, you will just have to install a few packages:

```
sudo apt update
sudo apt install -y golang-go debootstrap rsync gpg squashfs-tools git
```

#### Archlinux-based systems

Everything you need is packaged for archlinux, you will just have to install a few packages:

```
sudo pacman -Syu
sudo pacman -S go debootstrap rsync gnupg squashfs-tools git --needed
```

### Clone the source repository

Download the source code of the `distrobuilder` repository (this repository).

```
git clone https://github.com/lxc/distrobuilder
```

### Build the executable

Enter the directory with the source code of `distrobuilder` and run `make` to compile the source code. This will generate the executable program `distrobuilder`, and it will be located at `$HOME/go/bin/distrobuilder`.

```
cd ./distrobuilder
make
```

This location is standard for go tooling, but may require that you add to your $PATH the directory `$HOME/go/bin/` so that you do not need to run the command with the full path.

Alternatively, you can place the executable in a different directory, like so:

```
go build -o ~/.local/bin/ ./distrobuilder
```
