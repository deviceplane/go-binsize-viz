# Go executable size visualization using D3

This directory contains code and data to visualize the contents of Go
binaries.

## How to use

Apply tools in order (Python 3 required):

1. `go tool nm -size <binary file> | c++filt` and redirect to some file, e.g. `symtab.txt`

   (provided with the Go toolchain.)

2. `python3 tab2pydic.py` on the previously generated file, redirect to e.g. `out.py`

3. `python3 simplify.py` on the previously generated file, redirect to `data.js` **specifically**

4. `python3 -m http.server`

5. open browser on https://localhost:8000/treemap_v3.html

## Included example data using CockroachDB

1. `python3 -m http.server`

2. open browser on https://localhost:8000/cockroach_sizes.html
