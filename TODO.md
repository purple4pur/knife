## Goals

- basic Scoop commands
- single file
- self-manageable

## Non-goals

- fully follow/support Scoop manifest structure

## directory structure:

- $HOME/knife/
    - apps/
        - knife/
            - current -> 0.1.0
            - 0.1.0/
        - chezmoi/
            - current -> 2.48.1
            - 2.48.1/
    - cache/
    - manifests/
        - chezmoi.json
    - shims/
        - knife -> ../apps/knife/current/$bin
        - chezmoi -> ../apps/chezmoi/current/$bin

## manifest structure

`ctags-nightly.json`:

```
{
  "version": "2024.05.27",
  "url": "https://github.com/universal-ctags/ctags-nightly-build/releases/download/2024.05.27+653ca9204527fe1da7ecf97c3da4308f9ab17d2c/uctags-2024.05.27-linux-x86_64.tar.gz",
  "dl_type": "tar.gz",
  "bin": [
    [
      "uctags-2024.05.27-linux-x86_64/bin/ctags",
      "ctags"
    ]
  ],
  "checkver": {
    "url": "https://github.com/universal-ctags/ctags-nightly-build/releases/latest",
    "regex": "/releases/tag/(?:v|V)?([\\d.]+)\\+([\\da-f]+)",
    "match": {
      "fulltag": "${1}+${2}"
    }
  },
  "autoupdate": {
    "url": "https://github.com/universal-ctags/ctags-nightly-build/releases/download/${fulltag}/uctags-${version}-linux-x86_64.tar.gz",
    "bin": [
      [
        "uctags-${version}-linux-x86_64/bin/ctags",
        "ctags"
      ]
    ]
  }
}
```

### Breakdown

TBD

## TODO

- [x] downlaod file from url
- [x] extract
- [x] update
- [x] uninstall

- [ ] error handling
- [ ] error/warning message

- [ ] debug mode
- [ ] force mode

- [ ] database
- [ ] list

- [ ] init file structure
