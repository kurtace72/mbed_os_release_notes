# mbed OS 5.5 Releases

This is the release note for ARM mbed OS 5.5. It summarizes the major enhancements in this version. You can find the mbed OS 5.5.0 release on [GitHub](https://github.com/ARMmbed/mbed-os/tree/mbed-os-5.5).

## About this release

The mbed OS 5.5 release upgrades to the latest version of CMSIS, paving the way for support of the latest ARM compilers, ARMv8-M based MCUs, and lower power RTOS modes. It also introduces cellular connectivity, embedded storage and hardware security enhancements to further simplify development of connected, managed IoT devices. In addition, this release contains many minor fixes and enhancements and brings target platform support up to 85 targets.

## Core 

mbed OS 5.5 upgrades to the latest CMSIS version, CMSIS5, including the enhanced CMSIS-RTOS2 kernel. This is a significant step in our roadmap to enable support for the latest generation of compilers (ARM GCC Embedded 6, ARM Compiler 6 and IAR Embedded Workbench 8), support for v8-M architecture cores, and introduction of low power tick-less RTOS and deep sleep modes. It also includes many general enhancements and fixes including upstreaming those that have been maintained within the mbed OS codebase itself. The upgrade should be generally transparent to developers using the mbed OS RTOS APIs, but please report in the forums[https://developer.mbed.org/forum/bugs-suggestions/] or contact us at support@mbed.com if you have any issues in this area.

The file system infrastructure now supports external SPI NOR FLASH devices. SPI NOR FLASH is a very low cost storage solution. Developers commonly use it in IoT devices to store firmware update images, device credentials and configuration information and to cache data for later syncing to the cloud. You can use the SPI NOR Flash storage with all mbed Enabled platforms, and is the recommended storage medium for devices requiring firmware update capabilities.

The release also includes a standard in-application flash programming API, FlashIAP, and first partner implementations. This component supports the upcoming mbed Cloud Update service, which manages device firmware update campaigns across fleets of devices.

## Connectivity 

mbed OS 5.5 introduces improved support for cellular connectivity modules, including standard integration via a built-in PPP network interface.

A Linux-based Thread Access Point reference that uses the Thread border router [is now available](INSERT LINK).

Our new native mbed OS BLE stack has reached our Early Partner Release milestone. This allows use of BLE transceivers with any mbed Enabled MCU, and to provide stack consistency across different BLE hardware. Based on this, we will be working with the first mbed Partners to enable support for their BLE transceivers and SoCs using this stack, planning to provide first access to developers in the 5.6 release. Partners interested in supporting BLE transceivers or SoCs with this stack should contact their Partner Enablement Team representative.

## Security 

mbed OS cryptography incorporates mbed TLS 2.5 and the completion of internal APIs for enabling hardware entropy, symmetric and asymmetric cryptographic acceleration. Many partners are implementing and landing support for acceleration on their target platforms and are seeing significant performance increases. Partner acceleration will land in patch releases as we work with partners to complete security audits and mainline these contributions.

uVisor is updated to address several performance and usability issues reported since the last release. Secure boxes on devices with an ARMv7-M MPU now use less memory and provide more user-friendly configuration options.

uVisor now also supports the new ARMv8-M architecture, including the TrustZone for ARMv8-M security extensions. Support for this architecture is still experimental and is currently only accessible through [a feature branch in mbed OS](INSERT LINK).

## Targets

Thanks to our partners’ hard work, mbed OS 5.5 now supports 85 target platforms.

We'll continue to add targets in our biweekly patch releases as partners work with us on support.

## Fixes and changes

Please see the [mbed OS GitHub repository](https://github.com/ARMmbed/mbed-os/tree/mbed-os-5.5) for a full list of changes introduced in this release. You can find a list of known issues [here](INSERT LINK).

## Using the release 

You can fetch the latest version of the mbed OS 5.5 release from the `mbed-os` GitHub repository using the branch “[mbed-os-5.5](https://github.com/ARMmbed/mbed-os/tree/mbed-os-5.5)”.

Please feel free to ask any questions or provide feedback about this release on the forum[https://developer.mbed.org/forum/], or to contact us at support@mbed.org.
