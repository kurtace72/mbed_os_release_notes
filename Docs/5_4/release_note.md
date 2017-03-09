#mbed OS 5.4.0 Release
 
This is the release note for ARM mbed OS 5.4.0. It summarizes the major enhancements in this version. 

You can find the mbed OS 5.4.0 release on [GitHub](https://github.com/ARMmbed/mbed-os/tree/mbed-os-5.4).

##About this release

mbed OS 5.4.0 incorporates functionality you can use to prepare for the upcoming mbed Cloud device management services. This includes bootloader and filesystem infrastructure and the certified Thread 1.1 stack for developers. In addition, this release contains many minor fixes and enhancements and brings target platform support up to 74 targets.

The following sections provide more details about this release.

##Core

mbed OS 5.4 adds flexible filesystem support to address the needs of IoT applications requiring storage within the end node. This release already includes a FAT filesystem implementation for removable media, such as SD cards, and future releases will add embedded flash filesystems and encryption.

The filesystem is integrated with the C standard libraries of the ARM, IAR and GCC compilers. It is available for use across all mbed Enabled platforms.

The release also includes early access to the mbed OS bootloader, so partners can add support for their targets' flash controllers. This forms part of the support for the upcoming mbed Cloud Update service, which allows managing device firmware update campaigns.

To read the documentation, see [file system](https://docs.mbed.com/docs/mbed-os-api-reference/en/latest/APIs/storage/filesystem/) and [bootloader](https://docs.mbed.com/docs/mbed-os-handbook/en/latest/advanced/bootloader/).

##Connectivity

mbed OS 5.4 uses the recently certified mbed Thread 1.1 stack to provide solutions for building end nodes and border routers.

A Linux-based Access Point reference that uses the Thread border router is also available.

The mbed OS [LoRaWAN APIs](https://github.com/ARMmbed/mbed-os/tree/feature-lorawan/features/FEATURE_LORAWAN) are available for partner feedback and integration.

##Security

The mbed crypto libraries in mbed TLS include all the internal partner APIs and documentation for enabling hardware entropy and symmetric and asymmetric cryptographic acceleration. Partners are working on implementations for their target platforms, and a partner workshop will support them. We expect support for the first set of targets in 5.5.

##Upcoming

The feature branch work on our [CMSIS5 and CMSIS-RTOS2](https://github.com/ARMmbed/mbed-os/tree/feature_cmsis5/rtos) upgrade is nearing completion, so testing will begin soon after the release of 5.4. We are aiming for inclusion on mainline for 5.5.

Throughout the year, we also plan a program of upgrading supported compilers to ensure the latest features and fixes from the different ARM compilers are available to developers; this will mean supporting ARM GCC Embedded 6, ARM Compiler 6 and IAR Embedded Workbench 8.

If you would like to be involved in helping test any of these upgrades to help minimize the effect on developers, please contact us.

##Targets

Thanks to our partners’ hard work, mbed OS 5.4 now supports 74 [target platforms](https://developer.mbed.org/platforms/).

We will continue to add new targets in our biweekly releases as partners introduce support.

##Fixes and changes

Please see the mbed-os GitHub repository referenced below for a full list of changes introduced in this release. You can find a list of known issues [here](https://github.com/ARMmbed/mbed_os_release_notes/blob/master/Docs/5_4/known_issues.md).

##Using the release

You can fetch the mbed OS 5.4.0 release from the [mbed-os GitHub](https://github.com/ARMmbed/mbed-os) repository using the tag “mbed-os-5.4.0”.

Please feel free to ask any questions or provide feedback about this release on the forum, or to contact us at [support@mbed.org](mailto:support@mbed.org).
