# Functions

## Downloading `.m3u8` files

Sometimes it's useul to download `.m3u8` files.
Luckily, a library called `ffmpeg` exists helping you with that.
I created a small function you can call from the command-line, where you need to specify the `master.m3u8` link first and the final filename (e.g. `video.mp4`) as a second parameter.

```bash
function download_m3u8() {
    ffmpeg -protocol_whitelist file,http,https,tcp,tls,crypto -i "$1" -c copy "$2"
}
```

Here's an example usage:

```shell
$ download_m3u8 https://example.com/master.m3u8 video.mp4
```
