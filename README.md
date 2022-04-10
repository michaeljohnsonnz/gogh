# Gogh

Our class was given the task to choose 3 programs from [awesome-shell](https://github.com/alebcay/awesome-shell). We need to demonstrate how to install and use it on a virtualbox with Ubuntu. 

The 3 programs I've selected are as follows:
- [gogh](https://github.com/Mayccoll/Gogh)
- [prettyping](https://github.com/denilsonsa/prettyping)
- [critic](https://github.com/Checksum/critic.sh)

For this exercise, we're working with [gogh](https://github.com/Mayccoll/Gogh).

## Table of Contents
- [Gogh](#gogh)
  - [Table of Contents](#table-of-contents)
  - [1. Install](#1-install)
    - [1.1 Requirements](#11-requirements)
    - [1.2 Interactive Install](#12-interactive-install)
  - [2. Errors](#2-errors)
    - [2.1 Error: Unsupported Terminal](#21-error-unsupported-terminal)
    - [2.2 Error: Default Profile](#22-error-default-profile)

## 1. Install

### 1.1 Requirements

This is requirement to install `gogh` in interactive mode.

```bash
sudo apt-get install dconf-cli uuid-runtime

```
### 1.2 Interactive Install

This provides an interactive installation of themes for your terminal window.

```bash
bash -c "$(wget -qO- https://git.io/vQgMr)"
```

## 2. Errors

### 2.1 Error: Unsupported Terminal

The command `bash -c "$(wget -qO- https://git.io/vQgMr)"` was receiving an error so about my terminal not being supported so I tried `sudo bash -c "$(wget -qO- https://git.io/vQgMr)"`. This created the error below.

![Gogh error default profile](https://github.com/michaeljohnsonnz/gogh/blob/main/gogh-error-unsupported-terminal.png)

I followed the steps.

```bash
# Verify terminal name is gnome-terminal
ps -h -o comm -p $PPID

# Verify terminal name is gnome-terminal
echo $TERMINAL

# Set TERMINAL to gnome-terminal
export TERMINAL="gnome-terminal"

# Verify terminal name is gnome-terminal
echo $TERMINAL
```

I was still receiving the same error so I found a suggestion in a comment that it was a default profile issue.

### 2.2 Error: Default Profile

**Problem:** I received an error about my default profile.

![Gogh error default profile](https://github.com/michaeljohnsonnz/gogh/blob/main/gogh-error-default-profile.png)

**Solution:** On Ubuntu, I needed to change the name of the terminal's default profile from `unamed` to `Default`

Go to the hamburger menu, select `Preferences` and on the left hand side, change profile `unnamed` to something else. I used `Default`, `default`, and `vm` so I don't think it matters what you enter, as long as you enter something. Then I was able to run the command `bash -c "$(wget -qO- https://git.io/vQgMr)"` successfully.