# isla-lang

This constructs an OCaml datatype, parser, and pretty printer for the SMT
instruction-semantics description output by [isla](https://github.com/rems-project/isla/). Everything is generated
from file `isla_lang.ott` using [ott](https://github.com/ott-lang/ott).

## Installation

The recommended way of installing isla-lang is via `opam`. You can pin this
repository (which makes it available in your current switch) using:
```sh
opam pin add -y isla-lang "git+https://github.com/rems-project/isla-lang.git"
```
Or you can pin your local clone by running the following command at the root
of the repository:
```sh
opam pin add -y isla-lang .
```
Note that the previous command will install the last committed changes only,
and thus not include (staged or unstaged) local changes. You need to use the
`-w` option if you want to pin the repo with all the local changes.

To only install the project's dependencies, run the following command
from your local clone of the repository:
```sh
opam install --deps-only ./isla-lang.opam
```

## Development notes

The file `isla-lang.opam` is autogenerated by dune. This is configured in the
`dune-project` file.

Usual make command like `make`, `make install`, `make uninstall` and `make
clean` work as usual and are trivial calls to dune sub-commands. We advise
not to do manual installs with `make install` and use `opam` (as explained
above) instead.

Note that this package comes with PDF versions of the languages of isla
traces. To avoid having `pdflatex` as a dependency, these files are stored
in the repository under the `doc` directory. They can be updated by using
`make update_pdfs`.

The package also comes with an example program called `isla-lang`. From the
repository, it can be invoked with `dune exec -- isla-lang <ARGS>`. You can
run `dune exec -- isla-lang -h` to see a list of available options.

## Funding

This software was developed by the University of Cambridge Computer
Laboratory (Department of Computer Science and Technology), in part
under DARPA/AFRL contract FA8650-18-C-7809 ("CIFV"), in part funded by
EPSRC Programme Grant EP/K008528/1 "REMS: Rigorous Engineering for
Mainstream Systems", in part funded from the European Research Council
(ERC) under the European Union’s Horizon 2020 research and innovation
programme (grant agreement No 789108, "ELVER"), in part supported by
the UK Government Industrial Strategy Challenge Fund (ISCF) under the
Digital Security by Design (DSbD) Programme, to deliver a DSbDtech
enabled digital platform (grant 105694), and in part funded by Google.
