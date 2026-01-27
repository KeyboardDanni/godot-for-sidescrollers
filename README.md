
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

The actual scripts for this are found in the `scripts` branch.

The generated `gfs_patched` branch should not be modified directly, as git-assembler will overwrite its history. Changes should instead be made on patch branches and then added as merge steps inside the `assembly` file.

Special thanks to [fire](https://github.com/fire) for guiding me toward this workflow. He's a developer for the [V-Sekai](https://github.com/V-Sekai) social VR project, which maintains its own Godot fork. Go check it out!

## Which version?

Godot for Sidescrollers is currently patched against **4.6 stable**.

## Which patches are included?

Generally speaking, Godot for Sidescrollers tries to avoid making breaking changes where possible. A project created in vanilla Godot should be able to open fine in Godot for Sidescrollers, and a project made in GfS should work in vanilla with only small changes, if any.

Therefore, compatibility-preserving bugfixes, small (non-asset-related) features, and editor workflow improvements are all good candidates for inclusion.

A list of patches can be found in `PATCHES.md`.

## Licensing

Code for the patches is licensed under the MIT License, the [same license used by Godot](https://github.com/godotengine/godot/blob/master/LICENSE.txt).
