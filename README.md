# Playlist converter

The idea here is simple; a command line tool that will convert a
specified Rhythmbox playlist to Ogg Vorbis and dump the output where you
tell it too.

## Usage

Minimally you can use it like this:

```bash
  playlist_converter --name myplaylist
  # or:
  playlist_converter -n myplaylist
```
The result will be a folder created in the current directory filled with
Ogg Vorbis encoded versions of all the songs in the "myplaylist"
playlist.

You can also specify where you want the output directory created:

```bash
  playlist_converter --name myplaylist --output_dir /media/mike/usb_stick
  # or:
  playlist_converter -n myplaylist -o /media/mike/usb_stick
```

## Dependencies

You will need vorbis-tools installed since the oggenc command is used to
encode the files.

# TODO

* This probably makes more sense as a Rhythmbox plugin, since is relies
  on reading Rhythmbox's "private" files.
* Options to output mp3 or other files might be nice.
* Options to modify the encoding quality
* If it makes sense for this to be a CLI tool, a Go rewrite would be
  nice.
* How does CMUS store its playlist?
