## v0.5.0 to-be-released

### Added

* Mappers support tuple transformation using wrap and group operations (solnic)

### Changed

* `ROM::RA` interface is no longer mixed into relations by default (solnic)

## v0.4.1 2014-12-15

### Added

* Adapter can now implement `Adapter#dataset(name, header)` to return a dataset (solnic)
* For multi-step setup the DSL is available in `ROM` too (solnic)
* Global environment can be stored via `ROM.finalize` and accessible via `ROM.env` (solnic)
* Mapper won't infer attributes from the header if `:inherit_header` option is set to false (solnic)

### Changed

* Schema can be defined in multiple steps (solnic)
* Setting model in mapper DSL is no longer required and defaults to `Hash` (solnic)
* Adapter datasets no longer have to return headers when they are provided by schema (solnic)

[Compare v0.4.0...v0.4.1](https://github.com/rom-rb/rom/compare/v0.4.0...v0.4.1)

## v0.4.0 2014-12-06

### Added

* Command API (solnic)
* Setup DSL is now available within the `ROM.setup` block (solnic)
* Support for setting up a logger for an adapter (solnic)
* New `Adapter#dataset?(name)` which every adapter must implement (solnic)

### Fixed

* method-missing in `Repository` and `Env` kindly calls `super` (solnic)

### Changed

* Abstract `Adapter` defines `:connection` reader so it doesn't have to be
  defined in adapter descendants (solnic)

[Compare v0.3.1...v0.4.0](https://github.com/rom-rb/rom/compare/v0.3.1...v0.4.0)

## v0.3.1 2014-11-25

### Added

* attributes for `group` mapping operation can be specified without options (solnic)
* attributes for `wrap` mapping operation can be specified without options (solnic)
* `Env` uses Equalizer (solnic)
* boot dsl methods return self (solnic)

### Fixed

* when schema is missing booting will gracefuly skip building relations and mappers (solnic)
* in-memory join handles one-to-many and many-to-one correctly (solnic)

[Compare v0.3.0...v0.3.1](https://github.com/rom-rb/rom/compare/v0.3.0...v0.3.1)

## v0.3.0 2014-11-24

This version is a rewrite that introduces a new, simplified architecture based
on a new adapter interface.

[Compare v0.2.0...v0.3.0](https://github.com/rom-rb/rom/compare/v0.2.0...v0.3.0)

## v0.2.0 2014-04-06

### Added

* [feature] added :rename option to schema attribute DSL (solnic)
* [feature] added support for join, group, wrap, project and rename operations (solnic)
* [feature] added support for setting domain object loading strategy (solnic)
* [feature] Environment.setup can be used with a block to define schema and mapping (solnic)
* [feature] added public interface for building mappers (see Mapper.build) (solnic)
* [feature] added support for mapping embedded objects using wrap/group (solnic)
* [feature] environment exposes mapper registry via Environment#mappers (solnic)

### Changed

* [BREAKING] rom-relation, rom-mapper and rom-session were merged into rom project (solnic)
* [BREAKING] changed mapping DSL (users do...end => relation(:users) do...end) (solnic)
* [BREAKING] added :from option to mapping DSL which replaced :to (solnic)
* [internal] mappers are now backed by [morpher](https://github.com/mbj/morpher) (solnic)
* [internal] renaming and optimizing relations happens on the schema level now (solnic)
* [internal] environment will raise if unknown relation is referenced via `Environment#[]` (solnic)

[Compare v0.1.2...v0.2.0](https://github.com/rom-rb/rom/compare/v0.1.2...v0.2.0)

## v0.1.2 2013-09-02

* [updated] [rom-relation](https://github.com/rom-rb/rom-relation/blob/v0.1.2/Changelog.md#v012-2013-09-02)

[Compare v0.1.1...v0.1.2](https://github.com/rom-rb/rom/compare/v0.1.1...v0.1.2)

## v0.1.1 2013-08-30

* [updated] [rom-relation](https://github.com/rom-rb/rom-relation/blob/v0.1.1/Changelog.md#v011-2013-08-30)
* [updated] [rom-session](https://github.com/rom-rb/rom-session/blob/v0.1.1/Changelog.md#v011-2013-08-30)

[Compare v0.1.0...v0.1.1](https://github.com/rom-rb/rom/compare/v0.1.0...v0.1.1)

## v0.1.0 2013-08-23

First public release
