## Goals

- basic Scoop commands
- single file
- self-manageable

## Non-goal

- fully follow Scoop manifest structure

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

TBA

## TODO

- [x] downlaod file from url
- [x] extract
- [x] update

- [ ] debug mode
- [ ] force mode

- [ ] database

- [ ] init file structure
