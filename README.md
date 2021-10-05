# shop

> _Minimal package manager for UNIX shells._

`shop` is a simplistic package manager for UNIX shells and a build system.


## Installation.

- `wget -qO - https://raw.githubusercontent.com/Nitrux/shop/main/bin/shop | bash -s i Nitrux/shop`.
- `echo "export PATH=$PATH:~/.shop/.bin" >> ~/.bashrc` (if your shell is `bash`, of course).


## Usage.

`shop [CMD]`, where `CMD` is any of:

- `b [out]`: Read `./shopfile` and build the project. If `out` is given, it will override the
   target defined in `./shopfile`.
- `i [pkgs]`: Install the given packages. `shop` understands this format: `<user/repo>[/tag]`.
  If `/tag` is given, the package will be installed as `user/repo-tag`. Otherwise, as `user/repo`.
- `u [pkgs]`: Update all or the given packages.
- `r [pkgs]`: Remove the given packages.
- `l`: List installed packages.

### shopfile format.

The `shopfile` is your build file. There you specify your main script, the packages it uses and
the output file (this last one can be overriden on the command line). Below is an example of how
a `shopfile` might look like:

```
# Comments work as always.
# This is the content of './shopfile'.
# shop uses the bcf file format (https://github.com/Nitrux/bcf).

Main main.sh      # The entrypoint, the main script.
Target "$PWD/app" # The output.

Include Nitrux/bcf:bcf      # The frist two are files from shop packages.
      , cool/pkg:file       # These last two are files under './lib'.
      , lib/pretty-print.sh # You can tell because files from packages
      , lib/logger.sh       # are preceded by a semicolon.
```

A shebang is __mandatory__ in your main script.


## Package repository structure.

Convention over configuration:

- Repositories must be hosted at GitHub.
- Libraries should be placed in `lib/`.
- Executables should be placed in `bin/`.
