# mbed OS 5.3 releases
This is the release note for mbed OS 5.3.0, summarizing the major enhancements in this version. 
You can find the mbed OS 5.3.0 release on GitHub. 

##About this release 
This release makes available early versions of key features we are working on in development branches, alongside many enhancements and bug fixes to our stable release codeline. This release will be of particular interest to partners and developers who would like to work with us on these features ahead of them being made generally available. 

The headline feature developments made available are: 

- Initial [CMSIS5 and CMSIS-RTOS2](https://github.com/ARMmbed/mbed-os/tree/feature_cmsis5) upgrade
- Integration points for [Hardware Acceleration of Symmetric and Asymmetric Encryption](https://github.com/ARMmbed/mbed-os/tree/feature_hw_crypto)
- Introduction of native [LoRaWAN APIs](https://github.com/ARMmbed/mbed-os/tree/feature-lorawan) 

mbed OS 5.3 supports 70 target platforms. 

The following sections provide more details of these and other changes in this release. 

##Core 
A first functional integration of the next generation CMSIS5 libraries, including the new CMSIS-RTOS2 RTOS kernel. This upgrade is integrated under the mbed OS Peripheral and RTOS APIs such that it will have little or no impact on developers, but provides important enhancements that can be taken advantage of internally. 

These enhancements include: 

- Primitives and integration points for supporting TrustZone for Cortex-M and uVisor 
- Improved RTOS kernel 
- Support for ARM Compiler 6 
- Many patches and modifications that mbed OS had made to CMSIS4 and CMSIS-RTOS now incorporated directly in to the CMSIS5 and CMSIS-RTOS2 codebases 

This allows tracking of the latest CMSIS5 development, and will be brought in to the mainline release when it is ready. Impact on end developers when this happens should be very limited, but open up further opportunities for mbed OS functionality and portability.  

##Security 
Building on the Hardware Entropy work in mbed OS 5.2, mbed OS 5.3 adds the integration points for implementing Hardware Acceleration on different target platforms. This support extends to both Symmetric and Asymmetric encryption operations, and when implemented for a target will transparently provide benefit for developers directly or indirectly using functions that rely on TLS/DTLS or other Cryptographic operations. 

Partners looking to provide implementations for their targets should contact their ARM Partner Enablement representative for guidance, such that support can be made available for developers using their platforms in future mbed OS releases.      

##Connectivity 
New LoRaWAN APIs are introduced to provide native development support for LoRaWAN applications on any mbed Enabled LoRa hardware. These APIs are available for partners and developers to analyze and help refine whilst the full mbed OS LoRaWAN stack is integrated, ahead of making it available as part of our mainline release. In particular, please contact us if you have an interest in LoRa and LoraWAN as a module manufacturer, OEM product developer or network provider.  

Wi-Fi support has also been further improved, with built in support for both the u-blox ODIN-W2 and Espressif ESP8266 modules. Look out for further partner support, which will become available in patch releases. 

##Targets 
Thanks to our partners’ hard work, mbed OS 5.3 supports 70 [targets platforms](https://developer.mbed.org/platforms/). 

We will continue to add new targets in our bi-weekly releases as partners introduce support.  

##Fixes and Changes 
Please see the mbed-os GitHub repository referenced below for a full list of changes introduced in this release. 

##Using the release 
You can fetch the mbed OS 5.3.0 release from the [mbed-os GitHub](https://github.com/ARMmbed/mbed-os) repository, using the tag “mbed-os-5.3.0”. 

Please feel free to ask any questions or provide feedback on this release on the forum, or to contact us at [support@mbed.org](mailto:support@mbed.org).
 
