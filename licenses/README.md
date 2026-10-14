# Licences and source of the bundled programs

The I-Simpa Night Mode application (`app.exe`) is free to download and use; all rights reserved. The installer
also puts these separate programs in its `solvers\` folder. Each is under its own licence, and their source is
available as each licence requires.

| Program | What it is | Licence | Source |
|---|---|---|---|
| `spps.exe`, `classicalTheory.exe`, `preprocess.exe` | I-Simpa's SPPS and TCR solvers and their mesh preprocessor | GPL-3.0 | I-Simpa at tag [`v1.4.0_snapshot_14_01_2026`](https://github.com/Universite-Gustave-Eiffel/I-Simpa/tree/v1.4.0_snapshot_14_01_2026) (commit `929a5c8e5f590b189f29155faeff8670f3699479`), with the two patches in [`solver-source/`](solver-source/) applied in name order |
| `spps-gpu.exe` | SPPS for NVIDIA GPUs | GPL-3.0 | On request (see below) |
| `tetgen.exe` | TetGen 1.5.0, the tetrahedral mesher (WIAS Berlin, Hang Si) | AGPL-3.0 | [`solver-source/tetgen1.5.0.tar.gz`](solver-source/tetgen1.5.0.tar.gz), WIAS's own release, unmodified |
| `msvcp140.dll`, `vcruntime140.dll`, `vcruntime140_1.dll` | Microsoft Visual C++ runtime | Microsoft Visual C++ Redistributable licence | Redistributable binaries |

The two patches change how the solvers store surface-receiver data (a time bin for sound maps, and sparse
storage of their series).

Building the solvers: I-Simpa's own CMake project with `SKIPISIMPA=ON`, Visual Studio 2022 x64, Release; TetGen
1.5.0 with the same compiler settings as I-Simpa's own `tetgen` target.

**Source on request:** write to the address on the [GitHub profile](https://github.com/Burhanuddin98) or open an
[Issue](https://github.com/Burhanuddin98/I-Simpa_Cherry/issues), naming the program and the version. This offer
stands for three years from each release.

[`THIRD-PARTY-NOTICES.txt`](THIRD-PARTY-NOTICES.txt) is the full list of the open-source components inside
`app.exe` and their licence texts; the app shows the same under **Help, About**.

The full GPL-3.0 text: <https://www.gnu.org/licenses/gpl-3.0.txt>. The AGPL-3.0 text:
<https://www.gnu.org/licenses/agpl-3.0.txt>.
