# FIX-PANEL-

Runtime assets used by **CRYSTALVN LOADER 2**. The loader downloads these on demand, verifies every file with SHA-256 and installs it locally — nothing here is bundled inside the loader executable.

| Path | Contents |
| --- | --- |
| `Redist/vc-redist.zip` | Microsoft Visual C++ 2005–2022 runtimes (x86 + x64) |
| `Redist/directx.zip` | DirectX runtime setup |
| `Emulator/BlueStacksInstaller_5.22.125.1001_native.exe` | BlueStacks 5 bootstrapper |
| `FF/V7A-FFTH.xapk.part01…04` | Free Fire XAPK split into sub-100 MiB parts |
| `FF/manifest.json` | Part sizes + SHA-256 and the hash of the reassembled XAPK |
| `downloads.json` | Sizes + SHA-256 for the runtime packages |

The four `FF` parts are one archive: the loader downloads them in order, joins them into `V7A-FFTH.xapk`, checks the full SHA-256 and only then installs it into the running BlueStacks instance. Do not rename or replace a single part.
