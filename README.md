# CV

My Curriculum Vitae, maintained as a LaTeX document in a GitHub repository. This
repository leverages [GitHub Workflows](./.github/workflows/) and
[Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/) to
automatically build, version, and release my CV with a changelog on GitHub.

This project started as a (_slightly ridiculous_) idea that I had to demonstrate
my experience both on paper, and practically through the management of GitHub
repository, in a way that I thought would stand out. Check the
[releases](https://github.com/NathanielJS1541/CV/releases) section for the
latest version of my CV in `.pdf` form, along with a changelog.

The generated version numbers conform to the
[semantic versioning specification](https://semver.org/) but each digit is used
to reflect my career progression, backed by the conventional commit types and
scopes defined in [CONTRIBUTING.md](./CONTRIBUTING.md#conventional-commits):

- The **major** version is used to indicate changes of employer. This is
  reflected by a [breaking change](./CONTRIBUTING.md#breaking-changes) commit,
  which should be a `feat!` [type](./CONTRIBUTING.md#types) as it will require a
  new document section.
- The **minor** version is used to indicate changes of role at a particular
  employer. This is reflected by the `feat` commit
  [type](./CONTRIBUTING.md#types), as it requires a new sub-section to be added
  under the current employer section.
- The **patch** version is used for any changes that represent no change of role
  or employer. This includes the `fix` commit [type](./CONTRIBUTING.md#types)
  (for any edits and re-writes), and any of the other defined commit
  [types](./CONTRIBUTING.md#types) for general repo maintenance (i.e. `ci`,
  `docs`, `style`, etc.).

<!-- omit from toc -->
## Contents

- [Repository Structure](#repository-structure)
- [Release Strategy](#release-strategy)
- [Contributing](#contributing)
  - [IDE](#ide)
  - [Conventional Commits](#conventional-commits)
- [Licenses](#licenses)
  - [License Coverage](#license-coverage)
  - [Primary MIT License](#primary-mit-license)
  - [CC-BY-NC-ND-4.0 CV Contents License](#cc-by-nc-nd-40-cv-contents-license)
  - [What This Means For You](#what-this-means-for-you)

## Repository Structure

```text
CV                               # Repository root.
 ├─ .github/                     # GitHub files i.e. workflows, templates, etc.
 ├─ .vscode/                     # VSCode shared workspace files.
 ├─ build/                       # Build output directory (local only!).
 ├─ front_matter/                # .tex files defining the front matter.
 ├─ images/                      # Image files used in figures.
 ├─ preamble/                    # .tex files defining the preamble contents.
 ├─ sections/                    # .tex files defining the document sections.
 ├─ .gitignore                   # .gitignore file.
 ├─ cliff.toml                   # git-cliff configuration file.
 ├─ CONTRIBUTING.md              # Contribution styles and guidelines.
 ├─ LICENSE                      # Primary license for the repository.
 ├─ main.tex                     # Main entry point for the .tex document.
 └─ README.md                    # Main repository README (You are here!).
```

## Release Strategy

The workflows within this repo are set up to create a release whenever any
changes are pushed to `main`. The document version will be automatically bumped
based on the conventional commits, and releases and changelogs will
automatically be published to GitHub.

## Contributing

The [CONTRIBUTING.md](./CONTRIBUTING.md) document details the contribution
styles I will be using for this document, and also contains guidance for
building the document locally.

### IDE

This document is designed around the use of
[VSCode](https://code.visualstudio.com/) as an IDE since it is freely available
and relatively easy to use.

To configure [VSCode](https://code.visualstudio.com/) for use with LaTeX, see
the [VSCode Setup section of CONTRIBUTING.md](./CONTRIBUTING.md#vscode-setup).

### Conventional Commits

This repository uses
[Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/) to allow
automatic versioning and changelog generation.

See [CONTRIBUTING.md](./CONTRIBUTING.md) for the commit
[types](./CONTRIBUTING.md#types) and [scopes](./CONTRIBUTING.md#scopes) defined
for this repository.

## Licenses

The contents of this repository are licensed under **multiple licenses**. Most
of the repository is licensed under the [primary MIT license](./LICENSE), but
some directories are licensed under separate licenses, and not covered under the
[primary MIT license](./LICENSE).

I have done this to allow all "reusable" parts of this repo (i.e. the
[workflows](./.github/workflows/) and the files from my
[LaTeX template](https://github.com/NathanielJS1541/LaTeX_Template)) to benefit
others by allowing modification, redistribution, and commercial use under a more
permissive [MIT License](./LICENSE), while personalised material (i.e. the
main CV [contents](./sections/)) is not available for modification,
redistribution, or commercial use. See the [License Coverage](#license-coverage)
section for more detail about the different licenses within the repo.

### License Coverage

Any directories containing a separate `LICENSE` file are covered by that license
_only_, and not under the [primary MIT license](./LICENSE). This license also
applies **recursively to all subdirectories** and contents.

In the absence of a directory explicitly providing a different `LICENSE` file,
its contents are covered by the [primary MIT license](./LICENSE).

The following licenses are used in addition to the
[primary MIT license](./LICENSE):

- The contents of the [sections](./sections/) directory are covered by a
  [`CC-BY-NC-ND-4.0` license](./sections/LICENSE).

### Primary MIT License

```
SPDX-License-Identifier: MIT
```

The primary license is an [MIT license](https://mit-license.org/), and is stored
in the [main LICENSE file](./LICENSE) of the repo. This is a permissive license
that allows modification and redistribution of the files it covers, conforming
to the license of the
[template](https://github.com/NathanielJS1541/LaTeX_Template) this repo was
created from, and allowing others to create their own forks or derivative works.

### CC-BY-NC-ND-4.0 CV Contents License

```
SPDX-License-Identifier: CC-BY-NC-ND-4.0
```

The actual "contents" of the CV (contained in the
[sections directory](./sections/)) are personal to me, and as such are covered
by a "Creative Commons Attribution Non Commercial No Derivatives 4.0
International" [license](./sections/LICENSE).

This license has been chosen as it protects the personal contents of my CV, but
is scoped only to that directory to allows others to modify the
[MIT-licensed](./LICENSE) sections to create their own documents, provided the
contents of the [sections directory](./sections/) are removed in entirety and
not redistributed.

For guidance when forking or redistributing this repo specific to the
[CC-BY-NC-ND-4.0](./sections/LICENSE) license, see
[the license portion of the sections README](./sections/README.md#license).

### What This Means For You

- You may freely use, fork, modify, and redistribute the contents of this repo
  covered by the [MIT license](./LICENSE), providing that you include a copy of
  the [LICENSE](./LICENSE) file and keep the copyright notice intact.
- Any licenses explicitly defined within directories of this repo **must** be
  obeyed for the entire directory contents, including subdirectories
  (recursively).
- If you wish to modify, redistribute, or use the [MIT-licensed](./LICENSE),
  sections for commercial purposes, you must remove any directories (such as
  [sections](./sections/)) where the licenses do not allow modification,
  redistribution, or commercial use. Always check the
  [coverage](#license-coverage) and conditions of other licenses before creating
  modified versions of this repo or document.
