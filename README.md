DSSP 4.0
========

This is a rewrite of DSSP, now offering full mmCIF support. The difference
with previous releases of DSSP is that it now writes out an annotated mmCIF
file by default, storing the secondary structure information in the 
_struct_conf category.

Another new feature in this version of DSSP is that it now defines
Poly-Proline helices as well.

The DSSP program was designed by Wolfgang Kabsch and Chris Sander to
standardize secondary structure assignment. DSSP is a database of secondary
structure assignments (and much more) for all protein entries in the Protein
Data Bank (PDB). DSSP is also the program that calculates DSSP entries from
PDB entries.

DSSP does not predict secondary structure.

Requirements
------------

The tools are based on [libcif++](https://github.com/PDB-REDO/libcifpp)
and the code is written in modern C++ so you need a compiler capable
of handling C++17 code.

Building
--------

Make sure you install [libcif++](https://github.com/PDB-REDO/libcifpp) first before building.

After that, building should be as easy as typing:

```
git clone https://github.com/PDB-REDO/dssp.git
cd dssp
mkdir build
cd build
cmake ..
cmake --build . --config Release
ctest -C Release
cmake --install .
```

This will install the `mkdssp` program in `$HOME/.local/bin`. If you want to
install elsewhere, specify the prefix with the [CMAKE_INSTALL_PREFIX](https://cmake.org/cmake/help/v3.21/variable/CMAKE_INSTALL_PREFIX.html) variable.

Usage
-----

See [manual page](doc/mkdssp.pdf) for more info.
