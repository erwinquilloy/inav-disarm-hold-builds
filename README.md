# INAV + MSP DisplayPort disarm hold (unofficial builds)

Build recipe for INAV 9.0.0, 9.0.1, 9.1.0 and 10.0.0-rc2 with one addition, `osd_msp_disarm_hold`.
Not made or supported by the INAV team.

The hold keeps telling the MSP DisplayPort air unit "armed" for 0-7 seconds after a disarm, so
goggles that record only while armed also record the stats screen. The flight controller disarms
at once and every other MSP user sees the real state. Default 0 = off.

- `patches/`: the complete change, per version
- `prepare.sh`: applies it to the official source
- `.github/workflows/build.yml`: builds every release target and creates draft releases

The 9.x builds are released on [erwinquilloy/inav](https://github.com/erwinquilloy/inav/releases); 10.0 and later here.

Reproduce: check out the INAV tag, run `prepare.sh <checkout> <version>`, then build INAV as usual.

License: GPL-3.0, like INAV (see `COPYING`).
