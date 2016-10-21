# mbed OS 5.2 known issues

## mbed OS 5.2.0

1. UBLOX_EVK_ODIN_W2 - mbed-os-example-client - no connection established when using WiFi.
1. ARM_BEETLE_SOC does not support IAR and uVision export.
1. ARCH_PRO does not flash in uVision (missing flash algorithm).
1. NUCLEO_F401RE export for uVision is not supported.
1. UBLOX_EVK_ODIN_W2 - The WiFi driver on u-blox ODIN-W2 enables a range of weak cryptographic primitives in mbed TLS to support legacy protocols. This can make the TLS connection vulnerable too, and could be subject to a downgrade attack. It is therefore not recommended to use mbed TLS on this platform for production use.
