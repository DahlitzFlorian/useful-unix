# Aliases

## Find all todos

I pretty much like the concept of creating a single `TODO` file per project in the root directory of the project.
However, it may happen, that I have the time to work on something, but are not quite sure, which urgent todos are still open.
Therefore, I defined a small alias, listing all `TODO` files in my users home directory excluding the `.local` directory.

```bash
alias todos="find /home/florian -path /home/florian/.local -prune -o -name TODO -print"
```


## Open Files with Assoziated Applications

The past two years I mainly worked on MacOS and liked the capability to open a file from the command-line with the assoziated application by simply typing:

```shell
$ open file
```

On Debian you have a similar tool called `xdg-open`.
That's why I created an alias for that:

```bash
alias open="xdg-open"
```

# Git Aliases

There exist a few git commands I use quite frequently.
For those commands I created aliases, so that I don't have to type so many characters.

```bash
alias gs="git status"
alias gd="git diff"
```


# Copy and Paste to Clipboard

`xclip` is a tool, which helps you copying and pasting content from stdout and to stdin.
You may need to install it through `apt` or the package manager of your distro.
As I see myself quite often in the situation, that I want to copy such content to clipboard and paste content from the clipboard to stdin, I created aliases for them:

```bash
alias c="xclip -selection clipboard"
alias p="xclip -selection clipboard -o"
```
