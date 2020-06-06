---
title: "Surveying MCU unique ID capabilities"
#categories:
#  - projects
tags:
  - mcu
  - embedded
  - security
---

As part of a work project, I recently took a survey of the embedded unique ID availability in common
MCUs, mostly Cortex-M devices, from different silicon vendors. In this case, I'm specifically
talking about unique IDs that are programmed by the silicon vendor on the tester.

Unique IDs are invaluable for many use cases. Probably the most common use is for network IDs,
such as an Ethernet MAC or wireless node ID. Some devices even name their unique ID(s) with this
purpose in mind. They can also be used for cryptographic protocols for binding to a given
device, as well as other purposes.

The MCUs I've worked on typically had 96- or 128-bit unique IDs, and so I naturally thought that
most MCUs would have similar IDs. It turns out this is incorrect, and the majority of devices
surveyed only have 64-bit IDs. Ideally, devices would have a 128-bit ID that is globally unique.
With a 64-bit ID, you can only be certain of uniqueness within the vendor or device family.

The most common construction of a unique ID that I've seen is closer to a serial number. Part of
the ID is formed from the wafer number and lot, the die coordinates, and possibly other manufacturing
data such as date and fab. If there are remaining bits in the ID, those can be set from either
an incrementing serial number, or a random value.

The NXP i.MX RT1064 is representative of this kind of ID. Its 64-bit ID is composed of these fields:

- LOT_NO_ENC[42:0]: 43-bit lot number
- WAFER_NO[4:0]: 5-bit wafer number
- DIE-Y-COORDINATE[7:0]: 8-bit Y coordinate
- DIE-X-COORDINATE[7:0]: 8-bit X coordinate

However, this form of unique ID is not the only. A few newer devices use crypographic-quality
random numbers for their unique ID. Or, like the NXP LPC55S69, use a UUID that is compliant with
RFC4122.

The point here is that you should be careful with expectations of embedded unique IDs. Depending
on the application, you may need to understand the scope of uniqueness. For instance, don't expect
a 64-bit unique ID to be globally unique. And depending on the construction, it may not even be
unique between device families of the same vendor. Unfortunately, this information is not often
documented in the device's reference manual. Talk to your FAE if you need more information (then
post a comment on the gist below to add to the survey!).

The results of this survey are saved as the gist embedded below. New devices will be added as time
permits. Comments with additions are welcome.

<script src="https://gist.github.com/flit/c44980d20586460bb09b284c891f9ae6.js"></script>


