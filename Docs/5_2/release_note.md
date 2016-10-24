# mbed OS 5.2 releases

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
