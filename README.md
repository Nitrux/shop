# shop

> _Minimal package manager for UNIX shells._

`shop` is an unencumbered package manager for UNIX shells (`bash`, `mksh`, etc.),
intended to work alongside [`bass`](https://github.com/luislavaire/bass), though the latter is not required.


- Packages are installed in `~/.shop/`.
- Packages are downloaded from Github.


## Usage.

### Adding packages.

The tag or branch name is optional, as well as the import name.

```
shop i <user/repo>[/branch] [name]
```

### Updating packages.

If no packages are specified, update all packages.

```
shop u [pkgs]
```

### Removing packages.

Remove the specified packages.

```
shop r <pkg> [pkgs]
```
