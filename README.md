# Gogh

## Install

This is to install `gogh` in interactive mode.

```bash
sudo apt-get install dconf-cli uuid-runtime

```

To prevent an error about not being a supported terminal we need to set the `TERMINAL` environment variable

```bash
export TERMINAL="gnome-terminal"
```

Interactive installation of themes.

```bash
bash -c "$(wget -qO- https://git.io/vQgMr)"
```

**Note:** On Ubuntu I needed to change the name of the terminal's default profile from `unamed` to `Default`