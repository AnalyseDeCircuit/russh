# OxideTerm's russh fork

This repository contains the SSH library used by
[OxideTerm](https://github.com/AnalyseDeCircuit/oxideterm). It is based on
[upstream russh](https://github.com/warp-tech/russh) 0.63.0 at commit
`dbe2234491fcd50e0bf68438452932f918092fe0`.

The history was extracted from OxideTerm's `crates/russh` directory. Existing
protocol, compatibility, transfer and secret-handling patches are retained;
see [the patch inventory](OXIDETERM_PATCHES.md). The original Apache-2.0 license
and upstream contributor attribution remain in place.

OxideTerm consumes this repository through a full Git commit SHA in its Cargo
patch table. Updating this fork does not automatically update the application.

Build from this directory using `Cargo.toml`. `Cargo.toml.orig` is the upstream
package manifest preserved for provenance; its workspace references are not a
standalone build entry point. The application workspace's Clippy configuration
does not apply to this repository.

For a change, run the relevant library regression tests here, then verify the
pinned revision and SSH integration in OxideTerm. Keep the application's
`Cargo.lock` update together with its revision change.
