# I-Simpa Night Mode

A new desktop application for room-acoustics simulation, built on the solvers of
[I-Simpa](https://github.com/Universite-Gustave-Eiffel/I-Simpa) (Université Gustave Eiffel): SPPS particle
tracing and TCR classical theory, plus SPPS on NVIDIA GPUs.

Free to download and use. Windows 10 and 11, 64-bit.

## Download

**[Download the latest version](https://github.com/Burhanuddin98/I-Simpa_Cherry/releases/latest)**: under
*Assets*, the file ending in `-win64-setup.exe` (about 10 MB).

To check that the download is genuine, compare its SHA-256 with the `.sha256` file beside it. In PowerShell:

```powershell
Get-FileHash .\I-Simpa-Night-Mode-1.1.0-a5c3111-win64-setup.exe
```

Download only from this page. A copy from anywhere else may have been changed.

## Install

1. Run the setup file. It installs for your Windows user only and needs no administrator rights.
2. Windows SmartScreen may say *"Windows protected your PC"*, because the installer is not yet code-signed.
   Click **More info**, then **Run anyway**.
3. Open **I-Simpa Night Mode** from the Start menu. `.simpa` project files open in it with a double-click.

The installer brings everything the app needs: the solvers and the Microsoft C++ runtime they use. If your PC
lacks Microsoft's WebView2 runtime, it downloads and installs it (Windows 11 always has it).

To uninstall: Windows Settings, Apps, I-Simpa Night Mode. Your own projects and results are never removed.

## Requirements

- Windows 10 or 11, 64-bit.
- SPPS on the GPU needs an NVIDIA graphics card with a current driver. Without one, SPPS and TCR run on the
  processor as usual.
- Memory and disk depend on the room and the run; the app forecasts both before a run starts.

## First steps

On the start screen, open **Tutorial 1** (a small teaching room) or one of the example rooms, then go to
**Simulate** and press **Run**. The user manual is under **Help, User manual**.

## What it does

- **Start:** example rooms (Elmia, an industrial hall, BRAS CR1-CR4), I-Simpa's tutorials 1-3, a box room of any
  size, PLY/OBJ/STL and I-Simpa `.proj` import, recent projects, crash recovery.
- **Geometry:** a model check before any run (watertight, self-intersections, flipped normals, open edges,
  units), repair to a new file, surface groups, sound-level planes at any angle, fitting zones.
- **Materials:** absorption, scattering, transmission and the reflection law per band, with I-Simpa's reference
  library, the BRAS benchmark materials in a library window, and CATT material-list import.
- **Sources and receivers:** placed on any face; spectra with dB(A) entry; directivity; receiver groups.
- **Simulate:** SPPS, TCR or SPPS on the GPU; memory and run-time forecasts; a checklist that stops a run that
  cannot succeed; background runs with a live console.
- **Measured rooms:** a room's own measured impulse responses laid over the simulated decays, with the error per
  parameter.
- **Results:** SPL, G, EDT, T15, T20, T30, C50, C80, D50, Ts, STI and dB(A) to ISO 3382-1 and IEC 60268-16;
  sound maps and parameter maps per face; difference maps; particle playback; listening through the room;
  CSV, JSON, PNG and WAV export.
- **Every value shown passes a check.** A value that does not is shown as REFUSED, with its reason.

## Not in this version

Stereo or binaural listening; pausing a run; languages other than English; an update check. The manual lists
the rest.

## Feedback

Bug reports and requests: [Issues](https://github.com/Burhanuddin98/I-Simpa_Cherry/issues). Please include the
version from **Help, About** and, for a failed run, the run's console text.

## Licence

The I-Simpa Night Mode application is free to download and use. Its source code is not published; all rights
reserved. It ships separate programs under their own licences, I-Simpa's solvers under the GPL-3.0 among them.
Their notices, and the source for each, are in [`licenses/`](licenses/).

I-Simpa Night Mode is not made or endorsed by Université Gustave Eiffel.
