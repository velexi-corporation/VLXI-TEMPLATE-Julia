Velexi Julia Project Cookiecutter
=================================

--------------------------------------------------------------------------------------------

Table of Contents
-----------------

1. [Overview][#1]

    1.1. [Repository Contents][#1.1]

    1.2. [Software Dependencies][#1.2]

    1.3. [License][#1.3]

2. [Quick Start][#2]

3. [Documentation][#3]

--------------------------------------------------------------------------------------------

## 1. Overview

The [Velexi Julia Project Cookiecutter][github-vlxi-cookiecutter-julia] is intended to
streamline the process of setting up a Julia project with Velexi's default configuration
choices for the following:

* license,

* Git,

* continuous integration (CI), and

* code coverage tracking.

The `templates` directory contains files that are customizations of the default
configurations generated by `PkgTemplates`, such as

* modifications of GitHub Actions workflow configurations,

* structure for `src` directory

* sample `runtests.jl` based on the `TestTools` package.

### 1.1. Repository Contents

```
├── README.md          <- this file
├── NEWS.md            <- cookiecutter release notes
├── LICENSE            <- cookiecutter license
├── bin/               <- cookiecutter CLI tools
├── docs/              <- cookiecutter documentation and other helpful documents
└── templates/         <- example and template files
```

### 1.2. Software Dependencies

* Julia (>=1.6)

### 1.3. License

The contents of this cookiecutter are covered under the Apache License 2.0 (included in the
`LICENSE` file). The copyright for this cookiecutter is contained in the `NOTICE` file.

--------------------------------------------------------------------------------------------

## 2. Quick Start

1. Clone this repository.

   ```shell
   $ git clone https://github.com/velexi-corporation/VLXI-Cookiecutter-Julia.git
   ```

2. Use the `create-project` CLI tool to create a new empty Julia project. In the following
   command, replace `PROJECT_NAME` with the name of the new Julia project.

   ```shell
   $ bin/create-project PROJECT_NAME
   ```

   __Notes__

   * The `create-project` CLI tool supports several command-line options. Use
     `create-project --help` to see a full list of options.

   * The directory containing the new Julia project is relocateable. It has no dependency
     on this cookiecutter package.

3. Verify the copyright year and owner in the copyright notice created by `create-project`.
   If the project is licensed under Apache License 2.0, the copyright notice is located in
   the `NOTICE` file. Otherwise, the copyright notice is located in the `LICENSE` file.

4. (OPTIONAL) Replace auto-generated project files with custom versions based on files in
   the `templates` directory.

--------------------------------------------------------------------------------------------

## 3. Documentation

* [Julia Packaging Guide](docs/Julia-Packaging-Guide.md)

* [Velexi Julia Code Structure and Style Conventions](docs/Velexi-Julia-Code-Structure-and-Style-Conventions.md)

* [Template Documentation](templates/README.md)

--------------------------------------------------------------------------------------------

[------------------------------------INTERNAL LINKS------------------------------------]: #

[#1]: #1-overview
[#1.1]: #11-repository-contents
[#1.2]: #12-software-dependencies
[#1.3]: #13-license

[#2]: #2-quick-start

[#3]: #3-documentation

[------------------------------------- REFERENCES -------------------------------------]: #

[github-vlxi-cookiecutter-julia]: https://github.com/velexi-corporation/VLXI-Cookiecutter-Julia
