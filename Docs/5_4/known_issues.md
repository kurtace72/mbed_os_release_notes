# mbed OS Known Issues

## About this document

This is the list of known issues for the [5.4.0 release of mbed OS and related tools](https://docs.mbed.com/docs/mbed-os-release-notes/en/latest/5_4/release_note/).

We publish mbed OS as a collection of modules on GitHub. Issues are raised in the specific repositories and then tracked internally. The purpose of this document is to provide a single view of the outstanding key issues that have not been addressed for this release. As such, it is a filtered and reviewed list based on priority and potential effect. Each item summarizes the problem and includes any known workarounds, along with a link to the GitHub issue (if applicable). We welcome any comments or proposed solutions.

For more information about an issue, contact us on the [forums](http://forums.mbed.com).

## Additional information

For further information regarding this release, please refer to the release notes referenced above.

# Known issues

## Online IDE does not support multiple binary production

* **Description**: Compiling an application with bootloader only produces the standalone application binary. It should produce the composite binary.

* **Workaround**: Use mbed CLI.

* **Reported Issue**: https://github.com/ARMmbed/mbed-os-example-bootloader-blinky/issues/4

* **Priority**: MAJOR

## mbed TLS causes stack overflow in mbed OS targets

* **Description**: The stack memory usage of some mbed TLS features is higher than 4 KB, which may cause stack overflow errors when running in constrained embedded environments with mbed OS, which are particularly limited in RAM.

* **Workaround**: The amount of stack required depends on the application and what features of the library it chooses to use. More intensive, demanding tasks may not be possible on more limited, constrained devices, so we recommend designing for the limitations of the target device or choosing a device suitable for your application.

* **Reported Issue**: https://github.com/ARMmbed/mbed-os-example-tls/issues/14

* **Priority**: MAJOR

## mbed TLS DTLS renegotiation checks also compare record epoch value

* **Description**: The TLS renegotiation routines execute after the DTLS record sequence number for incoming or outgoing messages has exceeded a user-defined period. According to the RFC 6347 Section 4.3.1, the record sequence is a 6 byte unsigned integer, but the mbed TLS function `ssl_check_ctr_renegotiate()` compares 8 bytes. The additional 2 bytes correspond to the record epoch value, which may result in the incorrect execution of the renegotiation routines.

* **Workaround**: There is no known workaround for this issue.

* **Reported Issue**: https://github.com/ARMmbed/mbedtls/issues/687

* **Priority**: MAJOR

 
## mbed TLS server does not check that TLS_FALLBACK_SCSV is the last cipher suite

* **Description**: An mbed TLS server does not check that the TLS_FALLBACK_SCSV value is the last element in the cipher suites part of the ClientHello message. Note that RFC7505 Section 4 states that placing the SCSV at that position is a SHOULD for the client. However, the server behavior description in RFC7505 Section 5 does not prescribe anything regarding the location of the TLS_FALLBACK_SCSV in the ClientHello.

* **Workaround**: There is no known workaround for this issue.

* **Reported Issue**: https://github.com/ARMmbed/mbedtls/issues/810

* **Priority**: MAJOR

 
## mbed TLS commissioner does not retransmit message when it receives retransmission

* **Description**: There are two issues with DTLS handshake retransmission. First, the joiner fails to correctly parse received records because it does not correctly handle queued retransmissions received. Second, the commissioner may cause a deadlock because it does not retransmit certain records after it receives retransmission as instructed in RFC6347 Section 4.2.4.

* **Workaround**: There is no known workaround.

* **Reported Issue**: https://github.com/openthread/openthread/pull/1207

* **Priority**: MAJOR