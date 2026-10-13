<h1 align="center">
  <img src="https://raw.githubusercontent.com/JappeOS/JappeOS/dev/Icons/jappeos-logo-banner-white-512.png" width="120"><br>
  nvidia-utils-jappeos
</h1>

<p align="center">
  <strong>Packaging for `nvidia-utils`, `opencl-nvidia` and `nvidia-open-dkms` for JappeOS.</strong>
</p>

<p align="center">
  <a href="./issues"><img src="https://img.shields.io/github/issues/JappeOS/nvidia-utils-jappeos?style=plastic&color=edda09"></a>
  <a href="./pulls"><img src="https://img.shields.io/github/issues-pr/JappeOS/nvidia-utils-jappeos?style=plastic&color=40a842"></a>
  <a href="./blob/main/LICENSE"><img src="https://img.shields.io/github/license/JappeOS/nvidia-utils-jappeos?style=plastic&color=9d09ed"></a>
  <img src="https://img.shields.io/badge/arch-x86__64-blue?style=plastic">
  <img src="https://img.shields.io/badge/status-experimental-orange?style=plastic">
  <a href="https://discord.gg/dRtU4HR"><img src="https://img.shields.io/discord/716673375946407972?style=plastic&color=3250a8"></a>
</p>

---

## Overview

Packaging for `nvidia-utils`, `opencl-nvidia` and `nvidia-open-dkms` for JappeOS.
This is just a packaging repository for the package manager, not a source repo.

This packaging repository provides modified versions of the `nvidia-utils`, `opencl-nvidia` and
`nvidia-open-dkms` packages. The main purpose of these modifications is to solve an issue where
the `nvidia-utils` package installed a configuration that blacklisted the `nouveau` driver from loading.
But `nvidia-utils` is just a utility library and not the driver itself, which causes a situation
where the `nouveau` driver cannot load because it is blacklisted, and the proprietary driver
cannot load because it's not even installed. These changes ensure that `nouveau` is only
blacklisted when the proprietary driver (`nvidia-open-dkms`) is actually installed.

## Features

* Provides improved versions of `nvidia-utils`, `opencl-nvidia` and `nvidia-open-dkms` packages for JappeOS.

## Role in the OS

Allows Nvidia drivers to be handled cleanly.

## Contributing

Contributions of all kinds are welcome and appreciated. You can help the project by:

- ⭐ Starring the repository to show your support
- 💖 Sponsoring the project (if available)
- 🐞 Reporting bugs via [GitHub Issues](./issues)
- 💡 Requesting or discussing new features

For code contributions, please see [`CONTRIBUTING.md`](./CONTRIBUTING.md) for guidelines.

## License

This repository is part of the JappeOS project and is licensed under the terms described in the [`LICENSE`](./LICENSE) file.