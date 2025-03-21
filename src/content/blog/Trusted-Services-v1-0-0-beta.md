---
author: shebu-kuriakose
title: Trusted Services v1.0.0-beta and enabling PSA Certified on Cortex-A devices
date: 2022-12-05 10:00:00

image: "../../assets/images/blog/musca_tf_crop_1500x1500.png"
---

# **Trusted Services v1.0.0-beta and enabling PSA Certified on Cortex-A devices**

The Trusted Services project has made the first tagged release [v1.0.0-beta](https://git.trustedfirmware.org/TS/trusted-services.git/tag/?h=v1.0.0-beta). The release includes PSA
Certified Secure Services that can be deployed on Cortex-A devices to meet PSA Certified requirements. The release also includes necessary build and test infrastructure and documentation content.

The project provides a framework for developing and deploying device root-of-trust services for A-
profile devices. The services in the project exists as [Firmware Framework-A](https://developer.arm.com/documentation/den0077/latest) Secure Partitions. The
Secure Partitions are managed by a Secure Partition Manager Core (SPMC) running as part of a Trusted
Operating System (e.g., [OP-TEE](/projects/op-tee/)) or Secure-EL2 Hypervisor (e.g., [Hafnium](/projects/hafnium/)) within a Trusted Execution
Environment.

The release includes PSA Crypto, Storage and Attestation Secure Partitions exposing the PSA Certified
Functional APIs, the same APIs available today on Arm v8-M Cortex-M platforms via Trusted Firmware-
M. Additionally, UEFI SMM services are available through the SMM gateway Secure Partition. The
services within the Secure Partitions can be invoked by applications for secure operations.

OP-TEE in 3.17 and later releases support Secure Partition Manager Core (SPMC). Details can be found
[here](https://optee.readthedocs.io/en/latest/architecture/spmc.html). The diagram below shows Trusted Services deployment on a reference platform.

![TS deployment on reference platform](../../assets/images/TF_TS_Diagram.png)

Visit project [documentation](https://trusted-services.readthedocs.io/en/latest/) to find out more and [subscribe to the mailing list](https://lists.trustedfirmware.org/mailman3/lists/trusted-services.lists.trustedfirmware.org/) to remain updated and get
involved in the project. The TS roadmap can be found [here](https://github.com/Trusted-Services/trusted-services/wiki/Trusted-Services-Roadmap). The project will make further releases as more
features are added and improvements are made to supported features and documentations.
