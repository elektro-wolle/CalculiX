# CalculiX version 2.15

This is a repository with CalculiX code dedicated to run on MacOS.

The official homepage of CalculiX is found here: 
------------------------------------------------

http://www.dhondt.de/


It provides links to where the upstream(official) CalculiX code can be obtained.


# Building on MacOS

Prepare system, `gcc-8` is required:

```sh
brew install gcc@8
```

Clone this repository

```sh
git clone https://github.com/elektro-wolle/CalculiX.git
cd CalculiX
```

Build `SPOOLES2.2` library:

```sh
cd SPOOLES2.2
make lib
cd MT/src
make makeLib
```

Build `ARPACK`:

```sh
cd ../../../ARPACK/
make lib
```

Build `CCX` and install:

```sh
cd ../CalculiX/ccx_2.15/src/
make -j4
cp ccx_2.15 /usr/local/bin/
```

