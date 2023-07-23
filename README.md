# ForLAPACK

![ForLAPACK](media/logo.png)

## How to Use ForLAPACK

### Adding ForLAPACK as an fpm Dependency

If you want to use ForLAPACK as a dependency in your own fpm project,
you can easily include it by adding the following line to your `fpm.toml` file:

```toml
[dependencies]
forlapack = {git="https://github.com/gha3mi/forlapack.git"}
```

### Installation of ForLAPACK Library

To use ForLAPACK, follow the steps below:

- **Reuirements:**

  Fortran Compiler

- **Clone the repository:**

   You can clone the ForLAPACK repository from GitHub using the following command:

   ```shell
   git clone https://github.com/gha3mi/forlapack.git
   ```

   ```shell
   cd forlapack
   ```

- **Build using the Fortran Package Manager (fpm):**

   ForLAPACK can be built using [fpm](https://github.com/fortran-lang/fpm).
   Make sure you have fpm installed, and then execute the following command:

  **GNU Fortran Compiler (gfortran)**

   ```shell
   fpm install --prefix . --compiler gfortran "flag -O3 -frecursive"
   ```

## Contributing

Contributions to `ForLAPACK` are welcome!
If you find any issues or would like to suggest improvements,
please open an issue or submit a pull request.
