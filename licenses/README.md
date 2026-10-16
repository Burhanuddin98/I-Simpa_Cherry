# Licences and source of the bundled programs

The I-Simpa Cherry application (`app.exe`) is free to download and use; all rights reserved. The installer
also puts these separate programs in its `solvers\` folder. Each is under its own licence.

| Program | What it is | Licence |
|---|---|---|
| `spps.exe`, `classicalTheory.exe`, `preprocess.exe` | I-Simpa's SPPS and TCR solvers and their mesh preprocessor (Université Gustave Eiffel) | GPL-3.0-or-later |
| `spps-gpu.exe` | SPPS ported to NVIDIA GPUs | GPL-3.0-only |
| `tetgen.exe` | TetGen 1.5.0, the tetrahedral mesher (WIAS Berlin, Hang Si) | AGPL-3.0 |
| `msvcp140.dll`, `vcruntime140.dll`, `vcruntime140_1.dll`, `vcomp140.dll` | Microsoft Visual C++ runtime | Microsoft Visual C++ redistributable terms |

**Their complete source** is published with every release, beside the installer: the file
`i-simpa-cherry-<version>-solver-source.zip` on the [releases page](https://github.com/Burhanuddin98/I-Simpa_Cherry/releases).
It holds I-Simpa at the exact commit the solvers are built from (tag `v1.4.0_snapshot_14_01_2026`, commit
`929a5c8e5f590b189f29155faeff8670f3699479`), the two patches applied to it (also in [`solver-source/`](solver-source/)),
the source of `spps-gpu.exe`, TetGen 1.5.0 as released by WIAS, the build scripts, and instructions to build each
program.

The two patches change how the solvers store surface-receiver data: a time bin for sound maps, and sparse storage
of their series.

[`THIRD-PARTY-NOTICES.txt`](THIRD-PARTY-NOTICES.txt) lists the open-source components inside `app.exe` and the
shipped example rooms, with their licence texts; the app shows the same under **Help, About**.

Licence texts: GPL-3.0 <https://www.gnu.org/licenses/gpl-3.0.txt>, AGPL-3.0
<https://www.gnu.org/licenses/agpl-3.0.txt>; both also ship inside the installer and the source archive.
