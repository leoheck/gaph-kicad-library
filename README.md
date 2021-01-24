# Kicad Library

This is a library with custom parts (symbols, footprints and 3D models) used in our projects. These parts here are usually out of the Kicad Library or they are customizations.

It follows the [KLC](http://kicad-pcb.org/libraries/klc/) as much as possible.

> This project is currently using Kicad 5.1.6


## Managing this Library

There is a sample project called `board` that can be used as start for a new project and it can also be used to manage the this library.
Just clone this repo, and launch the sample project with:

```
cd board
kicad board.pro
```

## Available Parts

There are be 2 libraries. One for the GAPH made ICs and the second one, to add custom components that are not found on the original Kicad's Library. The custom parts are there to add missing 3D models, or to provide a custom, or easy to use footprint and symbol. 

1. GAPH Chips
2. GAPH Custom Parts

## Creating a new project

I recommend to add this library as a submodule to your project, as it follows:

```
mkdir my-new-board
cd my-new-board
git init
git submodule add git@github.com:leoheck/gaph-kicad-library.git library
cp -r library/board/board.pro .
cp -r library/fp-lib-table .
cp -r library/sym-lib-table .
```

This is the same structure used in `board` sample project. The sample project can be used as a template for a new project too.
