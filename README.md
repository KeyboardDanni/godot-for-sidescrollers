
# Godot for Sidescrollers

![Screenshot of Gobold](https://raw.githubusercontent.com/KeyboardDanni/gobold/main/screenshot.png)

## What?

Godot for Sidescrollers is an unofficial fork of [Godot Engine](https://github.com/godotengine/godot) that aims to improve the experience of both making and playing 2D pixel art games.

## Why?

When it comes to making 2D games, Godot is a very capable tool. It offers pixel-based coordinates, which is useful for making sure all your art assets are using a consistent scale. It also has physics interpolation - a feature that isn't present in most engines - which allows you to take advantage of buttery-smooth high refresh rates while still maintaining the determinism that is important for many 2D action games.

Unfortunately, like any piece of software, there are bugs and other shortcomings. Patches are available for some of these, but they may not be in the latest stable release of Godot (or even merged into the latest git).

For the short term, Godot for Sidescrollers aims to bridge the gap by making these improvements available today in the latest stable release.

The project's longterm goal is for Godot for Sidescrollers to become redundant.

## How?

This project uses [git-assembler](https://www.thregr.org/wavexx/software/git-assembler/) to simplify merging patches on top of the latest stable release by allowing each patch to be in a separate branch, so they can all be merged into a fresh branch without complicating the revision history.

The actual scripts for this are found in the `main` branch.

The generated `gfs_patched` branch should not be modified directly, as git-assembler will overwrite its history. Changes should instead be made on patch branches and then added as merge steps inside the `assembly` file.

## Which version?

Godot for Sidescrollers is currently patched against **4.4.1 stable**.

## Which patches are included?

Generally speaking, Godot for Sidescrollers tries to avoid making breaking changes where possible. A project created in vanilla Godot should be able to open fine in Godot for Sidescrollers, and a project made in GfS should work in vanilla with only small changes, if any.

Therefore, compatibility-preserving bugfixes, small (non-asset-related) features, and editor workflow improvements are all good candidates for inclusion.

A list of patches can be found in `PATCHES.md`.

## Licensing

Code for the patches is licensed under the MIT License, the [same licensed used by Godot](https://github.com/godotengine/godot/blob/master/LICENSE.txt).



# Godot Engine

<p align="center">
  <a href="https://godotengine.org">
    <img src="logo_outlined.svg" width="400" alt="Godot Engine logo">
  </a>
</p>

## 2D and 3D cross-platform game engine

**[Godot Engine](https://godotengine.org) is a feature-packed, cross-platform
game engine to create 2D and 3D games from a unified interface.** It provides a
comprehensive set of [common tools](https://godotengine.org/features), so that
users can focus on making games without having to reinvent the wheel. Games can
be exported with one click to a number of platforms, including the major desktop
platforms (Linux, macOS, Windows), mobile platforms (Android, iOS), as well as
Web-based platforms and [consoles](https://docs.godotengine.org/en/latest/tutorials/platform/consoles.html).

## Free, open source and community-driven

Godot is completely free and open source under the very permissive [MIT license](https://godotengine.org/license).
No strings attached, no royalties, nothing. The users' games are theirs, down
to the last line of engine code. Godot's development is fully independent and
community-driven, empowering users to help shape their engine to match their
expectations. It is supported by the [Godot Foundation](https://godot.foundation/)
not-for-profit.

Before being open sourced in [February 2014](https://github.com/godotengine/godot/commit/0b806ee0fc9097fa7bda7ac0109191c9c5e0a1ac),
Godot had been developed by [Juan Linietsky](https://github.com/reduz) and
[Ariel Manzur](https://github.com/punto-) (both still maintaining the project)
for several years as an in-house engine, used to publish several work-for-hire
titles.

![Screenshot of a 3D scene in the Godot Engine editor](https://raw.githubusercontent.com/godotengine/godot-design/master/screenshots/editor_tps_demo_1920x1080.jpg)

## Getting the engine

### Binary downloads

Official binaries for the Godot editor and the export templates can be found
[on the Godot website](https://godotengine.org/download).

### Compiling from source

[See the official docs](https://docs.godotengine.org/en/latest/contributing/development/compiling)
for compilation instructions for every supported platform.

## Community and contributing

Godot is not only an engine but an ever-growing community of users and engine
developers. The main community channels are listed [on the homepage](https://godotengine.org/community).

The best way to get in touch with the core engine developers is to join the
[Godot Contributors Chat](https://chat.godotengine.org).

To get started contributing to the project, see the [contributing guide](CONTRIBUTING.md).
This document also includes guidelines for reporting bugs.

## Documentation and demos

The official documentation is hosted on [Read the Docs](https://docs.godotengine.org).
It is maintained by the Godot community in its own [GitHub repository](https://github.com/godotengine/godot-docs).

The [class reference](https://docs.godotengine.org/en/latest/classes/)
is also accessible from the Godot editor.

We also maintain official demos in their own [GitHub repository](https://github.com/godotengine/godot-demo-projects)
as well as a list of [awesome Godot community resources](https://github.com/godotengine/awesome-godot).

There are also a number of other
[learning resources](https://docs.godotengine.org/en/latest/community/tutorials.html)
provided by the community, such as text and video tutorials, demos, etc.
Consult the [community channels](https://godotengine.org/community)
for more information.

[![Code Triagers Badge](https://www.codetriage.com/godotengine/godot/badges/users.svg)](https://www.codetriage.com/godotengine/godot)
[![Translate on Weblate](https://hosted.weblate.org/widgets/godot-engine/-/godot/svg-badge.svg)](https://hosted.weblate.org/engage/godot-engine/?utm_source=widget)
[![TODOs](https://badgen.net/https/api.tickgit.com/badgen/github.com/godotengine/godot)](https://www.tickgit.com/browse?repo=github.com/godotengine/godot)
