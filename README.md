# ipretty

Interactive Emacs Lisp pretty-printing

`pretty.el` provides interactive functions to pretty-print the result of an expression and a global made `ipretty-mode` that advices `eval-print-last-sexp` to pretty print.

## Installation

### quelpa

`quelpa` is at https://github.com/quelpa/quelpa

```lisp
(quelpa '(ipretty :fetcher github :repo "steckerhalter/ipretty"))
```

## Usage

Bind the functions to keys:

```lisp
(global-set-key (kbd "C-h C-j") 'ipretty-last-sexp)
(global-set-key (kbd "C-h C-k") 'ipretty-last-sexp-other-buffer)
```

To make `eval-print-last-sexp` (bound to `C-j` in `lisp-interaction-mode`) pretty-print you can use the global mode `ipretty-mode`:

    M-x ipretty-mode

Turning the mode off will remove the advice and `eval-print-last-sexp` will work normally again.