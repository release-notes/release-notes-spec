# Release Notes Schema Specification

[![Subscribe to Release Notes](https://release-notes.com/badges/v1.svg)](https://release-notes.com/@release-notes/release-notes-spec)

## About

The goal of this repository is to work out an **easy to use**,
**human readable** and **machine processable** YAML schema specification for release notes.

## The Specification

The key words “MUST”, “MUST NOT”, “REQUIRED”, “SHALL”, “SHALL NOT”, “SHOULD”, “SHOULD NOT”, “RECOMMENDED”, “MAY”, and “OPTIONAL” in this document are to be interpreted as described in [RFC 2119](http://tools.ietf.org/html/rfc2119).

The release notes MUST be defined in a `release-notes.yml` file on project root.

The format of that file MUST be [YAML](http://www.yaml.org/spec/1.2/spec.html).

The document MUST provide a **title**.

The document SHOULD provide a **description**.

The document MUST prodive **releases**, an array of `ReleaseDetails`.

The releases SHOULD be ordered, the latest release comes first.

A release MUST provide a **version**.

A release MUST provide a **date** of type `ISODate` or `ISODateTime`.

A release MAY provide a **title**.

A release SHOULD provide a **description**.

### The Upcoming Release

An upcoming release MUST have the version set to `Unreleased`,
`Next` or `Upcoming`.

The upcoming release MAY omit the **date** info.

### Modification Types

A release MAY provide a list of **added** functionality.

A release MAY provide a list of **removed** functionailty.

A release MAY provide a list of **changed** functionailty.

A release MAY provide a list of **improved** functionality.

A release MAY provide a list of **deprecated** functionality.

A release MAY provide a list of **fixed** functionality.

A release MAY provide a list of **secured** fixes.

All modification list items MUST be either string or an object with a
**title** property.

### Tags

A modification in object notation MAY provide a list of **tags**.
Each tag MUST be a string that SHOULD be treated case insensitive.


## Example

```yaml
title: Release Notes of an awesome project
description: >
  Awesome project makes your cli a better place.

releases:
- version: Unreleased
  added:
  - Add more fancy stuff.
  deprecated:
  - Deprecate some "not so awesome" command.
- version: 0.1.1
  date: 2017-10-30
  fixed:
  - title: Do not crash on win32.
    tags: ["Windows"]
- version: 0.1.0
  date: 2017-10-30
  description: The first release
  added:
  - Introduce some awesomeness.
```

## Project Repositories

The Release Notes project consists of the following repositories:
   
- [Release Notes Hub](https://github.com/release-notes/release-notes-hub)
- [Release Notes CLI Tool](https://github.com/release-notes/release-notes-cli)
- [Release Notes Node.js lib](https://github.com/release-notes/release-notes-node)
- [Release Notes Specification](https://github.com/release-notes/release-notes-spec)
- [Release Notes JSON-Schema Definitions](https://github.com/release-notes/release-notes-schema)

---

### LICENSE

The files in this archive are released under MIT license.
You can find a copy of this license in [LICENSE](LICENSE).
