# Release Notes Schema Specification

## About

The goal of this repository is to work out an **easy to use**,
**human readable** and **machine processable** schema for release notes.

Currently most of the open source projects out there do not provide
details of what was added or what has changed when they release a new
version.

## Why should I care about release notes?

Because this is an easy way for other people to keep track on what has
changed in your software.
[Semantic Versioning](http://semver.org) is a great commitment on
building compatible components in a distributed open source world.
**BUT** it will not tell your dependents whether they have to urgently
upgrade to the next compatible version, eg. in case of an security fix.


## The Specification

The release notes MUST be defined in a `release-notes.yml` file,
on project root.

The format of that file MUST be [YAML](http://www.yaml.org/spec/1.2/spec.html).

The document MUST provide a **title**.

The document SHOULD provide a **description**.

The document MUST prodive **releases**, an array of `ReleaseDetails`.

The releases SHOULD be ordered, the latest release comes first.

A release MUST provide a **version**.

A release MUST provide a **date** of type `ISODate` or `ISODateTime`.

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

## Related Projects

- [keep a changelog](http://keepachangelog.com)
- [vandamme - A Changelog parser](https://github.com/tech-angels/vandamme/)

---

LICENSE

The files in this archive are released under MIT license.
You can find a copy of this license in [LICENSE](LICENSE).
