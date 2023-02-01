[![License: GPL v3](https://img.shields.io/badge/License-GPL%20v3-blue.svg)](https://www.gnu.org/licenses/gpl-3.0)
[![JCS-ELPA](https://raw.githubusercontent.com/jcs-emacs/badges/master/elpa/v/flymake-elsa.svg)](https://jcs-emacs.github.io/jcs-elpa/#/flymake-elsa)

# flymake-elsa - Flymake for Elsa

[![CI](https://github.com/flymake/flymake-elsa/actions/workflows/test.yml/badge.svg)](https://github.com/flymake/flymake-elsa/actions/workflows/test.yml)

Integration of [Elsa](https://github.com/emacs-elsa/Elsa) into [Flymake]().

# Elsa in Eask projects

The recommended way to use Elsa is with [Eask](https://github.com/emacs-eask/cli).

## Installation

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

## Usage

Just use Flycheck as usual in your [Eask](https://github.com/emacs-eask/cli) projects.
