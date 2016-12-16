# mbed OS 5.3 known issues

## About this document

This is the list of known issues for the [mbed OS 5.3.0 release](https://docs.mbed.com/docs/mbed-os-release-notes/en/latest/5_3/release_note/). 

The purpose of this document is to provide a single view of the key outstanding issues that have been identified for this release. 
As such it is a filtered and reviewed list based on priority and potential impact. Each item summarizes the problem and includes any 
known workarounds, along with a link to the GitHub issue (if applicable). We welcome any comments or proposed solutions.

For more information about an issue, contact us on the [forums](https://developer.mbed.org/forum/).

## Known issues

### [Beetle] BLE scan doesn't work on BLE.
* **Description**: On the beetle board, BLE scanning doesn't work and the scan procedure will never report any advertisement even if the procedure has been successfully launched.
* **Workaround**: None
* **Reported Issue**: [https://github.com/ARMmbed/mbed-os/issues/3400](https://github.com/ARMmbed/mbed-os/issues/3400)

## Odin Ethernet requires configuration
* **Description**: The default network interface for the Odin is Wi-Fi.
* **Workaround**: Make Ethernet the default interface by removing “EMAC” from “device_has” in targets.json
* **Reported Issue**: [https://github.com/ARMmbed/mbed-os/issues/3419](https://github.com/ARMmbed/mbed-os/issues/3419)

## sockets do not work for NUCLEO_F746ZG using IAR toolchain
* **Description**: The mbed-os-example-sockets program doesn't work when building with IAR  
* **Workaround**: None
* **Reported Issue**: [https://github.com/ARMmbed/mbed-os/issues/3387](https://github.com/ARMmbed/mbed-os/issues/3387) 

## NUMAKER_ PFM_NUC472 does not work with uvision
* **Description**: Error says IPv4 or IPv6 must be enabled
* **Workaround**: None
* **Reported Issue**: [https://github.com/ARMmbed/mbed-os/issues/3418](https://github.com/ARMmbed/mbed-os/issues/3418)

## mbed TLS causes stack overflow in mbed OS targets
* **Description**:
The stack memory usage of some mbed TLS features is higher than 4 KB, which may cause stack overflow errors when running in constrained embedded environments with mbed OS which are particularly limited in RAM.
* **Workaround**: The amount of stack required is very dependent on the application, and what features of the library it chooses to use. Obviously more intensive, demanding tasks may not be possible on more limited, constrained devices, so we recommend designing for the limitations of the target device, or choosing a device suitable for your application.
* **Reported Issue**: [https://github.com/ARMmbed/mbed-os-example-tls/issues/14](https://github.com/ARMmbed/mbed-os-example-tls/issues/14)

## DTLS renegotiation checks also compares record epoch value
* **Description**:
The TLS renegotiation routines are executed after the DTLS record sequence number for incoming or outgoing messages has exceeded a user-defined period. According with the RFC 6347 Section 4.3.1 the record sequence is an 6 byte unsigned integer, but the mbed TLS function `ssl_check_ctr_renegotiate()` compares 8 bytes. The additional 2 bytes correspond to the record epoch value, which may result in the incorrect execution of the renegotiation routines.
* **Workaround**: There is no known workaround for this issue.
* **Reported Issue**: [https://github.com/ARMmbed/mbedtls/issues/687](https://github.com/ARMmbed/mbedtls/issues/687)
