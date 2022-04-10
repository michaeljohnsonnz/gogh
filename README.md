# Gogh

As part of our homework we have to install and demonstrate 3 command line applications. For this task, I've chosen [https://github.com/Mayccoll/Gogh](https://github.com/Mayccoll/Gogh) and the following steps is what it took to get it going.

- [Gogh](#gogh)
  - [1. Install](#1-install)
    - [1.1 Requirements](#11-requirements)
    - [1.2 Error: Unsupported Terminal](#12-error-unsupported-terminal)

## 1. Install


### 1.1 Requirements

This is requirement to install `gogh` in interactive mode.

```bash
sudo apt-get install dconf-cli uuid-runtime

```

### 1.2 Error: Unsupported Terminal

I received an error about my terminal not being a supported terminal we need to set the `TERMINAL` environment variable

![Gogh error unsupported terminal](https://github.com/michaeljohnsonnz/gogh/blob/main/gogh-error-unsupported-terminal.png)

```bash
export TERMINAL="gnome-terminal"
```

Interactive installation of themes.

```bash
bash -c "$(wget -qO- https://git.io/vQgMr)"
```

**Note:** On Ubuntu I needed to change the name of the terminal's default profile from `unamed` to `Default`