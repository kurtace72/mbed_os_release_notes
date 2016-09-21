# mbed OS 5.1 releases

## mbed OS 5.1.4 release

We are pleased to announce the mbed OS 5.1.4 release is now available.

This release includes many minor enhancements and fixes, adds some target HAL ports in preparation for upcoming new targets (ST Disco F769NI, Delta DFBM NQ620, MTM mtconnect 04S, ST Nucleo f303ze), and some early additions for runtime heap memory tracking features we're working on that we'll share more on soon.

Here is a full list of all changes and fixes in this release.

### Ports for Upcoming Targets

2504: [Disco_F769NI] Added new target

2654: DELTA_DFBM_NQ620 platform porting

2615: [MTM_MTCONNECT04S] Added support for MTM_MTCONNECT04S

2548: Nucleof303ze

### Fixes and Changes

2678: Fixing NCS36510 compile on Linux

2657: [MAX326xx] Removed echoing of characters and carriage return

2651: Use lp_timer to count time in the deepsleep tests

2645: NUCLEO_F446ZE - Enable mbed5 release version

2643: Fix thread self termination

2634: Updated USBHost for library changes

2633: Updated USBDevice to use Callback

2630: Test names not dependent on disk location of root

2624: CFSTORE Bugfix for realloc() moving KV area and cfstore_file_t data structures not being updated correctly

2623: DISCO_L476VG - Add Serial Flow Control pins + add SERIAL_FC macro

2617: STM32F2xx - Enable Serial Flow Control

2613: Correctly providing directories to build_apis

2607: Fix uvisor memory tracing

2604: Tools - Fix fill section size variation

2601: Adding ON Semiconductor copyright notice to source and header files.

2597: [HAL] Fixed "intrinsic is deprecated" warnings

2596: [HAL] Improve memory tracer

2594: Fix TCPServer constructor

2593: Add app config command line switch for test and make

2589: [NUC472] Fix heap configuration error with armcc

2588: Timing tests drift refactor

2587: add PTEx pins as option for SPI on Hexiwear - for SD Card Interface

2584: Set size of callback irq array to IrqCnt

2583: github issue and PR templates

2582: [GCC_CR] fix runtime hang for baremetal build

2580: lwip - Add check for previously-bound socket

2579: lwip - Fix handling of max sockets in socket_accept

2578: Fix double free in NanostackInterface

2576: Add smoke test that builds example programs with mbed-cli

2575: tools-config! - Allow an empty or mal-formed config to be passed to the config system

2562: Fix GCC lazy init race condition and add test

2559: [utest]: Allow the linker to remove any part of utest if not used

2545: Added define guards for SEQUENTIAL_FLASH_JOURNAL_MAX_LOGGED_BLOBS so

2538: STM32F4xx - Add support of ADC internal channels (Temp, VRef, VBat)

2521: [NUCLEO_F207ZG] Add MBED5 capability

2514: Updated FlexCan and SAI SDK drivers

2487: Runtime dynamic memory tracing

2442: Malloc heap info

2419: [STM32F1] Add asynchronous serial

2393: [tools] Prevent trace-backs from incomplete args

2245: Refactor export subsystem

2130: stm32 : reduce number of device.h files

### Using the release

