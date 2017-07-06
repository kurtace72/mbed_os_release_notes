# mbed OS 5.5 Releases

## mbed OS 5.5.2 release
We are pleased to announce the [mbed OS 5.5.2 release](https://github.com/ARMmbed/mbed-os/releases/tag/mbed-os-5.5.2) is now available.

This release includes new target support for DISCO_F413ZH and VBLUno51 and an update for the STM32F7 cube from v1.6.0 to v1.7.0. It also includes SHA256 and SHA1 hardware acceleration support for NUCLEO_F439ZI, USB Device for DISCO_L072CZ_LRWAN1, plus fixes to mbed OS and tools to improve stability and functionality. 

### Known issues

The following list of known issues apply to this release:

Due to a dependency of stm32f413 on a later patch version of IAR, which is currently not available in our CI systems, IAR export support for this platform is not available for this release. 

[4697](https://github.com/ARMmbed/mbed-os/pull/4697): IAR: Remove stm32f413 from definitions

Here is a full list of all changes and fixes in this release.

### Ports for upcoming targets

[4410](https://github.com/ARMmbed/mbed-os/pull/4410): DISCO_F413ZH: Add new platform

[4629](https://github.com/ARMmbed/mbed-os/pull/4629): Add support for VBLUno51 board

### Fixes and changes

[4578](https://github.com/ARMmbed/mbed-os/pull/4578): Turn off "browse information" in Uvision template

[4616](https://github.com/ARMmbed/mbed-os/pull/4616): Fix unresolved include of `mbed_config.h` in Eclipse

[4375](https://github.com/ARMmbed/mbed-os/pull/4375): Stm32 SPI: Use LL API to improve performances

[4401](https://github.com/ARMmbed/mbed-os/pull/4401): STM32: Add USB used pins in `PinNames.h` files

[4520](https://github.com/ARMmbed/mbed-os/pull/4520): Update link in `CONTRIBUTING.md`

[4103](https://github.com/ARMmbed/mbed-os/pull/4103): Add `extra_targets.json` support to build tools

[4390](https://github.com/ARMmbed/mbed-os/pull/4390): Nucleo-F070RB doesn't work when use internal clock

[4405](https://github.com/ARMmbed/mbed-os/pull/4405): DISCO_L072CZ_LRWAN1: PC_13 definition missing in `PinNames.h` fix

[4426](https://github.com/ARMmbed/mbed-os/pull/4426): Improve directory scanning performance

[4538](https://github.com/ARMmbed/mbed-os/pull/4538): Avoid lock collision between SerialBase & UARTSerial

[4552](https://github.com/ARMmbed/mbed-os/pull/4552): NUCLEO_F767ZI: Add missing IAR definitions

[4557](https://github.com/ARMmbed/mbed-os/pull/4557): Enable I2C and AnalogIn drivers for CM3DS_MPS2 target

[4572](https://github.com/ARMmbed/mbed-os/pull/4572): DISCO_L072CZ_LRWAN1: Add support of USB device

[4157](https://github.com/ARMmbed/mbed-os/pull/4157): NUCLEO_F439ZI/mbedtls: Add SHA1 `hw_acceleration`

[4422](https://github.com/ARMmbed/mbed-os/pull/4422): STM32F4 set HSE timeout value to 100 ms

[4594](https://github.com/ARMmbed/mbed-os/pull/4594): Introduce `mbed::NonCopyable` traits

[4598](https://github.com/ARMmbed/mbed-os/pull/4598): Fix style issues in IAR exporter

[4604](https://github.com/ARMmbed/mbed-os/pull/4604): cmain IAR: Add mbed main

[4607](https://github.com/ARMmbed/mbed-os/pull/4607): Fix missing init in MBRBlockDevice

[4603](https://github.com/ARMmbed/mbed-os/pull/4603): STM32: `mbed_overrides.c` is common for all families

[4638](https://github.com/ARMmbed/mbed-os/pull/4638): DISCO_L475VG_IOT01A: Fix startup files for cmsis5

[4610](https://github.com/ARMmbed/mbed-os/pull/4610): STM32: `targets.json` file simplification

[4647](https://github.com/ARMmbed/mbed-os/pull/4647): Remove hardcode UART pins definitions for nRF52832 SoC

[4646](https://github.com/ARMmbed/mbed-os/pull/4646): RTX: Fixed RTXv5 mutex owner list handling

[4625](https://github.com/ARMmbed/mbed-os/pull/4625): Update STM32F7 cube from v1.6.0 to v1.7.0

[4421](https://github.com/ARMmbed/mbed-os/pull/4421): STM32: Clock source selection in .json config file

[4559](https://github.com/ARMmbed/mbed-os/pull/4559): fatfs: Remove unused `fat_filesystem_set_errno` function

[4571](https://github.com/ARMmbed/mbed-os/pull/4571): Events: Adopt osEventFlags from RTX 5

[4577](https://github.com/ARMmbed/mbed-os/pull/4577): XDOT_L151CC: Enable HSI after waking from stop mode so ADC functions

[4601](https://github.com/ARMmbed/mbed-os/pull/4601): RTOS: Fix MemoryPool and Queue destructor

[4632](https://github.com/ARMmbed/mbed-os/pull/4632): STM32: Fix us ticker set event timestamp double ISR possibility

[4641](https://github.com/ARMmbed/mbed-os/pull/4641): Increase L0 ADC sample time

[4656](https://github.com/ARMmbed/mbed-os/pull/4656): Correct comments in Flash API for STM32 L0 targets

[4671](https://github.com/ARMmbed/mbed-os/pull/4671): Retarget: Fix `microlib` for mbed OS 2

[4529](https://github.com/ARMmbed/mbed-os/pull/4529): Manage multiple instances of AnalogOut

[4565](https://github.com/ARMmbed/mbed-os/pull/4565): Add `FlashIAP` support for REALTEK_RTL8195AM

[4159](https://github.com/ARMmbed/mbed-os/pull/4159): NUCLEO_F439ZI/mbedtls: Add SHA256 hw_acceleration

### Using the release

You can fetch the mbed OS 5.5.2 release from the [mbed-os GitHub](https://github.com/ARMmbed/mbed-os) repository, using the tag "mbed-os-5.5.2".

Please feel free to ask any questions or provide feedback on this release [on the forum](https://forums.mbed.com/), or to contact us at [support@mbed.org](mailto:support@mbed.org).


## mbed OS 5.5.1 release

We are pleased to announce the [mbed OS 5.5.1 release](https://github.com/ARMmbed/mbed-os/releases/tag/mbed-os-5.5.1) is now available. This release includes a fix for a critical issue found in mbed-os-5.5.0:  [4584](https://github.com/ARMmbed/mbed-os/issues/4584) Introduction of RTX/CMSIS 5 has broken semaphore signaling. We have fixed the issue by reverting behavior to how it was in RTX/CMSIS 4.

The release also includes support for `CM3DS_MPS2` and `DISCO_L475VG_IOT01A` targets, an update to the u-blox ODIN-W2 driver binaries and bug fixes that improve the stability of the tools and codebase.

### Known issues

The following list of known issues applies to this release:

[4605](https://github.com/ARMmbed/mbed-os/issues/4605): Timing tests are unstable on the `ARM_BEETLE_SOC`

Here is a full list of all changes and fixes in this release.

### Ports for upcoming targets

[4414](https://github.com/ARMmbed/mbed-os/pull/4414): Enable `CM3DS_MPS2` target

[4242](https://github.com/ARMmbed/mbed-os/pull/4242): `DISCO_L475VG_IOT01A`: Add new target

### Fixes and changes

[4545](https://github.com/ARMmbed/mbed-os/pull/4545): Filter support with a white list of post-bin hooks in uvision

[4544](https://github.com/ARMmbed/mbed-os/pull/4544): Export static files from mbed export

[4542](https://github.com/ARMmbed/mbed-os/pull/4542): Issue #4528 K82F: Initialize the UART clock inside the board file

[4530](https://github.com/ARMmbed/mbed-os/pull/4530): Enable verbose builds when running example build tests

[4516](https://github.com/ARMmbed/mbed-os/pull/4516): Check for correct library naming in Travis CI

[4510](https://github.com/ARMmbed/mbed-os/pull/4510): u-blox: Rearrange ODIN target

[4502](https://github.com/ARMmbed/mbed-os/pull/4502): STM32: serial: Clear Overrun flag if it is set when checking if readable

[4562](https://github.com/ARMmbed/mbed-os/pull/4562): fatfs: Fix initialization of block device in mount/unmount functions

[4504](https://github.com/ARMmbed/mbed-os/pull/4504): Add reporting of reserved heap in Greentea

[4554](https://github.com/ARMmbed/mbed-os/pull/4554): Fix `NUCLEO_L476RG` linker scripts

[4563](https://github.com/ARMmbed/mbed-os/pull/4563): Increase background stack size to fix overflow

[4364](https://github.com/ARMmbed/mbed-os/pull/4364): Add C API for Greentea client

[4540](https://github.com/ARMmbed/mbed-os/pull/4540): Support app config option for export

[4541](https://github.com/ARMmbed/mbed-os/pull/4541): Fix a bug in `print_large_string`

[4579](https://github.com/ARMmbed/mbed-os/pull/4579): Fix semaphore in RTOS

[4444](https://github.com/ARMmbed/mbed-os/pull/4444): Resolve lwIP init twice issue

[4523](https://github.com/ARMmbed/mbed-os/pull/4523): Check Ethernet before including `lwipopts_conf.h`

[4337](https://github.com/ARMmbed/mbed-os/pull/4337): Platform support for new CellularInterface in `UBLOX_C027` and `UBLOX_C030_U201`

[4567](https://github.com/ARMmbed/mbed-os/pull/4567): Update u-blox ODIN-W2 driver binaries to 2.1 rc1

### Using the release

You can fetch the mbed OS 5.5.1 release from the [`mbed-os` GitHub](https://github.com/ARMmbed/mbed-os) repository by using the tag "mbed-os-5.5.1".

Please feel free to ask any questions or provide feedback on this release [on the forum](https://forums.mbed.com/), or to contact us at [support@mbed.org](mailto:support@mbed.org).

This is the release note for ARM mbed OS 5.5. It summarizes the major enhancements in this version. You can find the mbed OS 5.5.0 release on [GitHub](https://github.com/ARMmbed/mbed-os/tree/mbed-os-5.5).

## mbed OS 5.5.0 release

### About this release

The mbed OS 5.5 release upgrades to the latest version of CMSIS, paving the way for support of the latest ARM compilers, ARMv8-M Architecture based MCUs and lower power RTOS modes. It also introduces cellular connectivity, embedded storage and hardware security enhancements to further simplify development of connected, managed IoT devices. In addition, this release contains many minor fixes and enhancements and brings target platform support up to 85 targets.

### Core 

mbed OS 5.5 upgrades to the latest CMSIS version, CMSIS5, including the enhanced CMSIS-RTOS2 kernel. This is a significant step in our roadmap to enable support for the latest generation of compilers (ARM GCC Embedded 6, ARM Compiler 6 and IAR Embedded Workbench 8), support for v8-M architecture cores and introduction of low power tick-less RTOS and deep sleep modes. 

The release includes many general enhancements and fixes, and upstreams those that have been maintained within the mbed OS codebase itself. The upgrade should be generally transparent to developers using the mbed OS RTOS APIs, but please report in the [forums](https://developer.mbed.org/forum/bugs-suggestions/) or contact us at [support@mbed.com](mailto:support@mbed.com) if you have any issues in this area.

The file system infrastructure now supports SPI NOR Flash devices, a low-cost, external storage solution. Developers commonly use it in IoT devices to store firmware update images, device credentials and configuration information and to cache data for later syncing to the cloud. You can use the SPI NOR Flash storage with all mbed Enabled platforms, and it is the recommended storage medium for devices requiring firmware update capabilities.

The release also includes a standard in-application flash programming API, [FlashIAP](https://github.com/ARMmbed/mbed-os/blob/master/drivers/FlashIAP.h), and first partner implementations. This component supports the upcoming mbed Cloud Update service capability, available to licensees, that manages device firmware update campaigns across fleets of devices.

### Connectivity 

mbed OS 5.5 introduces improved support for cellular connectivity modules, including standard integration through a built-in PPP network interface.

A Linux-based Thread Access Point reference that uses the Thread border router [is now available](https://github.com/ARMmbed/mbed-access-point).

Our new native mbed OS BLE stack has reached our Early Partner Release milestone. This allows use of BLE transceivers with any mbed Enabled MCU and provides stack consistency across different BLE hardware. Based on this, we will be working with the first mbed Partners to enable support for their BLE transceivers and SoCs using this stack, planning to provide first access to developers in the 5.6 release. Partners interested in supporting BLE transceivers or SoCs with this stack should contact their Partner Enablement Team representatives.

### Security 

mbed OS cryptography incorporates mbed TLS 2.5 and the completion of internal APIs for enabling hardware entropy and symmetric and asymmetric cryptographic acceleration. Many partners are implementing and landing support for acceleration on their target platforms and are seeing significant performance increases. Partner acceleration will land in patch releases as we work with partners to complete security audits and mainline these contributions.

uVisor updates address several performance and usability issues reported since the last release. Secure boxes on devices with an ARMv7-M MPU now use less memory and provide more user-friendly configuration options.

uVisor now also supports the new ARMv8-M architecture, including the TrustZone for ARMv8-M security extensions. Support for this architecture is still experimental and is currently only accessible through [a feature branch in mbed OS](https://github.com/ARMmbed/mbed-os/tree/feature-uvisor-armv8m).

### Targets

Thanks to our partners’ hard work, mbed OS 5.5 now supports 85 target platforms.

We'll continue to add targets in our biweekly patch releases as partners work with us on support.

### Fixes and changes

Please see the [mbed OS GitHub repository](https://github.com/ARMmbed/mbed-os/tree/mbed-os-5.5) for a full list of changes introduced in this release. You can find a list of known issues [here](https://docs.mbed.com/docs/mbed-os-release-notes/en/latest/5_5/known_issues/).

### Using the release 

You can fetch the latest version of the mbed OS 5.5 release from the `mbed-os` GitHub repository using the branch “[mbed-os-5.5](https://github.com/ARMmbed/mbed-os/tree/mbed-os-5.5)”.

Please feel free to ask any questions or provide feedback about this release on the [forum](https://developer.mbed.org/forum/), or to contact us at support@mbed.org.
