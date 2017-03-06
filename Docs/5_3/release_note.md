# mbed OS 5.3 releases

## mbed OS 5.3.6 release
We are pleased to announce the [mbed OS 5.3.6 release](https://github.com/ARMmbed/mbed-os/releases/tag/mbed-os-5.3.6) is now available.

This release includes a number of bug fixes to improve stability. 

### Fixes and Changes

[3590](https://github.com/ARMmbed/mbed-os/pull/3590): [NUC472/M453] Export IAR project and other bugfixes

[3740](https://github.com/ARMmbed/mbed-os/pull/3740): STM32L4 HAL update for RTC Wake Up Timer

[3739](https://github.com/ARMmbed/mbed-os/pull/3739): STM32F7 : remove multiple HSE_VALUE define value

[3759](https://github.com/ARMmbed/mbed-os/pull/3759): STM32: spi_frequency table index fix

[3760](https://github.com/ARMmbed/mbed-os/pull/3760): Fix #3756 for 64 bytes transfers

[3779](https://github.com/ARMmbed/mbed-os/pull/3779): NCS36510: Fix the sporadic semaphore timing issue

[3806](https://github.com/ARMmbed/mbed-os/pull/3806): NXP KL43Z/KL27Z: fix spi format bits check

[3814](https://github.com/ARMmbed/mbed-os/pull/3814): NCS36510: I2C idle delay of 1us

[3803](https://github.com/ARMmbed/mbed-os/pull/3803): Bug fix of initial value of interrupt edge in "gpio_irq_init" again

### Using the release

You can fetch the mbed OS 5.3.6 release from the [mbed-os GitHub](https://github.com/ARMmbed/mbed-os) repository,
using the tag "mbed-os-5.3.6".

Please feel free to ask any questions or provide feedback on this release [on the forum](https://forums.mbed.com/), or to contact us at [support@mbed.org](mailto:support@mbed.org).

## mbed OS 5.3.5 release

We are pleased to announce that the [mbed OS 5.3.5 release](https://github.com/ARMmbed/mbed-os/releases/tag/mbed-os-5.3.5) is now available.

Here is a full list of changes and fixes in this release.

### Fixes and Changes

[3432](https://github.com/ARMmbed/mbed-os/pull/3432): Target STM USBHOST support

[3181](https://github.com/ARMmbed/mbed-os/pull/3181): NUCLEO_F207ZG extending PeripheralPins.c: all available alternate functions can be used now

[3624](https://github.com/ARMmbed/mbed-os/pull/3624): Fix Stack stats by running the test command with "-DMBED_HEAP_STATS_ENABLED=1"

[3626](https://github.com/ARMmbed/mbed-os/pull/3626): NUCLEO_F412ZG : Add USB Device +Host

[3628](https://github.com/ARMmbed/mbed-os/pull/3628): Fix warnings

[3629](https://github.com/ARMmbed/mbed-os/pull/3629): STM32: L0 LL layer

[3632](https://github.com/ARMmbed/mbed-os/pull/3632): IDE Export support for platform VK_RZ_A1H

[3642](https://github.com/ARMmbed/mbed-os/pull/3642): Missing IRQ pin fix for platform VK_RZ_A1H

[3653](https://github.com/ARMmbed/mbed-os/pull/3653): Adding fatal error detection to toolchains

[3661](https://github.com/ARMmbed/mbed-os/pull/3661): [Exporters] Add core to uvision exporter template

[3664](https://github.com/ARMmbed/mbed-os/pull/3664): Fix ncs36510 sleep definitions

[3655](https://github.com/ARMmbed/mbed-os/pull/3655): [STM32F4] Modify folder structure

[3657](https://github.com/ARMmbed/mbed-os/pull/3657): [STM32L4] Modify folder structure

[3658](https://github.com/ARMmbed/mbed-os/pull/3658): [STM32F3] Modify folder structure

[3685](https://github.com/ARMmbed/mbed-os/pull/3685): STM32: I2C: reset state machine

[3689](https://github.com/ARMmbed/mbed-os/pull/3689): Updated to allow for new directory structure for mbed-dev source.

[3718](https://github.com/ARMmbed/mbed-os/pull/3718): Fixing uvisor defines to fix build issues

[3692](https://github.com/ARMmbed/mbed-os/pull/3692): uVisor: Standardize available legacy heap and stack

[3621](https://github.com/ARMmbed/mbed-os/pull/3621): Fix for #2884, LPC824: export to LPCXpresso, target running with wron

[3649](https://github.com/ARMmbed/mbed-os/pull/3649): [STM32F7] Modify folder structure 

[3669](https://github.com/ARMmbed/mbed-os/pull/3669): Adding case insensitive 'error' detection

[3695](https://github.com/ARMmbed/mbed-os/pull/3695): Enforce device_name is valid in targets.json

[3717](https://github.com/ARMmbed/mbed-os/pull/3717): Add IAR export support for NUCLEO_F207ZG

[3723](https://github.com/ARMmbed/mbed-os/pull/3723): NCS36510: spi_format function bug fix

[3727](https://github.com/ARMmbed/mbed-os/pull/3727): Fix access before variable defined bug in test_api

[3708](https://github.com/ARMmbed/mbed-os/pull/3708): [NUC472/M453] Fix USB EP setting error in USBAudio


### Using the release

You can fetch the mbed OS 5.3.5 release from the [mbed-os GitHub](https://github.com/ARMmbed/mbed-os) repository,
using the tag "mbed-os-5.3.5".

Please feel free to ask any questions or provide feedback on this release [on the forum](https://forums.mbed.com/), or to contact us at [support@mbed.org](mailto:support@mbed.org).

## mbed OS 5.3.4 release

We are pleased to announce the [mbed OS 5.3.4 release](https://github.com/ARMmbed/mbed-os/releases/tag/mbed-os-5.3.4) is now available.

This release includes:

* New target support for DISCO_F769NI, DELTA_DFCM_NNN50 and MAX32630FTHR.
* Miscellaneous tool updates and fixes.

### Known Issues

No known issues for this release.

### Ports for Upcoming Targets

[3571](https://github.com/ARMmbed/mbed-os/pull/3571): DISCO_F769NI introduction

[3605](https://github.com/ARMmbed/mbed-os/pull/3605): Add DELTA_DFCM_NNN50 platform

[3640](https://github.com/ARMmbed/mbed-os/pull/3640): [MAX32630FTHR] Adding new platform

### Fixes and Changes

Here is a full list of all changes and fixes in this release.

[3397](https://github.com/ARMmbed/mbed-os/pull/3397): Add uVisor support for the DISCO_F429ZI

[3573](https://github.com/ARMmbed/mbed-os/pull/3573): fix failing RTC initialization for MTS_DRAGONFLY_F411RE

[3575](https://github.com/ARMmbed/mbed-os/pull/3575): Dev stm factorize gpio

[3584](https://github.com/ARMmbed/mbed-os/pull/3584): STM32: make PeripheralPins.h a common file

[3583](https://github.com/ARMmbed/mbed-os/pull/3583): STM32F7 Cube FW new release v1.5.1

[3534](https://github.com/ARMmbed/mbed-os/pull/3534): Turn on debugging by default when exporting. Remove optimizations for IAR and Uvision

[3560](https://github.com/ARMmbed/mbed-os/pull/3560): Refactor scan resources to account for base_paths

[3574](https://github.com/ARMmbed/mbed-os/pull/3574): Fix invalid assert in exporters

[3578](https://github.com/ARMmbed/mbed-os/pull/3578): Target system - Inherit names from target parents

[3586](https://github.com/ARMmbed/mbed-os/pull/3586): Linking to latest

[3587](https://github.com/ARMmbed/mbed-os/pull/3587): Fixing toolchain executable not found error for build.py

[3588](https://github.com/ARMmbed/mbed-os/pull/3588): arm-pack-manager - fix tracebacks

[3594](https://github.com/ARMmbed/mbed-os/pull/3594): Allow user overrides of LINKER_SCRIPT Make variable

[3599](https://github.com/ARMmbed/mbed-os/pull/3599): K22F: Enable TRNG

[3600](https://github.com/ARMmbed/mbed-os/pull/3600): [toolchains] Refactor sys libs

[3603](https://github.com/ARMmbed/mbed-os/pull/3603): Delete testing_mbed_OS_5.md

[3604](https://github.com/ARMmbed/mbed-os/pull/3604): Renaming test_env.cpp in greentea to avoid warning

[3608](https://github.com/ARMmbed/mbed-os/pull/3608): Exporters: make jinja engine strict

[3612](https://github.com/ARMmbed/mbed-os/pull/3612): tests: Fix error on MacOS for udp_dtls_handshake test

[3613](https://github.com/ARMmbed/mbed-os/pull/3613): README: Build info; Docs version updated

[3614](https://github.com/ARMmbed/mbed-os/pull/3614): STM32: make PortNames.h a common file

[3617](https://github.com/ARMmbed/mbed-os/pull/3617): EFM32GG: Fix GCC_ARM linker script

[3618](https://github.com/ARMmbed/mbed-os/pull/3618): STM32: Move types definitions to a common file

[3601](https://github.com/ARMmbed/mbed-os/pull/3601): Clean export dir

[3630](https://github.com/ARMmbed/mbed-os/pull/3630): Delete mbed_targets.md

[3631](https://github.com/ARMmbed/mbed-os/pull/3631): F3 CUBE update V1.7.0

[3635](https://github.com/ARMmbed/mbed-os/pull/3635): STM32 I2C : Fix bug in i2c_byte_read function

[3651](https://github.com/ARMmbed/mbed-os/pull/3651): Max32630 - fix LED4


### Using the release

You can fetch the mbed OS 5.3.4 release from the [mbed-os GitHub](https://github.com/ARMmbed/mbed-os) repository,
using the tag "mbed-os-5.3.4".

Please feel free to ask any questions or provide feedback on this release [on the forum](https://forums.mbed.com/), or to contact us at [support@mbed.org](mailto:support@mbed.org).


## mbed OS 5.3.3 release

We are pleased to announce that the [mbed OS 5.3.3 release](https://github.com/ARMmbed/mbed-os/releases/tag/mbed-os-5.3.3) is now available.

This release includes numerous fixes to code and tools (listed below).

### Known Issues

There are no known issues for this release.

### Fixes and Changes

[3470](https://github.com/ARMmbed/mbed-os/pull/3470): [RZ/A1H]Support RTX v4.80 for Cortex-A and a few Malloc API

[3488](https://github.com/ARMmbed/mbed-os/pull/3488): Dev stm i2c v2 unitary functions

[3492](https://github.com/ARMmbed/mbed-os/pull/3492): Fix #3463 CAN read() return value

[3503](https://github.com/ARMmbed/mbed-os/pull/3503): [LPC15xx] Ensure that PWM=1 is resolved correctly

[3504](https://github.com/ARMmbed/mbed-os/pull/3504): [LPC15xx] CAN implementation improvements

[3513](https://github.com/ARMmbed/mbed-os/pull/3513): NUCLEO_F412ZG - Add platform in RTOS tests + build_travis

[3514](https://github.com/ARMmbed/mbed-os/pull/3514): [NUC472/M453] Remove Tab in USB HAL

[3518](https://github.com/ARMmbed/mbed-os/pull/3518): Preventing app_config from clobbering CLI macros

[3526](https://github.com/ARMmbed/mbed-os/pull/3526): lwip - Fix static IP address issues with IPv4

[3531](https://github.com/ARMmbed/mbed-os/pull/3531): Correctly format include paths for eclipse export

[3537](https://github.com/ARMmbed/mbed-os/pull/3537): Remove default -m and -i options for project.py

[3538](https://github.com/ARMmbed/mbed-os/pull/3538): Remove deprecated clean argument

[3539](https://github.com/ARMmbed/mbed-os/pull/3539): NUCLEO_F412ZG - Add support of TRNG peripheral

[3540](https://github.com/ARMmbed/mbed-os/pull/3540): STM: SPI: Initialize Rx in spi_master_write

[3438](https://github.com/ARMmbed/mbed-os/pull/3438): K64F: Add support for SERIAL ASYNCH API

[3521](https://github.com/ARMmbed/mbed-os/pull/3521): Repair the Emblocks exporer and rename to EmBitz

[3550](https://github.com/ARMmbed/mbed-os/pull/3550): events - Fix overflow of timeout on STM32F4

[3559](https://github.com/ARMmbed/mbed-os/pull/3559): exporters - group by directories in prj root

[3519](https://github.com/ARMmbed/mbed-os/pull/3519): MCUXpresso: Fix ENET driver to enable interrupts after interrupt handler is set

[3528](https://github.com/ARMmbed/mbed-os/pull/3528): Modify update command to directly edit the mbed-os.lib files for each example

[3532](https://github.com/ARMmbed/mbed-os/pull/3532): Eclipse debug fixes (build w/ DEBUG=1 and load symbols)

[3544](https://github.com/ARMmbed/mbed-os/pull/3544): STM32L4 deepsleep improvement

[3546](https://github.com/ARMmbed/mbed-os/pull/3546): NUCLEO-F412ZG - Add CAN peripheral

[3547](https://github.com/ARMmbed/mbed-os/pull/3547): Add support for ethernet-only configuration with Nanostack.

[3551](https://github.com/ARMmbed/mbed-os/pull/3551): Fix I2C driver for RZ/A1H

[3562](https://github.com/ARMmbed/mbed-os/pull/3562): Alphabetize UVision groups

[3558](https://github.com/ARMmbed/mbed-os/pull/3558): K64F UART Asynch API: Fix synchronization issue

[3563](https://github.com/ARMmbed/mbed-os/pull/3563): LPC4088 - Fix vector checksum

[3567](https://github.com/ARMmbed/mbed-os/pull/3567): Dev stm32 F0 v1.7.0

[3577](https://github.com/ARMmbed/mbed-os/pull/3577): Fixes linking errors when building with debug profile

### Using the release

You can fetch the mbed OS 5.3.3 release from the [mbed-os GitHub](https://github.com/ARMmbed/mbed-os) repository,
using the tag "mbed-os-5.3.3".

Please feel free to ask any questions or provide feedback on this release [on the forum](https://forums.mbed.com/), or to contact us at [support@mbed.org](mailto:support@mbed.org).

## mbed OS 5.3.2 release

We are pleased to announce the [mbed OS 5.3.2 release](https://github.com/ARMmbed/mbed-os/releases/tag/mbed-os-5.3.2) is now available.

This release includes:

* New target support for UBLOX_EVK_NINA_B1.
* A rename of the KSDK2 package to MCUXpresso.
* CAN support for the DISCO_F303VC.
* A number of bug fixes and improvements.

Here is a full list of all changes and fixes in this release.

### Ports for Upcoming Targets

[3459](https://github.com/ARMmbed/mbed-os/pull/3459): Target: Add new target UBLOX_EVK_NINA_B1

### Fixes and Changes

[3430](https://github.com/ARMmbed/mbed-os/pull/3430): Fix ci shield eeprom test

[3381](https://github.com/ARMmbed/mbed-os/pull/3381): STM32F1 : map ST HAL assert into MBED assert

[3389](https://github.com/ARMmbed/mbed-os/pull/3389): STM32F2 : map ST HAL assert into MBED assert

[3390](https://github.com/ARMmbed/mbed-os/pull/3390): STM32F3 : map ST HAL assert into MBED assert

[3402](https://github.com/ARMmbed/mbed-os/pull/3402): nsapi - Fixed open/close issue in Socket

[3410](https://github.com/ARMmbed/mbed-os/pull/3410): STM32L4 : map ST HAL assert into MBED assert

[3422](https://github.com/ARMmbed/mbed-os/pull/3422): Enable CAN on DISCO_F303VC

[3428](https://github.com/ARMmbed/mbed-os/pull/3428): Change slave address in I2C master slave asynch test

[3442](https://github.com/ARMmbed/mbed-os/pull/3442): Dev stm i2c f1

[3450](https://github.com/ARMmbed/mbed-os/pull/3450): Correctly filtering examples in test script

[3460](https://github.com/ARMmbed/mbed-os/pull/3460): KSDK I2C: Update the return value to match the API documentation change

[3478](https://github.com/ARMmbed/mbed-os/pull/3478): Delete TESTING.md

[3477](https://github.com/ARMmbed/mbed-os/pull/3477): Delete COMMITTERS.md

[3479](https://github.com/ARMmbed/mbed-os/pull/3479): Delete Toolchain_Profiles.md

[3480](https://github.com/ARMmbed/mbed-os/pull/3480): Delete config_system.md

[3481](https://github.com/ARMmbed/mbed-os/pull/3481): Delete memap.md

[3339](https://github.com/ARMmbed/mbed-os/pull/3339): USB audio callback  rx and tx

[3472](https://github.com/ARMmbed/mbed-os/pull/3472): [RZ/A1H]Fix TTB setting of RO_DATA area

[3439](https://github.com/ARMmbed/mbed-os/pull/3439): Remove unused arguments from detect targets

[3451](https://github.com/ARMmbed/mbed-os/pull/3451): Rename KSDK2 to MCUXpresso. This is the new name of this package

[3469](https://github.com/ARMmbed/mbed-os/pull/3469): Remove invalid thread::start example

[3391](https://github.com/ARMmbed/mbed-os/pull/3391): STM32F4 : map ST HAL assert into MBED assert

[3454](https://github.com/ARMmbed/mbed-os/pull/3454): STM32: Refactor lp_ticker.c + rtc_api.c + sleep.c + rtc_api_hal.h files 

[3457](https://github.com/ARMmbed/mbed-os/pull/3457): [ONME-2844] Supporting non-blocking connect()

[3458](https://github.com/ARMmbed/mbed-os/pull/3458): [ONME-2844] Avoid option level collisions

[3484](https://github.com/ARMmbed/mbed-os/pull/3484): Limiting the thread stack for parallel threads test

[3486](https://github.com/ARMmbed/mbed-os/pull/3486): Move clean functionality out of the export api

[3493](https://github.com/ARMmbed/mbed-os/pull/3493): Delete events.md

[3494](https://github.com/ARMmbed/mbed-os/pull/3494): Delete ignoring_files_from_build.md

[3476](https://github.com/ARMmbed/mbed-os/pull/3476): Removing default toolchain paths

[3489](https://github.com/ARMmbed/mbed-os/pull/3489): NUCLEO_F103RB - Correct CAN and PWM alternate-functions

[3405](https://github.com/ARMmbed/mbed-os/pull/3405): Repair the transmit mailbox (0,1,2) empty interrupt flag not clear BUG

[3473](https://github.com/ARMmbed/mbed-os/pull/3473): Stm32f7 ethernet fix for IAR issue #3387

[3475](https://github.com/ARMmbed/mbed-os/pull/3475): Delete BUILDING.md

[3483](https://github.com/ARMmbed/mbed-os/pull/3483): Improve error message when exporting for make without a linker script

[3490](https://github.com/ARMmbed/mbed-os/pull/3490): Fix deprecated Thread ctor usage in RTOS tests

[3502](https://github.com/ARMmbed/mbed-os/pull/3502): MCUXpresso I2C: Handle 0 byte write

[3500](https://github.com/ARMmbed/mbed-os/pull/3500): Update mbed-client-c version 3.0.4

[3365](https://github.com/ARMmbed/mbed-os/pull/3365): [NUC472/M453] Support USB device


### Using the release

You can fetch the mbed OS 5.3.2 release from the [mbed-os GitHub](https://github.com/ARMmbed/mbed-os) repository,
using the tag "mbed-os-5.3.2".

Please feel free to ask any questions or provide feedback on this release [on the forum](https://forums.mbed.com/), or to contact us at [support@mbed.org](mailto:support@mbed.org).


## mbed OS 5.3.1 release

We are pleased to announce the [mbed OS 5.3.1 release](https://github.com/ARMmbed/mbed-os/releases/tag/mbed-os-5.3.1) is now available.

This release includes target support for FRDM-KW41 and mbed Enabled Maker board with NINA-B1 and EVA-M8Q.
There are also bug fixes and tool fixes. Please see below for a list of the changes.

Here is a full list of all changes and fixes in this release.

### Ports for Upcoming Targets

[3241](https://github.com/ARMmbed/mbed-os/pull/3241): Add support for FRDM-KW41

[3291](https://github.com/ARMmbed/mbed-os/pull/3291): Add mbed Enabled Maker board with NINA-B1 and EVA-M8Q


### Fixes and Changes

[3062](https://github.com/ARMmbed/mbed-os/pull/3062): TARGET_STM :USB device FS 

[3114](https://github.com/ARMmbed/mbed-os/pull/3114): Fix issue with unrecognized uvision file types

[3213](https://github.com/ARMmbed/mbed-os/pull/3213): STM32: Refactor us_ticker.c + hal_tick.c files

[3274](https://github.com/ARMmbed/mbed-os/pull/3274): Pass toolchain path info to subprocesses

[3283](https://github.com/ARMmbed/mbed-os/pull/3283): Remove remaining references to Curl from ARM pack manager

[3288](https://github.com/ARMmbed/mbed-os/pull/3288): Dev spi asynch l0l1

[3289](https://github.com/ARMmbed/mbed-os/pull/3289): Bug fix of initial value of interrupt edge in "gpio_irq_init" function.

[3302](https://github.com/ARMmbed/mbed-os/pull/3302): STM32F4 AnalogIn - Clear VBATE and TSVREFE bits before configuring ADC channels

[3305](https://github.com/ARMmbed/mbed-os/pull/3305): Support building mbed_critical.c with C++ compiler

[3320](https://github.com/ARMmbed/mbed-os/pull/3320): STM32 - Add ADC_VREF label

[3321](https://github.com/ARMmbed/mbed-os/pull/3321): no HSE available by default for NUCLEO_L432KC

[3352](https://github.com/ARMmbed/mbed-os/pull/3352): ublox eva nina - fix line endings

[3322](https://github.com/ARMmbed/mbed-os/pull/3322): DISCO_L053C8 doesn't support LSE

[3345](https://github.com/ARMmbed/mbed-os/pull/3345): STM32 - Remove TIM_IT_UPDATE flag in HAL_Suspend/ResumeTick functions

[3309](https://github.com/ARMmbed/mbed-os/pull/3309): [NUC472/M453] Fix CI failed tests

[3157](https://github.com/ARMmbed/mbed-os/pull/3157): [Silicon Labs] Add support for EFR32MG1 wireless SoC

[3301](https://github.com/ARMmbed/mbed-os/pull/3301): I2C - correct return values for write functions (docs) - part 1

[3303](https://github.com/ARMmbed/mbed-os/pull/3303): Fix #2956 #2939 #2957 #2959 #2960: Add HAL_DeInit function in gpio_irq destructor

[3304](https://github.com/ARMmbed/mbed-os/pull/3304): STM32L476: no HSE is present in NUCLEO and DISCO boards

[3318](https://github.com/ARMmbed/mbed-os/pull/3318): Register map changes for RevG

[3330](https://github.com/ARMmbed/mbed-os/pull/3330): Fix project profile parsing

[3336](https://github.com/ARMmbed/mbed-os/pull/3336): Squashed 'features/FEATURE_LWIP/lwip-interface/lwip/' changes from d7

[3349](https://github.com/ARMmbed/mbed-os/pull/3349): [Exporters] Fix generic ARM CPU target in uvision

[3350](https://github.com/ARMmbed/mbed-os/pull/3350): [Exporter docs] index.json update instructions

[3317](https://github.com/ARMmbed/mbed-os/pull/3317): NUCLEO_F429ZI has integrated LSE

[3312](https://github.com/ARMmbed/mbed-os/pull/3312): K64F: SPI Asynch API implementation

[3324](https://github.com/ARMmbed/mbed-os/pull/3324): Dev i2c common code

[3331](https://github.com/ARMmbed/mbed-os/pull/3331): Enabled example export building for more examples

[3347](https://github.com/ARMmbed/mbed-os/pull/3347): USB_4 : test OK with IAR ,GCC_ARM(limitation to ARM not needed)

[3355](https://github.com/ARMmbed/mbed-os/pull/3355): IAR export will not fail in the absence of a CMSIS pack

[3362](https://github.com/ARMmbed/mbed-os/pull/3362): Increase stack size in malloc test for Cortex-A

[3369](https://github.com/ARMmbed/mbed-os/pull/3369): Add CAN2 missing pins for connector CN12

[3377](https://github.com/ARMmbed/mbed-os/pull/3377): STM32 NUCLEO-L152RE Update system core clock to 32MHz

[3378](https://github.com/ARMmbed/mbed-os/pull/3378): K66F: Enable LWIP feature

[3382](https://github.com/ARMmbed/mbed-os/pull/3382): [MAX32620] Fix serial readable function.

[3399](https://github.com/ARMmbed/mbed-os/pull/3399): NUCLEO_F103RB - Add SERIAL_FC feature

[3409](https://github.com/ARMmbed/mbed-os/pull/3409): STM32L1 : map ST HAL assert into MBED assert

[3416](https://github.com/ARMmbed/mbed-os/pull/3416): Rename i2c_api.c for STM32F1 targets to fix IAR exporter

[3368](https://github.com/ARMmbed/mbed-os/pull/3368): CFSTORE fixes for building with DEBUG trace enabled

[3348](https://github.com/ARMmbed/mbed-os/pull/3348): Fix frequency function of CAN driver.

[3366](https://github.com/ARMmbed/mbed-os/pull/3366): NUCLEO_F412ZG - Add new platform

[3379](https://github.com/ARMmbed/mbed-os/pull/3379): STM32F0 : map ST HAL assert into MBED assert

[3385](https://github.com/ARMmbed/mbed-os/pull/3385): Remove deprecated flags args

[3393](https://github.com/ARMmbed/mbed-os/pull/3393): ISR register never re-evaluated in HAL_DMA_PollForTransfer for STM32F4

[3408](https://github.com/ARMmbed/mbed-os/pull/3408): STM32F7 : map ST HAL assert into MBED assert

[3411](https://github.com/ARMmbed/mbed-os/pull/3411): STM32L0 : map ST HAL assert into MBED assert

[3413](https://github.com/ARMmbed/mbed-os/pull/3413): Deduplicate IAR exporter templates and enable a few more targets

[3414](https://github.com/ARMmbed/mbed-os/pull/3414): Remove unnecessary absolute paths from IAR and ARM compilers

[3415](https://github.com/ARMmbed/mbed-os/pull/3415): [make exporters] Add quotes to echo statements

[3424](https://github.com/ARMmbed/mbed-os/pull/3424): STM32F4 - FIX to add the update of hdma->State variable

[3427](https://github.com/ARMmbed/mbed-os/pull/3427): Fix stm i2c slave

[3429](https://github.com/ARMmbed/mbed-os/pull/3429): Fix stm i2c fix init

[3434](https://github.com/ARMmbed/mbed-os/pull/3434): [NUC472/M453] Fix stuck in lp_ticker_init and other updates

[3436](https://github.com/ARMmbed/mbed-os/pull/3436): Fix network echo test host scripts for Mac


### Using the release

You can fetch the mbed OS 5.3.1 release from the [mbed-os GitHub](https://github.com/ARMmbed/mbed-os) repository,
using the tag "mbed-os-5.3.1".
Please feel free to ask any questions or provide feedback on this release [on the forum](https://forums.mbed.com/) or to contact us at [support@mbed.org](mailto:support@mbed.org).

## mbed OS 5.3.0 release 

This is the release note for mbed OS 5.3.0, summarizing the major enhancements in this version. 
You can find the mbed OS 5.3.0 release on GitHub. 

### About this release 
This release makes available early versions of key new features we are working on in development branches, alongside many enhancements and bug fixes to our stable release codeline. These new features will be of particular interest to partners and developers who would like to observe and contribute to their development ahead of them being made generally available. 

The new feature developments made available are: 

- Initial [CMSIS5 and CMSIS-RTOS2](https://github.com/ARMmbed/mbed-os/tree/feature_cmsis5/rtos) upgrade
- Integration points for [Hardware Acceleration of Symmetric and Asymmetric Encryption](https://github.com/ARMmbed/mbed-os/tree/feature_hw_crypto/features/mbedtls)
- Introduction of native [LoRaWAN APIs](https://github.com/ARMmbed/mbed-os/tree/feature-lorawan/features/FEATURE_LORAWAN) 

You can follow our development of these features - and contribute to them - by working with the feature branches linked above. 

In addition, the main mbed OS 5.3 release includes a number of fixes since 5.2 and now supports 70 target platforms. 

The following sections provide more details of these and other changes in this release. 

### Core 
A first functional integration of the next generation CMSIS5 libraries, including the new CMSIS-RTOS2 RTOS kernel. This upgrade is integrated under the mbed OS Peripheral and RTOS APIs such that it will have little or no impact on developers, but provides important enhancements that can be taken advantage of internally. 

These enhancements include: 

- Primitives and integration points for supporting TrustZone for Cortex-M and mbed uVisor 
- Improved RTOS kernel 
- Support for ARM Compiler 6 
- Many patches and modifications that mbed OS had made to CMSIS4 and CMSIS-RTOS now incorporated directly in to the CMSIS5 and CMSIS-RTOS2 codebases 

This allows tracking of the latest CMSIS5 development, and will be brought in to the mainline release when it is ready. Impact on end developers when this happens should be very limited, but open up further opportunities for mbed OS functionality and portability.  

### Security 
Building on the Hardware Entropy work in mbed OS 5.2, mbed OS 5.3 adds the integration points for implementing Hardware Acceleration on different target platforms. This support extends to both Symmetric and Asymmetric encryption operations, and when implemented for a target will transparently provide benefit for developers directly or indirectly using functions that rely on TLS/DTLS or other Cryptographic operations. 

Partners looking to provide implementations for their targets should contact their ARM Partner Enablement representative for guidance, such that support can be made available for developers using their platforms in future mbed OS releases.      

### Connectivity 
New LoRaWAN APIs are introduced to provide native development support for LoRaWAN applications on any mbed Enabled LoRa hardware. These APIs are available for partners and developers to analyze and help refine whilst the full mbed OS LoRaWAN stack is integrated, ahead of making it available as part of our mainline release. In particular, please contact us if you have an interest in LoRa and LoraWAN as a module manufacturer, OEM product developer or network provider.  

Wi-Fi support has also been further improved, with built in support for both the u-blox ODIN-W2 and Espressif ESP8266 modules. Look out for further partner support, which will become available in patch releases. 

### Targets 
Thanks to our partners’ hard work, mbed OS 5.3 supports 70 [targets platforms](https://developer.mbed.org/platforms/). 

We will continue to add new targets in our bi-weekly releases as partners introduce support.  

### Fixes and Changes 
Please see the mbed-os GitHub repository referenced below for a full list of changes introduced in this release. 

We have compiled a [list of known issues](https://github.com/ARMmbed/mbed_os_release_notes/blob/master/Docs/5_3/known_issues.md).

### Using the release 
You can fetch the mbed OS 5.3.0 release from the [mbed-os GitHub](https://github.com/ARMmbed/mbed-os) repository, using the tag “mbed-os-5.3.0”. 

Please feel free to ask any questions or provide feedback on this release on the forum, or to contact us at [support@mbed.org](mailto:support@mbed.org).
 
