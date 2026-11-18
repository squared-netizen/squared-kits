# squared-kits

The kits of the [squared SDK](https://squared-netizen.github.io/squared-netizen/):
each one adds a capability to a squared project when sqpg creates it, or
when square adds it later. A kit is a bridge to something outside squared
(a library, a platform API) or a ready-made piece of a project.

**Status: being moved here.** The kits live in squared-pg's `resources/kits/`
today; this repository is their new home (phase 2 of the sqpg redesign).
Each will be released from here as a cartridge (`kit.lua-<version>.sq`), so
sqpg plans from a kit's manifest instead of carrying a copy of it.

| Kit | What it adds |
| --- | --- |
| `kit.edu_cpp` | four short C++ lessons for a teaching workspace; text only |
| `kit.imgui` | Dear ImGui with its OpenGL 3 backend, bridged to SFML's window and input |
| `kit.lua` | an embedded Lua 5.4 interpreter and an `sq_lua/` script workspace |
| `kit.opengl` | EGL context management and an OpenGL ES 3.0 surface for NativeActivity |
| `kit.sfml` | SFML's System, Window, Graphics and Audio, built static for Android |
| `kit.terminal` | a header of terminal utilities: console I/O, a small regex facade, a FileHandle |
| `kit.termux` | a header-only bridge to the Termux:API command-line tools |

A kit that outgrows this repository moves to one of its own.

## How a kit is laid out

Each kit is an exploded cartridge: a folder with `SQ-INF/manifest.json` in the
Squared Cartridge Specification's envelope, its files under `tree/`, and in
`consumers.squared_pg` its parameters and the ownership of every path it
writes. See sqcart's specification for the format.

## Licence

MIT: see [LICENSE](LICENSE). A kit that bundles a third-party library keeps
that library's licence beside it. Security issues: see
[SECURITY.md](SECURITY.md).