You can fetch the mbed OS 5.1.4 release from the [mbed-os GitHub](https://github.com/ARMmbed/mbed-os) repository, using the tag "mbed-os-5.1.4".

Please feel free to ask any questions or provide feedback on this release [on the forum](https://forums.mbed.com/), or to contact us at [support@mbed.org](mailto:support@mbed.org).

## mbed OS 5.1 - 5th August 2016 

This is the release note for the mbed OS 5.1.0 release. It summarises the major changes in this version of mbed OS, as well as the requirements for partners looking to support this release on development platforms. 

## About this release 

This release marks significant changes and enhancements that have accelerated features of our roadmap, opened up the applicability of mbed OS to many more IoT use cases, and unlocked compatibility with our mbed OS 2 "Classic" ecosystem. 

## Version summary 

The headline changes in this release are: 

* RTOS - mbed OS now incorporates an RTOS. This much-requested feature provides native thread support to the OS and applications, simplifying development and integration of complex and robust application components like networking stacks. It also enables both blocking and non-blocking design patterns. The RTOS requires very limited system overhead. 
* Tooling - we have simplified the tooling and introduced native support for building and testing across the ARM Compiler 5, ARM GCC Embedded and IAR compiler toolchains. A command line interface script (mbed CLI) now drives the established mbed OS 2 build system to build the OS and associated developer applications and components. Dependencies are explicitly pinned to provide full reproducibility of builds. The target and toolchain can be selected independently of each other, and we run CI on mbed OS across all these compiler toolchains on every commit. yotta is not used in this release. 
* Compatibility - the introduction of the RTOS and changes to tooling have allowed the possibility of compatibility with the mbed OS 2 ("Classic") ecosystem. We have taken this opportunity to re-base and merge the two development lines so that we now have just one platform and one set of tools. Existing partners can take advantage of investments made in mbed over the years, and both new and existing partners need to invest in only one project. Developers can benefit from all legacy components and libraries, alongside the existing and new features of mbed OS. 

These architectural changes enable merging the mbed OS 2 and mbed OS 3 codebases, websites and ecosystems, and are marked with a major revision update - mbed OS 5 (2+3=5!). 

Our mbed OS 5.0.1 was an internal version available only to partners, and mbed OS 5.1.0 is the first generally available. 

Based on these changes and the hard work of our partners, mbed OS target support is also accelerated. This release supports multiple target platforms from multiple partners, with more ports regularly made available on a newly introduced minor release tick every two weeks. 

The following sections provide more details of these and other changes in this release. 

## Core 

### RTOS 

mbed OS now incorporates an RTOS. 

The RTOS core is based on the widely used open-source CMSIS-RTOS RTX, providing an established kernel that can support threads and other RTOS services on very tiny devices. The RTOS primitives are always available, so that drivers and applications can rely on features such as threads, semaphores and mutexes. The RTOS is initialised ahead of entering the main() thread, enabling components to rely on RTOS facilities even if the core application is single threaded. 
 
The implementation is based on CMSIS-RTOS RTX 4.79.0, and we will be tracking and contributing to the development of CMSIS-RTOS releases, allowing us to pick up support for new versions and architectural features such as TrustZone for Cortex-M. 

The MINAR eventing-only scheduler is not included in this release. An alpha version of a more flexible [event scheduler library](https://github.com/ARMmbed/mbed-events) is available, supporting the same design patterns within RTOS threads and components. This library will be merged and managed as part of the core OS codebase once it reaches release maturity.
 
### Drivers and support libraries 

There is now driver support for a wide range of standard MCU peripherals across the extended target platforms: 

* DigitalIn, DigitalOut, DigitalInOut 
* InterruptIn 
* PortIn, PortOut, PortInOut 
* BusIn, BusOut, BusInOut 
* AnalogIn, AnalogOut 
* PwmOut 
* I2C, I2CSlave 
* SPI, SPISlave 
* Serial 
 
Improved API documentation is now available [here](https://docs.mbed.com/docs/mbed-os-api-reference/).

These drivers have been internally upgraded to integrate thread safety logic, while maintaining compatibility with the mbed OS 2 APIs. This has been done within the generic components of the drivers to avoid changes to the different HAL implementations. 

A new ``Callback`` class supersedes ``FunctionPointer`` (still supported) to provide a more flexible and neater syntax for capturing and calling static function and class member callbacks. It now uses the same class regardless of the number of arguments on the callback. 

### C libraries 

The C libraries provided with each of the supported toolchains have been integrated into mbed OS, including implementation of thread safety support. 

## Security 

### uVisor 

uVisor has been upgraded to support the RTOS. 

We have made the modifications CMSIS required to allow uVisor to hook interrupts. These will be upstreamed to future CMSIS releases. 

uVisor now includes a disabled mode for ARMv7-M and ARMv6-M architectures that maintains code compatibility even when uVisor is not present or active, enabling a smooth software upgrade path as platforms introduce support for uVisor. 

### Crypto 

The crypto libraries now support:

* An insecure NULL entropy mode to simplify support during development.
* A HAL API for providing strong entropy sources based on a hardware TRNG.
* A reasonable strength entropy source based on non-volatile storage. 

###mbed TLS 

We have integrated version 2.3.0 of mbed TLS, providing TLS and DTLS support for services. 

See [the mbed TLS 2.3.0 release note](https://tls.mbed.org/tech-updates/releases/mbedtls-2.3.0-2.1.5-and-1.3.17-release).

Please note, applications using mbed TLS on boards that have not yet implemented hardware entropy support must use the NULL ENTROPY configuration to build. However, please be aware that no security will be offered by mbed TLS in those cases. 

## Connectivity 

The sockets API has been revised to support: 

* Multiple stacks 
* Multiple interfaces 
* Synchronous and asynchronous APIs 
 
We have successfully applied this to Ethernet, 6LoWPAN Mesh and WiFi interfaces. 

We've introduced an 802.15.4 MAC HAL to enable simplified porting of the 6LoWPAN and Thread stacks to different 802.15.4 radios. This release includes ports for multiple transceivers. 

We have released a 6LoWPAN Border Router reference application and an associated Linux-based Access Point example that demonstrates 6LoWPAN nodes connecting via an Access Points to the mbed Device Connector service. A development Thread Border Router is also available to mbed Partners. 

We've extended our Bluetooth Low Energy (BLE) API to support user-defined scheduling policies. This maintains compatibility with mbed OS 2 BLE applications, while allowing developers to take advantage of the RTOS to design more efficient solutions. The Bluetooth API is now supported across multiple vendor silicon, covering both SoC and MCU plus Transceiver chipset arrangements. 

## Services 

mbed OS integrates the latest mbed Cloud Client, providing connectivity and management services from mbed Device Connector. 

See [the mbed Device Connector site](https://connector.mbed.com/).

## Tools and workflow 

We've reworked the tools and workflows to address feedback from previous releases on the use of yotta and the desire for backward compatibility with mbed OS 2 (“Classic”). In this release we build the OS, components and applications using modified versions of the mbed OS 2 build scripts. 

### mbed CLI

You can use a new top level command line interface (mbed CLI) to drive the build, package management and test scripts. It is also a natural integration point for IDEs. 

See [the mbed CLI repository](https://github.com/ARMmbed/mbed-cli). 

### Dependencies 

This release does not use yotta; applications depend instead on a single mbed OS repository where all dependencies are pinned, making applications reproducible and simplifying development and management. 

See [the mbed OS repository](https://github.com/ARMmbed/mbed-os). 

### Code compatibility and toolchain support

Code is compatible with c99/C++03, and doesn't use any C++11 or C++14 features. 

We now support building and testing across multiple toolchains (ARM Compiler 5, GCC ARM Embedded, IAR). Supporting these three toolchains is a requirement for partner ports. 

The build tools now emit static RAM and FLASH sizes and a top level breakdown on every build. 

### Exporting to Third Party IDEs

We support generation of project files to enable opening mbed OS projects in Keil MDK, IAR Workbench and other environments. This is useful for development and launching debug sessions, and can be achieved from mbed CLI or the mbed Online Compiler. 

## mbed Enabled 

We've formalised the mbed Enabled program, providing versioned compliance criteria and technical requirements for boards, on-board interfaces and end products. 

The following resources are available: 

* The mbed Enabled [requirements documents](https://www.mbed.com/mbed-enabled-requirements/), available on the site.
* The mbed Enabled [application form](https://docs.google.com/forms/d/e/1FAIpQLSf87Qw7FsDelw9L4q_sB8QW3Hy5aff5WRwZUhPlNzf2Xm6iVw/viewform).

## Targets 

Thanks to our partners' hard work, including an onsite workshop, the mbed OS 5.1 release already supports the following targets: 

- [Seeed Arch Pro (ARCH_PRO)](https://developer.mbed.org/platforms/Seeeduino-Arch-Pro/)
- [Silicon Labs Pearl Gecko (EFM32PG_STK3401)](https://developer.mbed.org/platforms/EFM32-Pearl-Gecko/)
- [HEXIWEAR](https://developer.mbed.org/platforms/Hexiwear/)
- [NXP K22F (K22F)](https://developer.mbed.org/platforms/FRDM-K22F/)
- [NXP K64F (K64F)](https://developer.mbed.org/platforms/FRDM-K64F/)
- [NXP KL25Z (KL25Z)](https://developer.mbed.org/platforms/KL25Z/)
- [NXP KL46Z (KL46Z)](https://developer.mbed.org/platforms/FRDM-KL46Z/)
- [NXP LPC1768 (LPC1768)](https://developer.mbed.org/platforms/mbed-LPC1768/)
- [Embedded Artists LPC4088 (LPC4088)](https://developer.mbed.org/platforms/EA-LPC4088/)
- [Embedded Artists LPC4088_DM (LPC4088)](https://developer.mbed.org/platforms/EA-LPC4088-Display-Module/)
- [Maxim - (MAX32600MBED)](https://developer.mbed.org/platforms/MAX32600mbed/)
- [Maxim – MAXWSNENV](https://developer.mbed.org/platforms/MAXWSNENV/)
- [MultiTech Dragonfly F411RE (MTS_DRAGONFLY_F411RE)](https://developer.mbed.org/platforms/MTS-Dragonfly/)
- [MultiTech mdot F411RE (MTS_MDOT_F411RE)](https://developer.mbed.org/platforms/MTS-mDot-F411/)
- [Nordic nRF51-DK (NRF51_DK)](https://developer.mbed.org/platforms/Nordic-nRF51-DK/)
- [Nordic nRF52-DK (NRF52_DK)](https://developer.mbed.org/platforms/Nordic-nRF52-DK/)
- [Nuvoton NUC472 (NUMAKER_PFM_NUC472)](https://developer.mbed.org/platforms/Nuvoton-NUC472/)
- [Renesas GR-PEACH (RZ_A1H)](https://developer.mbed.org/platforms/Renesas-GR-PEACH/)
- [ST B96B_F446VE (B96B-F446VE)](https://developer.mbed.org/platforms/ST-B96B-F446VE/)
- [ST Discovery F429ZI (DISCO_F429ZI)](https://developer.mbed.org/platforms/ST-Discovery-F429ZI/)
- [ST Discovery F469NI (DISCO_F469NI)](https://developer.mbed.org/platforms/ST-Discovery-F469NI/)
- [ST Discovery F746NG (DISCO_F746NG)](https://developer.mbed.org/platforms/ST-Discovery-F746NG/)
- [ST Discovery L476VG (DISCO_L476VG)](https://developer.mbed.org/platforms/ST-Discovery-L476VG/)
- [ST Nucleo F070RB (NUCLEO_F070RB)](https://developer.mbed.org/platforms/ST-Nucleo-F070RB/)
- [ST Nucleo F072RB (NUCLEO_F072RB)](https://developer.mbed.org/platforms/ST-Nucleo-F072RB/)
- [ST Nucleo F091RC (NUCLEO_F091RC)](https://developer.mbed.org/platforms/ST-Nucleo-F091RC/)
- [ST Nucleo F103RB (NUCLEO_F103RB)](https://developer.mbed.org/platforms/ST-Nucleo-F103RB/)
- [ST Nucleo F303RE (NUCLEO_F303RE)](https://developer.mbed.org/platforms/ST-Nucleo-F303RE/)
- [ST Nucleo F401RE (NUCLEO_F401RE)](https://developer.mbed.org/platforms/ST-Nucleo-F401RE/)
- [ST Nucleo F410RB (NUCLEO_F410RB)](https://developer.mbed.org/platforms/ST-Nucleo-F410RB/)
- [ST Nucleo F411RE (NUCLEO_F411RE)](https://developer.mbed.org/platforms/ST-Nucleo-F411RE/)
- [ST Nucleo F429ZI (NUCLEO_F429ZI)](https://developer.mbed.org/platforms/ST-Nucleo-F429ZI/)
- [ST Nucleo F446RE (NUCLEO_F446RE)](https://developer.mbed.org/platforms/ST-Nucleo-F446RE/)
- [ST Nucleo F746ZG (NUCLEO_F746ZG)](https://developer.mbed.org/platforms/ST-Nucleo-F746ZG/)
- [ST Nucleo F767ZI (NUCLEO_F767ZI)](https://developer.mbed.org/platforms/ST-Nucleo-F767ZI/)
- [ST Nucleo L073RZ (NUCLEO_L073RZ)](https://developer.mbed.org/platforms/ST-Nucleo-L073RZ/)
- [ST Nucleo L152RE (NUCLEO_L152RE)](https://developer.mbed.org/platforms/ST-Nucleo-L152RE/)
- [ST Nucleo L432KC (NUCLEO_L432KC)](https://developer.mbed.org/platforms/ST-Nucleo-L432KC/)
- [ST Nucleo L476RG (NUCLEO_L476RG)](https://developer.mbed.org/platforms/ST-Nucleo-L476RG/)
- [U-blox C027 (UBLOX_C027)](https://developer.mbed.org/platforms/u-blox-C027/)

We will add new targets in our bi-weekly releases as partners introduce support. If you are a partner, please see details in the [Partner Portal](https://partners.mbed.com/en/partner-login/).  

##Getting Started 

To get started with this release, see the [Handbook](https://docs.mbed.com/docs/mbed-os-handbook/). 
