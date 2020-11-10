<p align="center">
  <img alt="Clipper" title="Clipper" src="icon@2x.png">
<h1 align="center"> Clipper*</h1> <br>
<p align="center">
   *A clone of the original <a href="https://github.com/AkashRajpurohit/clipper">Clipper</a>, a cross-platform clipboard manager, made with <a href="https://github.com/c-smile/sciter-sdk">Sciter</a> instead of Electron.
</p>

<p align="center">
 <img alt="preview" title="preview" src="preview.gif">
</p>

## Backstory

I thought it would be nice to have a concrete example of the same app made with Electron versus Sciter.
So I cloned [Clipper](https://github.com/AkashRajpurohit/clipper) in Sciter to the best of my ability.

The original as an Electron app is `165mb`.

In contrast, the Sciter release is only `6mb` (`3mb` compressed).

I used Quark (Sciter's version of electron-builder) to pack the program's resources into a single file, and [here](https://github.com/GirkovArpa/clipper-sciter/releases) is the result (I've only packaged for Windows at the moment).

Actually it didn't pack the `.mp3` files for some reason so I just zipped those up with the executable.

Not only is the filesize a magnitude of order lighter, but it starts up way faster and without an empty grey window at the beginning.

## Caveats

- I haven't copied the button click waves effect from the [Materialize](https://materializecss.com/waves.html) CSS library (yet).

- I haven't implemented the tray icon (yet).

- ~~Inactive, offscreen popups can be scrolled into view.~~ **Fixed!** Thanks to a pull request from [4silvertooth](https://github.com/4silvertooth).

I would like to emphasize that this is my attempt at a clone, but it's not a port. Since the original Clippy is written in React, a genuine port would utilize Sciter's "Reactor".

## Usage

Run [`scapp.exe`](https://github.com/c-smile/sciter-sdk/tree/master/bin.win/x64) in this folder.

## Packaging

Rename `index.html` to `index.htm` and follow the Quark instructions [here](https://quark.sciter.com/quark-application-samples/hello-world/), but use this repo as the source files instead of the hello world sample.

`.mp3` files won't be packaged for some reason, so they will need to be included alongside the resulting executable.