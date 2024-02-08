[![GitHub](https://img.shields.io/badge/GitHub-forlapack-blue.svg?style=social&logo=github)](https://github.com/gha3mi/forlapack)
[![License](https://img.shields.io/github/license/gha3mi/forlapack?color=green)](https://github.com/gha3mi/forlapack/blob/main/LICENSE)

**ForLAPACK** compiles the latest [LAPACK](https://github.com/Reference-LAPACK/lapack) using the Fortran Package Manager (fpm).

<!-- ![ForLAPACK](media/logo.png) -->

## How to Build

### 1. Requirements:

- Fortran Compiler

### 2. Clone the Repository:

Clone the ForLAPACK repository from GitHub using the following command:

```shell
git clone --recurse-submodules https://github.com/gha3mi/forlapack.git
```

Change to the ForLAPACK directory:

```shell
cd forlapack
```

Get the Latest LAPACK Source Code:

```shell
git submodule update --init --recursive
```

### 3. Remove the `DEPRECATED` Directory:

Remove the `src/SRC/DEPRECATED` directory from LAPACK source code:

```shell
rm -r src/SRC/DEPRECATED
```

### 4. Copy `INSTALL` Directory:

Copy the `src/INSTALL` directory to the `src/SRC` directory:

```shell
cp -r src/INSTALL src/SRC
```

### 5. Install Using the Fortran Package Manager (fpm):

ForLAPACK can be built using [fpm](https://github.com/fortran-lang/fpm). Ensure that you have fpm installed and then execute the following command:

```shell
fpm install --profile release --prefix .
```
The compiled library can be found in the `lib` directory.

Adjust the installation directory, compiler, and flags as needed:

- Use `--prefix <dir>` to set the installation directory.
- Use `--compiler <compiler>` to specify your Fortran compiler.
- Use `--flag '<flags>'` to customize your compiler flags.

## ForBLAS

To install BLAS, use [ForBLAS](https://github.com/gha3mi/forblas).

## Contributing

Contributions to `ForLAPACK` are welcome! If you find any issues or would like to suggest improvements, please open an issue or submit a pull request.
