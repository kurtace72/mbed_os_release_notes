### Known issues

This is the list of known issues for the [5.5.0 release of mbed OS and related tools](https://docs.mbed.com/docs/mbed-os-release-notes/en/latest/5_5/release_note/).

We publish mbed OS as a collection of modules on GitHub. Issues are raised in the specific repositories, and we then track the issues internally. The purpose of this document is to provide a single view of the outstanding key issues that have not been addressed for this release. It is a filtered and reviewed list based on priority and potential effect. Each item summarizes the problem and includes any known workarounds, along with a link to the GitHub issue if applicable. We welcome any comments or proposed solutions.

For more information about an issue, contact us on the [forums](http://developer.mbed.org/forums).

#### mbed TLS accepts certificates that use weak signature algorithms

* **Description**: mbed TLS accepts X.509 certificates that use the following signature algorithms: `md4WithRSAEncryption`, `md5WithRSAEncryption` and `sha1WithRSAEncryption`. These algorithms are considered weak or unsafe due to the hashing algorithms used.
* **Workaround**: For mbed TLS 2.1 and above, the default mbed TLS profile for `mbedtls_x509_crt_verify()` excludes all these weak algorithms and is safe to use. There are no known workarounds for mbed TLS 1.3.
* **Reported Issue**: Received via email.
* **Priority**: Critical

#### Handshake messages are not fragmented as per `MaxFragmentLength` Extension Negotiation

* **Description**: "Once a maximum fragment length other than 2^14 has been successfully negotiated, the client and server MUST immediately begin fragmenting messages (including handshake messages) to ensure that no fragment larger than the negotiated length is sent." In mbed TLS, only the application data is fragmented, and the handshake messages are not.
* **Workaround**: Disable `MaxFragmentLength` Extension Negotiation.
* **Reported Issue**: [https://github.com/ARMmbed/mbedtls/issues/387](https://github.com/ARMmbed/mbedtls/issues/387)
* **Priority**: Major

#### IP addresses in the X.509 certificate `subjectAltNames`

* **Description**: Parsing IP addresses in the X.509 certificate `subjectAltNames` is not supported yet. Certificate chains relying on IP addresses in `subjectAltNames` return a `BADCERT_CN_MISMATCH` error.
* **Workaround**: Merge branch [https://github.com/ARMmbed/mbedtls/tree/iotssl-602-san-ip](https://github.com/ARMmbed/mbedtls/tree/iotssl-602-san-ip) into your copy of mbed TLS before building the application. It is still in EXPERIMENTAL stage; use it on your own responsibility!
* **Reported Issue**: Issue reported by a customer in email.
* **Priority**: Major

#### Mismatch of root CA and issuer of CRL not caught

* **Description**: The `x509_crt_verifycrl()` function ignores the CRL when the CRL has an issuer different from the subject of the root CA certificate.
* **Workaround**: Make sure that the issuer of the CRL and the root CA certificate's subject are the same before passing them to `x509_crt_verifycrl()`.
* **Reported Issue**: Reported by a partner.
* **Priority**: Major

#### mbed TLS causes stack overflow in mbed OS targets

* **Description**: The stack memory usage of some mbed TLS features is higher than 4 KB, which may cause stack overflow errors when running in constrained embedded environments with mbed OS, which are particularly limited in RAM.
* **Workaround**: The amount of stack required is dependent on the application and what features of the library it chooses to use. More intensive, demanding tasks may not be possible on more limited, constrained devices, so we recommend designing for the limitations of the target device or choosing a device suitable for your application.
* **Reported Issue**: [https://github.com/ARMmbed/mbed-os-example-tls/issues/14](https://github.com/ARMmbed/mbed-os-example-tls/issues/14)
* **Priority**: Major

#### Commissioner does not retransmit message when it receives retransmission

* **Description**: There are two issues with DTLS handshake retransmission. First, the joiner fails to correctly parse received records because it does not correctly handle queued retransmissions received. Second, the commissioner may cause a deadlock because it does not retransmit certain records after it receives retransmission as instructed in RFC6347 Section 4.2.4.
* **Workaround**: There is no known workaround.
* **Reported Issue**: [https://github.com/openthread/openthread/pull/1207](https://github.com/openthread/openthread/pull/1207)
* **Priority**: Major

#### uVisor does not support nested interrupts

* **Description**: When running an application with uVisor enabled, nested interrupts are not supported.
* **Workaround**: There is no available workaround at the moment.
* **Reported Issue**: [https://github.com/ARMmbed/uvisor/issues/345](https://github.com/ARMmbed/uvisor/issues/345)
* **Priority**: Major

#### On ARMv7-M targets supporting uVisor, the RTOS runs with the same privilege as uVisor

* **Description**: The current architecture of uVisor and of RTX require the RTOS to run with the same privilege as uVisor. As such, the RTOS is considered trusted.
* **Workaround**: There is no available workaround at the moment.
* **Reported Issue**: [https://github.com/ARMmbed/uvisor/issues/235](https://github.com/ARMmbed/uvisor/issues/235)
* **Priority**: Major

#### `mbed-os-example-client` linking fails in ARMCC for Realtek board

* **Description**: `mbed-os-example-client` takes more flash space than reserved for Realtek board. For it to link properly, more code has to move to SDRAM, which is not yet implemented or tested.
* **Workaround**: There is no available workaround at the moment.
* **Reported Issue**: [https://github.com/ARMmbed/mbed-os/issues/4462](https://github.com/ARMmbed/mbed-os/issues/4462)
* **Priority**: Major

#### Mesh networking applications fails to compile with IAR on unsecure platform

* **Description**: If the target has not defined a source of hardware entropy, then mbed TLS support is disabled. This leads to compilation warnings on some Nanostack related modules and compilation failure when using IAR toolchain.
* **Workaround**: There is no available workaround at the moment.
* **Reported Issue**: [https://github.com/ARMmbed/mbed-os-example-mesh-minimal/issues/91](https://github.com/ARMmbed/mbed-os-example-mesh-minimal/issues/91)
* **Priority**: Major

#### UARTSerial asserts if debug is enabled

* **Description**: UARTSerial attempts to claim a mutex from interrupt context. If debug is not enabled, this fails silently, and the driver works as intended. If debug is enabled, the system stops in the assert.
* **Workaround**: Turn off the debug build.
* **Reported Issue**: [https://github.com/ARMmbed/mbed-os/issues/4537](https://github.com/ARMmbed/mbed-os/issues/4537)  

#### Introduction of RTX/CMSIS 5 has broken semaphore signaling

* **Description**: RTX 5 reduced the semaphore count limit from UINT16_MAX to the arbitrary value 1024 and added an assert that would halt if the semaphore count exceeded this limit. This is especially problematic for applications that are using the semaphore for signaling. In RTX 4, the semaphore was the only library-friendly mechanism available for signaling, and in RTX 5 it is still the only option for the C++ layer. This breaks a number of the higher-level APIs.
* **Workaround**: None
* **Reported Issue**: [https://github.com/ARMmbed/mbed-os/issues/4584](https://github.com/ARMmbed/mbed-os/issues/4584)
* **Priority**: Critical
