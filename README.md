# NBC - Not eXactly C Compiler Conda Package

## Overview

This repository contains the materials to build a conda package for the NBC compiler.

NBC is a compiler for the "Not eXactly C" (NXC) programming language, which is used for programming LEGO MINDSTORMS NXT robots.

- **Official Website:** [https://bricxcc.sourceforge.net/nbc/release/index.html](https://bricxcc.sourceforge.net/nbc/release/index.html)
- **Author:** John Hansen
- **License:** MPL

## Conda Package

This project provides the recipe to build conda packages for the `nbc` compiler for `linux-64` and `win-64` platforms.

### Building the Package

To build the conda package from this repository, you need `conda-build`:

```bash
conda install conda-build
```

Then, run the build command from the root of this directory:

```bash
conda build .
```

This will create the `nbc` package in your local conda channel.

### Installation

Once the package is built, you can install it from your local channel:

```bash
conda install -c local nbc
```

### Usage

After installation, you can use the compiler with the `nbc` command:

```bash
nbc your_program.nxc
```

To see all available compiler options, you can use the help command:

```bash
nbc -help
```

## Repository Structure

- `meta.yaml`: The main conda recipe file that defines the package metadata and build process.
- `build.sh`: The build script for Linux and macOS.
- `bld.bat`: The build script for Windows.
- `linux-64/`: Contains the pre-compiled `nbc` binary for Linux.
- `win-64/`: Contains the pre-compiled `nbc.exe` binary for Windows.
