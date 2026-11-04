# Release notes

Copy the newest `releases/SharpMZ2500_<date>.rbf` to `/media/fat/_Computer/` on the MiSTer SD card (setup, ROMs and
disks: [README](README.md#getting-started)). Newest first.

## 20261103 (first release)

- MZ-2500 and MZ-2520 models; 400- and 200-line modes (OSD **Lines**, applied at reset); MZ-2500, MZ-2000 and MZ-80B
  boot modes.
- Floppy: D88 disks in drives 1-2 with write-back (Ys III saves), the MB8876's rotation timing as in the reference
  emulator (the copy protection of Laydock, Macadam, Märchen Veil and Mugen II depends on it); sectors are fetched from
  the SD card while the disk turns, so loads take as long as on the real machine.
- Data recorder: MZT tapes in MZ-2500, MZ-2000 and MZ-80B modes at real speed. MAME `mz2000_snap` RAM images start
  at once (OSD **Load RAM image**).
- Video: text with kanji, PCG and 64 colours; 16-, 256- and 4096-colour graphics with scrolling, split screen and
  priority.
- YM2203 sound and beeper; RTC from the MiSTer clock; keyboard (Japanese positional or US symbols), mouse, joystick.
- Optional dictionary, phone and MZ-1R13 kanji ROMs in a longer `boot.rom` (`tools/make_bootrom.sh`).
- Framework: Template_MiSTer e901a9f (2026-11-03).

Test builds before this one were published in the development repository,
[alanswx/SharpMZ2500_MiSTer](https://github.com/alanswx/SharpMZ2500_MiSTer).
