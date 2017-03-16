# mbed OS 5.4 Releases

## mbed OS 5.4.1 release

We are pleased to announce the [mbed OS 5.4.1 release](https://github.com/ARMmbed/mbed-os/releases/tag/mbed-os-5.4.1) is now available.

This release includes an update of mbed TLS to version 2.4.2, bringing essential and critical security patches, including a fix for CVE-2017-2784. For core mbed OS, there are a number of bug fixes to improve the stability of the code and improvements to the tools. 

### Fixes and Changes

[3716](https://github.com/ARMmbed/mbed-os/pull/3716): fix for issue #3715: correction in startup files for ARM and IAR, alignment of system_stm32f429xx.c files

[3741](https://github.com/ARMmbed/mbed-os/pull/3741): STM32 remove warning in hal_tick_32b.c file

[3780](https://github.com/ARMmbed/mbed-os/pull/3780): STM32L4 : Fix GPIO G port compatibility

[3831](https://github.com/ARMmbed/mbed-os/pull/3831): NCS36510: SPISLAVE enabled (Conflict resolved)

[3832](https://github.com/ARMmbed/mbed-os/pull/3832): lwip: Increase timeout on network tests with python projects

[3836](https://github.com/ARMmbed/mbed-os/pull/3836): Allow to redefine nRF's PSTORAGE_NUM_OF_PAGES outside of the mbed-os

[3840](https://github.com/ARMmbed/mbed-os/pull/3840): STM32: gpio SPEED - always set High Speed by default

[3844](https://github.com/ARMmbed/mbed-os/pull/3844): STM32 GPIO: Typo correction. Update comment (GPIO_IP_WITHOUT_BRR)

[3846](https://github.com/ARMmbed/mbed-os/pull/3846): STORAGE: removal of unsupported tests having ported to sd-driver repository

[3850](https://github.com/ARMmbed/mbed-os/pull/3850): STM32: change spi error to debug warning

[3860](https://github.com/ARMmbed/mbed-os/pull/3860): Define GPIO_IP_WITHOUT_BRR for xDot platform

[3875](https://github.com/ARMmbed/mbed-os/pull/3875): Add post-build hook white-list to exporters

[3880](https://github.com/ARMmbed/mbed-os/pull/3880): DISCO_F469NI: allow the use of CAN2 instance when CAN1 is not activated

[3897](https://github.com/ARMmbed/mbed-os/pull/3897): Ignore FuzzyWuzzy warnings

[3898](https://github.com/ARMmbed/mbed-os/pull/3898): Prevent underflow in heap size calculation

[3913](https://github.com/ARMmbed/mbed-os/pull/3913): [NRF51822] Fix reference to sleep in hal_patch override

[3795](https://github.com/ARMmbed/mbed-os/pull/3795): Fix pwm period calc

[3828](https://github.com/ARMmbed/mbed-os/pull/3828): STM32 CAN API: correct format and type

[3842](https://github.com/ARMmbed/mbed-os/pull/3842): TARGET_NRF: corrected spi_init() to properly handle re-initialization

[3843](https://github.com/ARMmbed/mbed-os/pull/3843): STM32L476xG: set APB2 clock to 80MHz (instead of 40MHz)

[3852](https://github.com/ARMmbed/mbed-os/pull/3852): Ignore build directory from scan resources

[3866](https://github.com/ARMmbed/mbed-os/pull/3866): bd: Fix missing const attributes on functions

[3879](https://github.com/ARMmbed/mbed-os/pull/3879): NUCLEO_F446ZE: Add missing AnalogIn pins on PF_3, PF_5 and PF_10.

[3877](https://github.com/ARMmbed/mbed-os/pull/3877): Update mbed TLS feature to mbedtls-2.4.2

[3902](https://github.com/ARMmbed/mbed-os/pull/3902): Fix heap and stack size for NUCLEO_F746ZG

[3864](https://github.com/ARMmbed/mbed-os/pull/3864): Fix mbed 2 builds

[3829](https://github.com/ARMmbed/mbed-os/pull/3829): can_write(): return error code when no tx mailboxes are available 


### Using the release

You can fetch the mbed OS 5.4.1 release from the [mbed-os GitHub](https://github.com/ARMmbed/mbed-os) repository, using the tag "mbed-os-5.4.1".

Please feel free to ask any questions or provide feedback on this release [on the forum](https://forums.mbed.com/), or to contact us at [support@mbed.org](mailto:support@mbed.org).

## mbed OS 5.4.0 release
 
This is the release note for ARM mbed OS 5.4.0. It summarizes the major enhancements in this version. 

You can find the mbed OS 5.4.0 release on [GitHub](https://github.com/ARMmbed/mbed-os/tree/mbed-os-5.4).

## About this release

mbed OS 5.4.0 incorporates functionality you can use to prepare for the upcoming mbed Cloud device management services. This includes bootloader and filesystem infrastructure and the certified Thread 1.1 stack for developers. In addition, this release contains many minor fixes and enhancements and brings target platform support up to 74 targets.

The following sections provide more details about this release.

## Core

mbed OS 5.4 adds flexible filesystem support to address the needs of IoT applications requiring storage within the end node. This release already includes a FAT filesystem implementation for removable media, such as SD cards, and future releases will add embedded flash filesystems and encryption.

The filesystem is integrated with the C standard libraries of the ARM, IAR and GCC compilers. It is available for use across all mbed Enabled platforms.

The release also includes early access to the mbed OS bootloader, so partners can add support for their targets' flash controllers. This forms part of the support for the upcoming mbed Cloud Update service, which allows managing device firmware update campaigns.

To read the documentation, see [file system](https://docs.mbed.com/docs/mbed-os-api-reference/en/latest/APIs/storage/filesystem/) and [bootloader](https://docs.mbed.com/docs/mbed-os-handbook/en/latest/advanced/bootloader/).

## Connectivity

mbed OS 5.4 uses the recently certified mbed Thread 1.1 stack to provide solutions for building end nodes and border routers.

A Linux-based Access Point reference that uses the Thread border router is also available.

The mbed OS [LoRaWAN APIs](https://github.com/ARMmbed/mbed-os/tree/feature-lorawan/features/FEATURE_LORAWAN) are available for partner feedback and integration.

## Security

The mbed crypto libraries in mbed TLS include all the internal partner APIs and documentation for enabling hardware entropy and symmetric and asymmetric cryptographic acceleration. Partners are working on implementations for their target platforms, and a partner workshop will support them. We expect support for the first set of targets in 5.5.

## Upcoming

The feature branch work on our [CMSIS5 and CMSIS-RTOS2](https://github.com/ARMmbed/mbed-os/tree/feature_cmsis5/rtos) upgrade is nearing completion, so testing will begin soon after the release of 5.4. We are aiming for inclusion on mainline for 5.5.

Throughout the year, we also plan a program of upgrading supported compilers to ensure the latest features and fixes from the different ARM compilers are available to developers; this will mean supporting ARM GCC Embedded 6, ARM Compiler 6 and IAR Embedded Workbench 8.

If you would like to be involved in helping test any of these upgrades to help minimize the effect on developers, please contact us.

## Targets

Thanks to our partners’ hard work, mbed OS 5.4 now supports 74 [target platforms](https://developer.mbed.org/platforms/).

We will continue to add new targets in our biweekly releases as partners introduce support.

## Fixes and changes

Please see the mbed-os GitHub repository referenced below for a full list of changes introduced in this release. You can find a list of known issues [here](https://github.com/ARMmbed/mbed_os_release_notes/blob/master/Docs/5_4/known_issues.md).

##Using the release

You can fetch the mbed OS 5.4.0 release from the [mbed-os GitHub](https://github.com/ARMmbed/mbed-os) repository using the tag “mbed-os-5.4.0”.

Please feel free to ask any questions or provide feedback about this release on the forum, or to contact us at [support@mbed.org](mailto:support@mbed.org).
