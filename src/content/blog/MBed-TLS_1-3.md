---
author: shebu-kuriakose
title: Trusted Firmware MBed TLS - TLS 1.3, PSA Crypto APIs, and New LTS
date: 2021-12-17 10:00:00

image: "../../assets/images/blog/musca_tf_crop_1500x1500.png"
---

## Introduction

Mbed TLS project had done a major release, Mbed TLS 3.0 in July this year. The project has made Mbed
TLS 3.1.0, Mbed TLS 2.28.0 Long Term Support (LTS) and Mbed TLS 2.16.12 LTS releases this week.

Mbed TLS 3.1 has several changes since the 3.0 release. Refer to the [change log](https://github.com/ARMmbed/mbedtls/blob/v3.1.0/ChangeLog) for a complete list of
changes in the release. The project has achieved 2 major milestones as part of this release.

## Highlights

1. **TLS 1.3 minimum viable implementation:** TLS 1.0 and TLS 1.1 were formally deprecated by IETF in March 2021. TLS 1.2 continues to be supported in Mbed TLS. Many products under design are looking to support TLS1.3. This made it very important for Mbed TLS to start supporting TLS1.3.

   As a starting point an initial set of TLS 1.3 features have been upstreamed and made available in Mbed TLS 3.1 release. The TLS 1.3 features present in the release can be found [here](https://github.com/ARMmbed/mbedtls/pull/4963). Further work for complete support of TLS 1.3 will continue in the coming months.

2. **PSA Cryptography API v1.0 compliant:** [PSA Crypto APIs](https://developer.arm.com/documentation/ihi0086/latest/) provide user-friendly interfaces for cryptographic services including crypto primitives and key storage functionality. It is an important component of the PSA Certified framework providing portable interfaces to cryptographic operations on a wider variety of hardware.

   Mbed TLS project had started supporting a subset of PSA Crypto v1.0 APIs in last several releases. Mbed TLS 3.1 includes implementation of all essential PSA Crypto v1.0 APIs passing the PSA Crypto API compliance [test suite](https://github.com/ARM-software/psa-arch-tests). This makes it possible for various usecases to use the PSA Crypto APIs implementation in Mbed TLS for cryptographic operations.

3. **Mbed TLS 2.28.0 Long Term Support (LTS) release:** As the 3 year support period of Mbed TLS 2.16 LTS comes to an end, the project has created a new LTS release. This release is expected to be supported for next 3 years till end of 2024.

   During this period, only security and bug fixes will be integrated. We will maintain the API (Application Programming Interface) to be source code compatible, and maintain the ABI (Application Binary Interface), to ensure that users of the library can make the minimum of changes to their own software to ensure against regressions being introduced into their application software.

   No new features will be introduced, and the API will not be changed or extended, unless required by significant security issues or issues of interoperability with other vendors TLS stacks.

   New features and enhancements will continue to be done in the development branch and will be part of the future releases from the development branch like Mbed TLS 3.1 made this week.

4. **Mbed TLS 2.16.12 Long Term Support (LTS) release:** This is the final release of Mbed TLS 2.16, which concludes its support period at the end of 2021. Users requiring a long-term-support release are recommended to pick up Mbed TLS 2.28.0.

## What’s Next?

Remaining features for supporting TLS 1.3 and TLS using PSA Crypto for all cryptographic operation will be focus areas in early 2022. We welcome community participation in ongoing and future work items in the project that can be found [here](https://github.com/orgs/ARMmbed/projects/18). [Subscribe to the mailing list](https://lists.trustedfirmware.org/mailman3/lists/mbed-tls.lists.trustedfirmware.org/) to start participating in the design and development of the project. The bi-weekly [Mbed TLS Technical Forums](/meetings/mbed-tls-technical-forum/) are also an opportunity to understand major developments in the project.
