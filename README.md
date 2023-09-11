# distrobuilder

<p align="center">
  <img height="100" width="100" src=".sphinx/_static/download/containers.small.png">
</p>
<p align="center">
  <a href="https://github.com/lxc/distrobuilder/actions"><img src="https://github.com/lxc/distrobuilder/workflows/CI%20tests/badge.svg"></a>
  <a href=https://bestpractices.coreinfrastructure.org/projects/1728"><img src="https://bestpractices.coreinfrastructure.org/projects/1728/badge"></a>
</p>

System container image builder for LXC and LXD

## Status
Type            | Service               | Status
---             | ---                   | ---
CI              | GitHub                | 
Project status  | CII Best Practices    | 


## Command line options

<!-- Include start CLI -->
The following are the command line options of `distrobuilder`. You can use `distrobuilder` to create container images for both LXC and LXD.

```bash
$ distrobuilder
System container image builder for LXC and LXD

Usage:
  distrobuilder [command]

Available Commands:
  build-dir      Build plain rootfs
  build-lxc      Build LXC image from scratch
  build-lxd      Build LXD image from scratch
  help           Help about any command
  pack-lxc       Create LXC image from existing rootfs
  pack-lxd       Create LXD image from existing rootfs
  repack-windows Repack Windows ISO with drivers included

Flags:
      --cache-dir         Cache directory
      --cleanup           Clean up cache directory (default true)
      --debug             Enable debug output
      --disable-overlay   Disable the use of filesystem overlays
  -h, --help              help for distrobuilder
  -o, --options           Override options (list of key=value)
  -t, --timeout           Timeout in seconds
      --version           Print version number

Use "distrobuilder [command] --help" for more information about a command.

```
<!-- Include end CLI -->

## Installation

See [doc/howto/install.md](doc/howto/install.md) for instructions.

## How to use

See [How to use `distrobuilder`](doc/howto/build.md) for instructions.

## Troubleshooting

See [Troubleshoot `distrobuilder`](doc/howto/troubleshoot).
[![LXD](../.sphinx/_static/download/containers.png)](https://linuxcontainers.org/lxd)

# `distrobuilder`

`distrobuilder` is an image building tool for LXC and LXD.

Its modern design uses pre-built official images whenever available and supports a variety of modifications on the base image.
`distrobuilder` creates LXC or LXD images, or just a plain root file system, from a declarative image definition (in YAML format) that defines the source of the image, its package manager, what packages to install or remove for specific image variants, OS releases and architectures, as well as additional files to generate and arbitrary actions to execute as part of the image build process.

`distrobuilder` can be used to create custom images that can be used as the base for LXC containers or LXD instances.

The LXD team uses `distrobuilder` to build the images on the [Linux containers image server](https://images.linuxcontainers.org/).
You can also use it to build images from ISO files that require licenses and therefore cannot be distributed.

## Project and community

`distrobuilder` is free software and developed under the [Apache 2 license](https://www.apache.org/licenses/LICENSE-2.0).
It's an open source project that warmly welcomes community projects, contributions, suggestions, fixes and constructive feedback.

The LXD project is sponsored by [Canonical Ltd](https://www.canonical.com).

- [Code of Conduct](https://github.com/lxc/lxd/blob/master/CODE_OF_CONDUCT.md) <!-- wokeignore:rule=master -->
- [Contribute to the project](https://github.com/lxc/distrobuilder/blob/master/CONTRIBUTING.md)  <!-- wokeignore:rule=master -->
- [Discuss on IRC](https://web.libera.chat/#lxc) (see [Getting started with IRC](https://discuss.linuxcontainers.org/t/getting-started-with-irc/11920) if needed)
- [Ask and answer questions on the forum](https://discuss.linuxcontainers.org)
- [Join the mailing lists](https://lists.linuxcontainers.org)
