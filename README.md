# Rip In Peace

`rip` is a simple command-line tool for making easy work of ripping DVDs.

It requires that you have [dvdbackup](http://dvdbackup.sourceforge.net/) and [HandBrakeCLI](https://handbrake.fr/docs/en/latest/cli/cli-options.html) installed.

## Usage

```
rip [device] [output directory] (options)

[device] defaults to /dev/sr0
[output directory] defaults to the current directory

Options:
    -m,--movie          Treat the DVD as a movie (default). One file with be produced.
    -s,--series [i:j]   Treat the DVD as a TV series. One file per chapter will be produced.
                        Files will be named as series [i], starting at chapter [j] (default: 1:1)
    -t,--title [title]  Use [title] as the file name prefix. (defaults to auto-detection)
```

Example usage:

Rip a movie: `rip /dev/sr0 ~/movies/ -m`

Rip a TV series, starting at series 2, episode 1: `rip /dev/sr0 ~/tv/ -s 2:1`
