# Nocta One firmware

Firmware for Nocta One, an offline hardware password manager.

**Nothing is published here yet.** The firmware is not written. This repository
exists to settle the licence and the disclosure policy before any code lands.

## The hardware it runs on

Nocta One rev v3. The design is public and can be checked:
[NoctaLabs-Sh/Nocta-One-Hardware](https://github.com/NoctaLabs-Sh/Nocta-One-Hardware)

| Function | Part |
| --- | --- |
| MCU and radio | STM32WB5MMGH6TR (Cortex-M4 + Cortex-M0+, BLE 5) |
| Storage | W25Q128JVS, 128 Mbit SPI NOR (16 MB) |
| Power | nPM1300 PMIC, TPS62840 buck |
| Display | 2.7 inch e-ink, FPC |
| Secure element | TROPIC01 at IC3, land pattern on the board, not fitted on v3 |

Two things worth stating plainly:

The BLE stack runs on the M0+ core and ships as an ST binary. It is not mine and
it is not covered by this licence.

TROPIC01 is designed in but marked DNP on v3. You can verify both facts in the
schematic in the hardware repository. Until it is fitted, no claim on this
repository depends on it.

## Licence

GPL-3.0-or-later. Full text in [LICENSE](LICENSE).

The hardware is CERN-OHL-S v2. Both licences are reciprocal, so work derived
from either side stays open.

Section 6 of GPL-3.0 means the bootloader stays user-flashable. That is
deliberate. A vault you cannot build and flash yourself is one you have to take
on trust, and the point of this project is that you should not have to.

Intended behaviour, not yet implemented: flashing a build I did not sign wipes
stored credentials and leaves the device visibly marked, so an unofficial build
is possible and never silent.

## Security

Vulnerability reporting: [SECURITY.md](SECURITY.md).

## Status

Nothing to build. The toolchain is not decided; bare C with STM32CubeMX is the
likely direction. Progress is written up at
[noctalabs.sh/blog](https://www.noctalabs.sh/blog).

Nocta Labs is a trading name of Robert Callens, Leuven, Belgium.
