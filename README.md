# Wallcalendar LaTeX documentclass

A wall calendar class with custom layouts and support for internationalization.

## Features

The documentclass comes with the following layouts:

- Full page photo, the calendar days overlaid with opacity
- Full page photo, the photo above the calendar days
- Small landscape photo, with a calendar grid
- Photo and Notes, photo and calendar on separate pages to allow space for note taking
- Title page
- Year planner
- Thumbnails and captions
- Varnish mask

There is also support for loading event marks from a CSV file.

See `wallcalendar.pdf` for the user manual, and `wallcalendar-code.pdf` for the
commented code documentation.

The manual includes examples and tutorials, but you may also want to see the [doc/examples][examples] folder on Github.

![wallcalendar layouts](./wallcalendar-layouts.png)

[examples]: https://github.com/profound-labs/wallcalendar/tree/master/doc/examples

## Installing

### TeXLive

TeXLive includes the `wallcalendar` package since 2018.

### Using from a git clone

I recommend however to clone this repository for each new calendar project, this
way you can make small changes directly in `wallcalendar.cls` or the `lua`
scripts.

You can start with one of the examples and start tweaking it. Optionally, remove
the docs if you don't want to include them in your project.

```
git clone https://github.com/profound-labs/wallcalendar.git

cd wallcalendar
cp doc/examples/cal-photo-and-notes.tex ./new-calendar.tex

cp -r doc/examples/data .
cp -r doc/examples/photos .
cp -r doc/examples/fonts .

rm doc/ -r
rm LICENSE.txt Makefile README.md wallcalendar-code.pdf wallcalendar-layouts.png wallcalendar.pdf

lualatex -interaction=nonstopmode -halt-on-error ./new-calendar.tex
```

### As a local package

If you wanted to install it as a local package, the `make local-install` task in
the project root will try to install it at `$TEXMFHOME/tex`.

## Back matter

Github: https://github.com/profound-labs/wallcalendar

Contact: Gambhiro Bhikkhu <gambhiro.bhikkhu.85@gmail.com>

LPPL LaTeX Public Project License

