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
