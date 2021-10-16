# ppsh
A simple shell screenshot tool that uploads to an ssh server,
  named after the PPSh, a Soviet submachine gun, because it shoots and ends with `sh`.

Replacement for my old python script because finding a maintained SFTP library for Python is more effort than it’s worth.

## Usage

```sh
ppsh
```

to capture a screenshot and upload it or

```sh
ppsh file.png
```

to upload `file.png` to the remote server.

## Configuration

The first few lines of the script are the config variables.
Use them to set the remote host, destination folder, etc.

## Dependencies

This script will work on Xorg and Wayland by checking the `WAYLAND_DISPLAY` environment variable.

When used on Xorg, it requires `maim` for the image capture and `xsel` for clipboard management.  
When used on Wayland, it requires `grim`/`slurp` for the image capture and `wl-copy` for clipboard management.
