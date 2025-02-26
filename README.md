[![License: GPL v3](https://img.shields.io/badge/License-GPL%20v3-blue.svg)](https://www.gnu.org/licenses/gpl-3.0)
[![JCS-ELPA](https://raw.githubusercontent.com/jcs-emacs/badges/master/elpa/v/flymake-elsa.svg)](https://jcs-emacs.github.io/jcs-elpa/#/flymake-elsa)

# flymake-elsa - Flymake for Elsa

[![CI](https://github.com/flymake/flymake-elsa/actions/workflows/test.yml/badge.svg)](https://github.com/flymake/flymake-elsa/actions/workflows/test.yml)

Integration of [Elsa](https://github.com/emacs-elsa/Elsa) into [Flymake]().

# 💡 Elsa in Eask projects

The recommended way to use Elsa is with [Eask](https://github.com/emacs-eask/cli).

## 💾 Installation

Install `flymake-elsa` from [JCS-ELPA](https://jcs-emacs.github.io/jcs-elpa/) and add the following to your
`init.el`:

``` emacs-lisp
(add-hook 'emacs-lisp-mode-hook #'flymake-elsa-load)
```

We require that `eask` executable is usable from Emacs.  You can test
this by evaluating `(executable-find "eask")`.  If this returns `nil`,
you need to add your eask directory to `exec-path`.

You can also use the amazing
[exec-path-from-shell](https://github.com/purcell/exec-path-from-shell)
to initialize your `exec-path` from your shell's `$PATH`.

## 🔧 Usage

Just use Flymake as usual in your [Eask](https://github.com/emacs-eask/cli) projects.

## 🛠️ Contribute

### 🔬 Development

To run the test locally, you will need the following tools:

- [Eask](https://emacs-eask.github.io/)
- [Make](https://www.gnu.org/software/make/) (optional)

Install all dependencies and development dependencies:

```sh
eask install-deps --dev
```

To test the package's installation:

```sh
eask package
eask install
```

To test compilation:

```sh
eask compile
```

**🪧 The following steps are optional, but we recommend you follow these lint results!**

The built-in `checkdoc` linter:

```sh
eask lint checkdoc
```

The standard `package` linter:

```sh
eask lint package
```

*📝 P.S. For more information, find the Eask manual at https://emacs-eask.github.io/.*

## ⚜️ License

This program is free software; you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation, either version 3 of the License, or
(at your option) any later version.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU General Public License for more details.

You should have received a copy of the GNU General Public License
along with this program.  If not, see <https://www.gnu.org/licenses/>.

See [`LICENSE`](./LICENSE.txt) for details.
