# shop

> _Minimal package manager for UNIX shells._

`shop` is an unencumbered package manager for UNIX shells (`bash`, `mksh`, etc.),
intended to work alongside [`bass`](https://github.com/luislavaire/bass), though the latter is not required.


- Packages are installed in `~/.shop/`.
- Packages are hosted on Github.


## Usage.

### Adding packages.

```
shop i <user/repo>[/<tag|branch>]
```

### Updating packages.

```
shop u [pkgs]
```

### Removing packages.

```
shop r [pkgs]
```


## Package repository structure.

Files that are to be consumed by users must be placed under `lib/`.
