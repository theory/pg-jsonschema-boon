# Changelog

All notable changes to this project will be documented in this file. It uses the
[Keep a Changelog] format, and this project adheres to [Semantic Versioning].

  [Keep a Changelog]: https://keepachangelog.com/en/1.1.0/
  [Semantic Versioning]: https://semver.org/spec/v2.0.0.html
    "Semantic Versioning 2.0.0"

## [v0.1.9] — Unreleased

### ⬆️ Dependency Updates

*   Upgraded dependencies, notably the bytes package (CVE-2026-25541).

## [v0.1.8] — 2025-09-26

### ⬆️ Dependency Updates

*   Upgraded pgrx to v0.16.1 to support PostgreSQL 18
*   Upgraded all other dependencies

  [v0.1.8]: https://github.com/theory/pg-jsonschema-boon/compare/v0.1.7...v0.1.8

## [v0.1.7] — 2025-05-30

### ⬆️ Dependency Updates

*   Upgraded pgrx to v0.14.3
*   Upgraded all other dependencies

### 📔 Notes

*   Dropped support for Postgres 12 (no longer supported by pgrx).
*   Removed the `$libdir/` prefix from `module_pathname`, so if the module is
    installed elsewhere in `dynamic_library_path` Postgres will be able to
    find it.
*   Moved from the `tembo-io` org to `theory` on GitHub.
*   Reduced memory overhead of some error values, as suggested by the Rust
    1.87.0 linter.

  [v0.1.7]: https://github.com/theory/pg-jsonschema-boon/compare/v0.1.6...v0.1.7

## [v0.1.6] — 2025-02-25

### ⬆️ Dependency Updates

*   Upgraded pgrx to v0.13.0
*   Upgraded all other dependencies
*   Added missing v0.1.5 upgrade file

  [v0.1.6]: https://github.com/theory/pg-jsonschema-boon/compare/v0.1.5...v0.1.6

## [v0.1.5] — 2025-01-08

### ⬆️ Dependency Updates

*   Upgraded boon to v0.6.1 to mitigate vulnerabilities in its dependencies.
*   Upgraded all other dependencies

  [v0.1.5]: https://github.com/theory/pg-jsonschema-boon/compare/v0.1.4...v0.1.5

## [v0.1.4] — 2024-12-04

### ⬆️ Dependency Updates

*   Upgraded pgrx to v0.12.9
*   Upgraded all other dependencies

  [v0.1.4]: https://github.com/theory/pg-jsonschema-boon/compare/v0.1.3...v0.1.4

## [v0.1.3] — 2024-10-03

### ⬆️ Dependency Updates

*   Upgraded pgrx to v0.12.5 with support for the Postgres 17.0 release
*   Upgraded all other dependencies

  [v0.1.3]: https://github.com/theory/pg-jsonschema-boon/compare/v0.1.2...v0.1.3

## [v0.1.2] — 2024-08-26

### ⬆️ Dependency Updates

*   Upgraded pgrx to v0.12.1

### ⚡ Improvements

*   Made the extension relocatable

### 📔 Notes

*   Dropped support for Postgres 11 (no longer supported by pgrx).
*   Added support for Postgres 17.

  [v0.1.2]: https://github.com/theory/pg-jsonschema-boon/compare/v0.1.1...v0.1.2

## [v0.1.1] — 2024-06-12

The theme of this release is *fast follows.*

### ⬆️ Dependency Updates

*   Upgraded boon to v0.6.

### ⚡ Improvements

*   Removed custom schema loader, taking advantage of the feature of boon v0.6
    to remove all loaders (santhosh-tekuri/boon#12).

  [v0.1.1]: https://github.com/theory/pg-jsonschema-boon/compare/v0.1.0...v0.1.1

## [v0.1.0] — 2024-04-30

The theme of this release is *learning Rust and pgrx.*

### ⚡ Improvements

*   First release, everything is new!
*   JSON Schema validation using [boon]
*   Fully supports draft 2020-12, draft 2019-09, draft-7, draft-6, and draft-4
*   Multi-object schema composition
*   Remote fetching of resources disabled

### 🏗️ Build Setup

*   Built with Rust
*   Use `make` for most actions
*   Download from [PGXN] or [GitHub]
*   [CI testing] on PostgreSQL 11--16

### 📚 Documentation

*   Build and install docs in the [README]
*   Full [reference documentation]
*   Performance [benchmark script]
*   Multi-schema [composition example]

  [v0.1.0]: https://github.com/theory/pg-jsonschema-boon/compare/34d5d49...v0.1.0
  [boon]: https://github.com/santhosh-tekuri/boon
  [README]: https://github.com/theory/pg-jsonschema-boon/blob/v0.1.0/README.md
  [PGXN]: https://pgxn.org/dist/jsonschema/
  [GitHub]: https://github.com/theory/pg-jsonschema-boon/releases
  [reference documentation]: https://github.com/theory/pg-jsonschema-boon/blob/v0.1.0/doc/jsonschema.md
  [benchmark script]: https://github.com/theory/pg-jsonschema-boon/blob/v0.1.0/eg/bench.sql
  [composition example]: https://github.com/theory/pg-jsonschema-boon/blob/v0.1.0/eg/user.sql
  [CI testing]: https://github.com/theory/pg-jsonschema-boon/actions/workflows/lint-and-test.yml
