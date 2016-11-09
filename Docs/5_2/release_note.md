# mbed OS 5.2 releases

## mbed OS 5.2.2 release
We are pleased to announce the [mbed OS 5.2.2 release](https://github.com/ARMmbed/mbed-os/releases/tag/mbed-os-5.2.2) is now available.

This release includes support for new targets: Sara-N, MAX32625, FRDM-K82F and k22512. 

Other key highlights are:

- Implementation of the API for serial port flow control in NRF51 targets.

- Support for 6LoWPAN PAN ID filter added to mbed mesh API configuration.

- Updated u-blox ODIN-W2 drivers.

- A number of bug fixes and tool improvements.

### Known issues in this release

There is currently a DNS resolution failure in Thread mode. This causes a failure in the 
mbed-os-example-client and will be fixed in a subsequent release. This can be worked around by reverting 
to mbed-os-5.2.0.

Here is a full list of all changes and fixes in this release.

### Ports for Upcoming Targets

[3011](https://github.com/ARMmbed/mbed-os/pull/3011): Add u-blox Sara-N target.

[3099](https://github.com/ARMmbed/mbed-os/pull/3099): MAX32625

[3151](https://github.com/ARMmbed/mbed-os/pull/3151): Add support for FRDM-K82F

[3177](https://github.com/ARMmbed/mbed-os/pull/3177): New mcu k22512 fixing pr 3136

### Fixes and Changes

[2990](https://github.com/ARMmbed/mbed-os/pull/2990): [tools] Parallel building of tests

[3008](https://github.com/ARMmbed/mbed-os/pull/3008): NUCLEO_F072RB: Fix wrong timer channel number on pwm PB_5 pin

[3013](https://github.com/ARMmbed/mbed-os/pull/3013): STM32xx - Change how the ADC internal pins are checked before pinmap_

[3023](https://github.com/ARMmbed/mbed-os/pull/3023): digital_loop tests update for STM32

[3041](https://github.com/ARMmbed/mbed-os/pull/3041): [nRF5] - added implementation of API of serial port flow control configuration.

[3092](https://github.com/ARMmbed/mbed-os/pull/3092): [tools + tests] Adding parallelized build option for iar and uvision exporters

[3084](https://github.com/ARMmbed/mbed-os/pull/3084): [nrf5] fix in Digital I/O : a gpioe pin was uninitialized badly

[3009](https://github.com/ARMmbed/mbed-os/pull/3009): TRNG enabled. TRNG APIs implemented. REV A/B/C/D flags removed. Warnings removed

[3139](https://github.com/ARMmbed/mbed-os/pull/3139): Handle [NOT_SUPPORTED] exception in make.py

[3074](https://github.com/ARMmbed/mbed-os/pull/3074): Target stm init gcc alignement

[3140](https://github.com/ARMmbed/mbed-os/pull/3140): [tests] Replacing getchar with RawSerial getc in greentea-client

[3158](https://github.com/ARMmbed/mbed-os/pull/3158): Added support for 6lowpan PAN ID filter to mbed mesh api configuration

[2988](https://github.com/ARMmbed/mbed-os/pull/2988): Update of can_api.c fixing #2987

[3175](https://github.com/ARMmbed/mbed-os/pull/3175): Updating IAR definition for the NCS36510 for IAR EW v7.8

[3170](https://github.com/ARMmbed/mbed-os/pull/3170): [tests] Preventing test from printing before Greentea __sync

[3169](https://github.com/ARMmbed/mbed-os/pull/3169): [Update of #3014] Usb updates

[3143](https://github.com/ARMmbed/mbed-os/pull/3143): CFStore fix needed for the Cloud Client

[3135](https://github.com/ARMmbed/mbed-os/pull/3135): lwip - Fix memory leak in k64f cyclic-buffer overflow

[3048](https://github.com/ARMmbed/mbed-os/pull/3048): Make update.py test compile examples prior to updating mbed-os version.

[3162](https://github.com/ARMmbed/mbed-os/pull/3162): lwip/nsapi - Clean up warnings in network code

[3161](https://github.com/ARMmbed/mbed-os/pull/3161): nsapi - Add better heuristic for the default record of DNS queries

[3173](https://github.com/ARMmbed/mbed-os/pull/3173): [Exporters] Add a device_name to microbit entry in targets.json

[3072](https://github.com/ARMmbed/mbed-os/pull/3072): i2c_loop tests update for STM32

[2958](https://github.com/ARMmbed/mbed-os/pull/2958): Allowing mbed_app.json files to be discovered for tests.

[2969](https://github.com/ARMmbed/mbed-os/pull/2969): [nRF52] - switch irq priorities of driver handlers to the lowest level

[3078](https://github.com/ARMmbed/mbed-os/pull/3078): lwip: Allow several configuration macros to be set externally (bis)

[3165](https://github.com/ARMmbed/mbed-os/pull/3165): Add address type checks to NanostackInterface

[3166](https://github.com/ARMmbed/mbed-os/pull/3166): nsapi_dns: Provide 2 IPv6-hosted default servers

[3171](https://github.com/ARMmbed/mbed-os/pull/3171): [tools] Fixing project.py -S printing problem

[3172](https://github.com/ARMmbed/mbed-os/pull/3172): [Exporters] New export-build tests

[3184](https://github.com/ARMmbed/mbed-os/pull/3184): #3183 Compiler warning in trng_api.c with K64F 

[3185](https://github.com/ARMmbed/mbed-os/pull/3185): Update tests to fix build failures. Also make the code similar to oth

[3104](https://github.com/ARMmbed/mbed-os/pull/3104): [NuMaker] Support CAN and fix PWM CLK error

[3182](https://github.com/ARMmbed/mbed-os/pull/3182): Exporter documentation

[3186](https://github.com/ARMmbed/mbed-os/pull/3186): MultiTech mDot - add back SPI3 pins

[3187](https://github.com/ARMmbed/mbed-os/pull/3187): [Export-Make] Use internal class variable for resolving templates in makefiles

[3195](https://github.com/ARMmbed/mbed-os/pull/3195): [Exporters - Make-based] Quote the shell call in mkdir and rmdir

[3204](https://github.com/ARMmbed/mbed-os/pull/3204): [Export build-test] Directory traversal error

[3189](https://github.com/ARMmbed/mbed-os/pull/3189): [Exporters - Make-based] Force make exporter to search PATH for compilers

[3200](https://github.com/ARMmbed/mbed-os/pull/3200): Using Popen for uVision and unifying the structure of the build function

[3075](https://github.com/ARMmbed/mbed-os/pull/3075): nsapi - Add standardized return types for size and errors

[3221](https://github.com/ARMmbed/mbed-os/pull/3221): u-blox odin w2 drivers update


### Using the release

You can fetch the mbed OS 5.2.2 release from the [mbed-os GitHub](https://github.com/ARMmbed/mbed-os) repository,
using the tag "mbed-os-5.2.2".

Please feel free to ask any questions or provide feedback on this release [on the forum](https://forums.mbed.com/), or to contact us at [support@mbed.org](mailto:support@mbed.org).

## mbed OS 5.2.1 release

We are pleased to announce the [mbed OS 5.2.1 release](https://github.com/ARMmbed/mbed-os/releases/tag/mbed-os-5.2.1) is now available.

### Fixes and Changes

[2966](https://github.com/ARMmbed/mbed-os/pull/2966): Add kw24 support

[3068](https://github.com/ARMmbed/mbed-os/pull/3068): MultiTech mDot - clean up PeripheralPins.c and add new pin names

[3089](https://github.com/ARMmbed/mbed-os/pull/3089): Kinetis HAL: Remove clock initialization code from serial and ticker 

[2943](https://github.com/ARMmbed/mbed-os/pull/2943): [NRF5] NVIC_SetVector functionality

[2938](https://github.com/ARMmbed/mbed-os/pull/2938): InterruptIn changes in NCS36510 HAL.

[3112](https://github.com/ARMmbed/mbed-os/pull/3112): events - Remove unused variable warning in ndebug builds

[2953](https://github.com/ARMmbed/mbed-os/pull/2953): nsapi - Fix leftover bytes from suffix during ipv6 parsing

[3108](https://github.com/ARMmbed/mbed-os/pull/3108): Fix sleep function for NRF52.

[3076](https://github.com/ARMmbed/mbed-os/pull/3076): STM32F1: Correct timer master value reading

[3085](https://github.com/ARMmbed/mbed-os/pull/3085): Add LOWPOWERTIMER capability for NUCLEO_F303ZE

[3093](https://github.com/ARMmbed/mbed-os/pull/3093): [SDFileSystem] Enable / Disable serial debug.

[3097](https://github.com/ARMmbed/mbed-os/pull/3097): Arm-Pack-Manager Remove pycurl dependency

[3046](https://github.com/ARMmbed/mbed-os/pull/3046): [BEETLE] Update BLE stack on Beetle board

[3005](https://github.com/ARMmbed/mbed-os/pull/3005): New build profile and docs

[3122](https://github.com/ARMmbed/mbed-os/pull/3122): [Silicon Labs] Update of Silicon Labs HAL

[3022](https://github.com/ARMmbed/mbed-os/pull/3022): OnSemi RAM usage fix

[3121](https://github.com/ARMmbed/mbed-os/pull/3121): STM32F3: Correct UART4 and UART5 defines when using DEVICE_SERIAL_ASYNCH

[2897](https://github.com/ARMmbed/mbed-os/pull/2897): nsapi - Standardize support of NSAPI_UNSPEC

[3024](https://github.com/ARMmbed/mbed-os/pull/3024): analog_loop tests update for STM32

[3142](https://github.com/ARMmbed/mbed-os/pull/3142): Targets- NUMAKER_PFM_NUC47216 remove mbed 2


### Using the release

You can fetch the mbed OS 5.2.1 release from the [mbed-os GitHub](https://github.com/ARMmbed/mbed-os) repository,
using the tag "mbed-os-5.2.1".

Please feel free to ask any questions or provide feedback on this release [on the forum](https://forums.mbed.com/), or to contact us at [support@mbed.org](mailto:support@mbed.org).

## mbed OS 5.2.0 - 21st October 2016

This is the release note for mbed OS 5.2.0, summarizing the major enhancements in this version. 

You can find the [mbed OS 5.2.0 release on GitHub](https://github.com/ARMmbed/mbed-os/releases/tag/mbed-os-5.2.0). 

### About this release 

This release builds on the [significant enhancements that came in mbed OS 5.1](../5_1/release.md) to add the following headline features: 

- WiFi SoCs and Modules – mbed OS now supports flexible integration for different SoC, Module and Network Processor WiFi architectures, opening up fully integrated platforms as development targets. As part of this work, the IP stack has also been upgraded to the latest LwIP version (2.0), bringing support for both IPv4 and IPv6 to Ethernet and WiFi targets. 
  
- Hardware Entropy – mbed OS now supports integration of Hardware Entropy sources, essential for strong platform security. Partners with targets containing True Random Number Generators (TRNGs) have already been integrating support so developers will be able to automatically take advantage of enhanced security. 
 
- Memory Profiling - mbed OS core components and tools have received a number of enhancements to allow memory footprint tracking and analysis. This includes runtime tools for tracking of dynamic memory utilisation and heap information, and stack checking to trap stack over-runs.  
 
mbed OS 5.2 also extends target support to over 60 target platforms. 

The following sections provide more details of these and other changes in this release. 

### Core 

An Events library is now part of the core platform, providing simple primitives for scheduling one-time or repeating events. The library can act as a drop-in scheduler, provide synchronization between multiple threads, or just act as a mechanism for moving events out of interrupt contexts.  

We have added dynamic memory profiling features, allowing tracing the maximum heap usage at runtime, as well as invoking callbacks on each memory operation for more sophisticated annotation. Statistics, including current and maximum bytes allocated and the number of allocations, give visibility of the dynamic memory behavior that can be used in test regression scripts, alongside the existing static memory footprint analysis information. 
 
### Security 

A portable HAL adds support for strong hardware entropy sources such as on-chip True Random Number Generators (TRNGs). These are used as part of the entropy pool the security functions of mbed OS rely on, ensuring each platform uses the maximum hardware-based security it can provide. 

Cipher-based Message Authentication Code (CMAC) support is added, and used in the mbed OS Thread stack.   

The version of mbed TLS integrated within mbed OS has been upgraded to the latest version (2.4.0). For more details, see the [mbed TLS 2.4.0 release note](https://tls.mbed.org/tech-updates/releases/mbedtls-2.4.0-2.1.6-and-1.3.18-released]). 

### Connectivity 

We have introduced support for different WiFi hardware architectures, enabling mbed OS to run on integrated WiFi SoCs and modules as well as work with companion WiFi network processors. This provides hardware design flexibility, and opportunities for significant BOM and complexity reduction, by running mbed OS on the WiFi modules themselves.   

The developer-facing WiFi APIs use the existing mbed OS socket interfaces (used by all IP networking) and network control features. The APIs bring up an interface, including setting the security credentials, scanning for available network access points and to read the signal strength (RSSI) for the current active connection.  

This release introduces support for the u-blox ODIN-W2 integrated WiFi module. We are actively working with a number of other WiFi partners that will be introducing support for their WiFi targets in forthcoming patch releases. 

The core IP stack used in mbed OS for Ethernet and WiFi has been upgraded to LwIP 2.0, bringing support for both IPv4 and IPv6. This complements our mesh networking stack, already optimised for providing 6LoWPAN and Thread networking support for 2.4GHz and Sub-GHz 802.15.4 radios.  

### Services 

The mbed Device Connector Client is now delivered as a separate module that will be updated as new mbed device management services are introduced.  

### Tools and workflow 

The mbed CLI tool has had numerous updates and improvements. For more details, see the [mbed CLI repository](https://github.com/ARMmbed/mbed-cli). 

The tools now support toolchain profiles, in particular to enable simple debug and release configurations. 

The Online IDE now supports git and GitHub repositories, so you can use both mercurial and GitHub distributed version control systems. 

The export mechanism supporting project generation for different toolchains and IDEs has been redeveloped to be more versatile and scalable, and now uses CMSIS-Packs for target information. When exporting to MDK and IAR, the corresponding target CMSIS-Packs must be available. Known issues include limited target coverage, needing additional configuration steps in IDEs to have projects fully functional, and exporters for Make may have linking errors where archives are used. We will be working with our silicon and tools partners to improve target coverage and project generation in future patch releases.

### mbed Enabled 

The mbed Enabled program continues to provide compliance criteria and technical requirements for boards, on-board interfaces and end products. It is unchanged for mbed OS 5.2, but we expect to introduce stricter requirements for Hardware Entropy support in future releases. 

The following resources are available: 

* The [mbed Enabled requirements documents](https://www.mbed.com/en/about-mbed/mbed-enabled/mbed-enabled-program-requirements/).
* The [mbed Enabled application form](https://docs.google.com/forms/d/e/1FAIpQLSf87Qw7FsDelw9L4q_sB8QW3Hy5aff5WRwZUhPlNzf2Xm6iVw/viewform).

### Targets 

Thanks to our partners’ hard work, mbed OS 5.2 has been extended to support over 60 targets. 

We will continue to add new targets in our bi-weekly releases as partners introduce support. If you are a partner, please see details in the [Partner Portal](https://partners.mbed.com/en/partner-login/). 

### Getting Started 

To get started with this release, see [the Handbook](https://docs.mbed.com/docs/mbed-os-handbook/en/5.2/). 
