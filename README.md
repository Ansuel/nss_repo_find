# NSS Firmware Repo
NSS Firmware bin find in various Online website.

These are used by the ipq806x and upper SoC to initialize and use the UBI32 coprocessor embedded in the CPU.

How to chose the right firmware
-

There are currently 2 type of Coprocessor tied to the SoC

- AK Akronite ( Ipq806x )
- HK Hawkeye/Cypress/Maple (ipq807x", "ipq60xx", "ipq50xx")
---
Every Letter revision is tied to the QSDK. The Firmware are NOT interchangeable with different QSDK. A mismatch between revision and QSDK version results in the coprocessor NOT WORKING (not packet acceleration, not crypto acceleration)

Revision are incremental.

- F -> QSDK6.1
- J -> QSDK10.0
- K -> QSDK11.0
- L -> QSDK11.1
---
The last letter R or E means that the firmware is dedicated to the RETAIL market or the ENTERPRISE market.
Most of the times R contains more feature than E.

---

In short to get the right firmware for ipq8064 based SoC with the code based on QSDK 10.0 we should uw AK for the coprocessor type and J for the revision:
NSS.AK.F.CS-5-E