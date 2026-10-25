# Manic EMU iPhone Duo build candidate

This repository hosts a GitHub Actions workflow for rebuilding the official Manic EMU 2.0.1 Sideload target with an iOS 27.1 or newer SDK. It checks out upstream commit `fbaeab79c214d5920bb51afa6f2d786fb2b12a58` and its dependencies.

This is an experimental SDK rebuild, not a verified complete iPhone Duo port. Folding, unfolding, skins, touch alignment, orientation changes, JIT, and save compatibility require device testing. Upstream third-party service API keys are blank, so those integrations may be unavailable in a self-built app.

## Build

Open **Actions → Manic EMU Duo build candidate → Run workflow**. The workflow also starts when its own file changes. It stops if the selected runner has no iOS 27.1+ SDK. A successful run uploads `ManicEMU-Duo-candidate-unsigned`; failures may upload a separate build log. Artifacts expire after seven days.

The IPA is unsigned for installation through a suitable signing tool such as SideStore. Do not delete the existing app or its game data to test this candidate. Confirm the installed signing identity and app identifier before attempting an in-place update; back up saves first.

## Source

[Official Manic EMU repository](https://github.com/Manic-EMU/ManicEMU), licensed upstream under AGPL-3.0. Bundled dependencies retain their respective licenses. No ROMs, saves, Apple credentials, or signing certificates are supplied by this workflow.
