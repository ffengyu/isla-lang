# isla-lang

This constructs an OCaml datatype, parser, and pretty printer for the SMT
instruction-semantics description output by isla.  
It uses [ott](https://github.com/ott-lang/ott) to generate those from `isla_lang.ott`.

This project needs `dune` to build (can be installed via opam)

At present this needs the latest master branch of ott installed. 
The best way of doing that is to check it out from Github
and do `opam install .` in the repository.

Normal dependencies are `menhir` for parsing and `pprint` for pretty-printing, both of which can be obtained normally on opam.

The file `isla-lang.opam` is autogenerated by dune. Use `make opam` to regenerate it.

Usual make command like `make`, `make install`, `make uninstall` and `make clean`
work as usual and are trivial to dune sub-commands.

You can build PDF version of the language of isla traces with `make pdf`.
