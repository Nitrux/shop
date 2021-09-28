# shop

> _Minimal package manager for UNIX shells._

`shop` is an unencumbered package manager for UNIX shells (`bash`, `mksh`, etc.),
intended to work alongside [`bass`](https://github.com/luislavaire/bass), though the latter is not required.


- Packages are installed in `~/.shop/`.
- Packages are hosted in Github.


## Installation.

- `wget -qO - https://raw.githubusercontent.com/luislavaire/shop/main/bin/shop | bash -s i luislavaire/shop`.
- `echo "export PATH=$PATH:~/.shop/.bin" >> ~/.bashrc` (if your shell is `bash`, of course).


## Usage.

`shop [CMD]`, where `CMD` is any of:

- `i [pkgs]`: Install the given packages. `shop` understands this format: `<user/repo>[/tag]`.
  If `/tag` is given, the package will be installed as `user/repo-tag`. Otherwise, as `user/repo`.
- `u [pkgs]`: Update all or the given packages.
- `r [pkgs]`: Remove the given packages.
- `l`: List installed packages.


## Package repository structure.

- Libraries should be placed in `lib/` (if you want to use [`bass`](https://github.com/luislavaire/bass)).
- Executables should be placed in `bin/`.
