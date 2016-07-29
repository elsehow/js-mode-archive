## DEPRECATED ##

**NOTE:**  This project has been deprecated in favor of [js3-mode](https://github.com/thomblake/js3-mode) which is much cleaner, smaller, less crufty, and easier to install.

This is not and has never been the repo for the built-in js-mode in emacs.

**This project will no longer be maintained here**

An improved chimeric fork of js-mode and js2-mode that supports comma-first style and other quirks.

The goal of this project was to get a javascript mode working that supports [npm style](https://github.com/isaacs/npm/blob/master/doc/coding-style.md), but it turns out this mode is compatible with other styles as well. Most of the credit for the indentation goes to js-mode, with some handy special cases put in by yours truly.

## Credits ##

Created by [Thom Blake](https://github.com/thomblake).

Forked from js-mode and js2-mode.

Inspired by [A better coding convention for lists and object literals in Javascript](https://gist.github.com/357981) and [npm style](https://github.com/isaacs/npm/blob/master/doc/coding-style.md).

With help from [Cheeso on StackOverflow](http://stackoverflow.com/questions/6144930/emacs-js-mode-for-npm-style) and [Mihai Bazon](http://mihai.bazon.net/projects/editing-javascript-with-emacs-js2-mode)

The js2-mode included here is basically Steve Yegge's js2-mode version 20090723 findable [here](http://code.google.com/p/js2-mode/) with some reasonable defaults set.  I expect to be improving this as time goes on.

The js-mode included here is the one included with emacs version 24, with some modifications to the way it indents in certain cases and added backwards-compatibility for emacs version 23.2.

## Installation ##

Both js.el and js2.el should be placed in your emacs include path. You'll need to byte-compile js2-mode before using it - in emacs, `M-x byte-compile-file RET <path-to-js2.el> RET`.  If you want, js2-mode can be configured using `M-x customize-group RET js2-mode RET`.  See [here](http://code.google.com/p/js2-mode/wiki/InstallationInstructions) for detailed installation instructions on js2-mode.

The .emacs file included contains what you need to stick the 2 modes together.

For known compatible/incompatible versions of emacs, see compat.md - feel free to let me know if it is compatible or incompatible with your version of emacs.

A future version is likely to simply be a fork of js2-mode with better indentation.

## Notes ##

Using this will entail having 2 separate JS parsers running, so sometimes it takes a while to 'catch up' - if the indentation on a line looks off, try pressing TAB again.  Right now it looks like this only happens with non-comma-first continued var statements.  A future version will be a single mode based on JS2-mode (which has a better JS parser) which should solve some of these problems.

If your JS is in error, the indentation might look wrong.  I tend to regard this as a feature.

Remember - if you start a line with `(`, `[`, `+`, or `-`, strongly consider preceding it with a semicolon (`;`).

I expect that there are still some bugs; if you see any, **please report them**. Feel free to **file issue reports on github** for things like "it indented like [code block] but I want it to be [code block]".

## License ##

This program is free software; you can redistribute it and/or
modify it under the terms of the GNU General Public License as
published by the Free Software Foundation; either version 3 of
the License, or (at your option) any later version.

This program is distributed in the hope that it will be
useful, but WITHOUT ANY WARRANTY; without even the implied
warranty of MERCHANTABILITY or FITNESS FOR A PARTICULAR
PURPOSE.  See the GNU General Public License for more details.

You should have received a copy of the GNU General Public License
along with this program.  If not, see http://www.gnu.org/licenses/.

(Several programs included and referenced here are GPL, so this is too
why not.)

## DEPRECATED ##

**NOTE:**  This project has been deprecated in favor of [js3-mode](https://github.com/thomblake/js3-mode) which is much cleaner, smaller, less crufty, and easier to install.
