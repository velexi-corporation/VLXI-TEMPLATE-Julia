Velexi Template: Julia Package (v0.1.4)
=======================================

___Authors___  
Kevin T. Chu `<kevin@velexi.com>`

------------------------------------------------------------------------------

Contents
--------

1. [Overview][#1]

    1.1. [Software Dependencies][#1.1]

    1.2. [Directory Structure][#1.2]

2. [Usage][#2]

    2.1. [Setting Up][#2.1]

    2.2. [Running Tests][#2.2]

    2.3. [Cleaning the Project Directory][#2.3]

------------------------------------------------------------------------------

## 1. Overview

This package template is intended to

* streamline the process of setting up a Julia package and

* provide a collection of tools to support Julia software development (e.g.,
  analysis of unit test coverage).

### 1.1. Software Dependencies

#### Base Requirements

* Julia (>=1.4)
* git

#### Julia Packages ####

See `[deps]` section of the following `Project.toml` files:

* `Project.toml` (generated by `init-pkg.jl` script)
* `bin/Project.toml`
* `test/Project.toml`

Note that all package dependencies are automatically installed by the Julia
package manager.

### 1.2. Directory Structure

    README.md
    LICENSE
    Makefile
    bin/
    src/
    test/
    template-docs/
    template-docs/examples

* `README.md`: this file (same as `template-docs/README-Template-Usage.md`)

* `LICENSE`: license file for this package template (same as
  `template-docs/LICENSE-Julia-Template`)

* `Makefile`: Makefile defining a collection of useful commands to maintain
  software (e.g., `test`, `clean`)

* `bin`: directory containing command-line utilities

    * `init-pkg.jl`: utility to initialize Julia package
    * `coverage.jl`: utility to analyze test coverage

* `src`: directory for source code

    * `ExampleModule.jl` is an example Julia module.
    * `ExampleType.jl` is an example source file for defining a type.
    * `ExampleMethods.jl` is an example source file for defining methods.

* `test`: directory for test code

    * `Example_tests.jl` contains example unit tests.
    * `runtests.jl` is an example test setup file.
    * `Project.toml` contains package dependencies for running unit tests.

* `template-docs`: directory containing documentation this package template.

* `template-docs/examples`: directory containing example and template files.

    * Example and template files are indicated by the `example` and `template`
      suffixes, respectively. These files are intended to simplify the set up
      of package. When appropriate, they should be renamed (with the `example`
      or `template` suffix removed).

------------------------------------------------------------------------------

## 2. Usage

### 2.1. Setting Up

* (OPTIONAL) Configure `direnv`.

    * Copy `template-docs/examples/envrc.example` to the package root directory
      and rename it to `.envrc`.

    * Follow `direnv` instructions to enable `.envrc` file.

* From the package root directory, use `make setup` to add the Julia packages
  required to set up the development environment.

  ```shell
  $ cd PKG_ROOT_DIR
  $ make setup
  ```

* Initialize Julia package.

    * Use the `init-pkg.jl` utility to initialize the package. In the following
      command, replace `PKG_NAME` with the name of your package.

      ```shell
      $ bin/init-pkg.jl PKG_NAME
      ```

      Note that `init-pkg.jl` supports several command-line options. To see the
      full list of options, use `init-pkg.jl --help`.

    * Update template files in the `src` and `test` directories to be
      consistent with `PKG_NAME`.

      * Replace all references to the `ExampleModule` module to `PKG_NAME` in
        filenames and source code.

* Replace the `README.md` and `LICENSE` files with package-specific versions.
  Templates are available in the `template-docs/examples` directory.

### 2.2. Running Tests

* Use `make` to run the unit tests and display coverage information.

  ```shell
  $ make
  ```

  Note that `test` is the default Make target, so `make test` will achieve the
  same result.

### 2.3. Cleaning the Package Directory

* Use `make clean` to automatically remove files and directories generated
  during setup or testing (e.g., temporary directories, coverage files).

  ```shell
  $ make clean
  ```

------------------------------------------------------------------------------

[-----------------------------INTERNAL LINKS-----------------------------]: #

[#1]: #1-overview
[#1.1]: #11-software-dependencies
[#1.2]: #12-directory-structure

[#2]: #2-usage
[#2.1]: #21-setting-up
[#2.2]: #22-running-tests
[#2.3]: #23-cleaning-the-package-directory

[#3]: #3-references
