# ngGo

[![npm version](https://img.shields.io/npm/v/ng-go.svg)](https://www.npmjs.com/package/ng-go)
[![node dependencies](https://david-dm.org/adambuczynski/ngGo.svg)](https://david-dm.org/adambuczynski/ngGo)
[![github issues](https://img.shields.io/github/issues/adambuczynski/ngGo.svg)](https://github.com/adambuczynski/ngGo/issues)
[![codacy](https://img.shields.io/codacy/7d72527f76b44256971ece497488fc80.svg)](https://www.codacy.com/app/adambuczynski/ngGo)

## About
### This project is forked from [adambuczynski/ngGo](https://github.com/adambuczynski/ngGo)

ngGo is an Angular.JS library for reading, parsing, displaying, editing and replaying Go game records.

ngGo has been based on the excellent work of Jan Prokop, who created the original javascript library [WGo.js](http://wgo.waltheri.net/). ngGo is based on WGo version 1.2.5, which was the latest version at the time of conversion.

All code has been refactored to fit the Angular framework. In addition, the code was reviewed and improved to provide more flexibility and run more efficiently. All files have also been cleaned up in general, linted and extensively commented to provide for easy to read source code with a consistent layout. Lastly, all the source code files have been organized in a logical manner and split up in sensible classes, making it easy to find all the specific modules and functionality of the library.

Note that some features of WGo were removed, as they did not fit in this library and weren't considered good practice for AngularJS development. This includes player control elements, game info display elements, notification popups, and any other hardcoded layout/HTML elements. The ngGo library is only concerned with handling game records and displaying the Go board. It is assummed that anyone using this library will implement their own player controls and game info display elements.

## Features
+ Player module to replay game records including variations and edit the board.
+ Board module to display and render the Go board using HTML 5 canvas.
+ Game module to keep track of board positions and validate moves.
+ Kifu module to store the game nodes and convert to and from SGF or JGF.

## JGF (JSON Game Format)
The ngGo library includes a [proposal](JGF.md) for a standardized JSON file format for game records. It builds on the original specifications of the [SGF file format](http://www.red-bean.com/sgf/), but has an improved and easier to parse and translate structure. In addition, the format has more flexibility than SGF for saving different/new kinds of markup or other node annotations.

ngGo also contains parsers to convert files from SGF to JGF and vice versa.

For the proposed JGF specification, please see [JGF.md](JGF.md).

## Todo
+ Finalize game record editing capabilities
+ Finalize various player modes
+ Improve game scoring algorithm
+ Add support for board animations
+ Create unit tests
