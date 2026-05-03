---
layout: post
title: "Getting SteamOS to Boot on PS5: First Steps"
date: 2026-04-24
categories: steamos ps5
---

[this is an ai generated file made for the sole purpose of being an template or a place holder] The PS5 ships with a custom AMD GPU — the Oberon SoC — and while it's locked down at the firmware level, the underlying hardware is close enough to a PC AMD GPU that it's worth trying to get a real Linux stack running on it.

This post documents my first steps toward booting SteamOS on PS5 hardware.

## What We're Working With

The PS5's GPU is based on AMD's RDNA 2 architecture, the same family as the RX 6000 series desktop cards. That means Mesa's RADV driver — the open-source Vulkan driver for AMD — should in theory be able to drive it, once we can get past the bootloader and get a kernel running.

Key components:

- **CPU**: AMD Zen 2, 8 cores / 16 threads
- **GPU**: AMD RDNA 2 (Oberon), ~10.3 TFLOPS
- **RAM**: 16 GB GDDR6 (unified)

## The Bootloader Problem

The first wall you hit is the PS5's secure boot chain. Unlike the PS4, which was cracked open relatively quickly, the PS5 uses a more robust trust chain. Current exploits target specific firmware versions, so staying on an older firmware is step one.

```bash
# Check your PS5 firmware version before updating
# Settings > System > System Software > Version
```

## Getting a Kernel to Run

Once you have exploit access, the goal is to chainload a Linux kernel. The PS5's x86-64 CPU means a standard AMD64 kernel works — the tricky part is the custom hardware initialisation, especially for the GPU and memory controller.

More on that in the next post.

## What's Next

- Getting the GPU recognised by the kernel
- Patching Mesa/RADV for Oberon-specific registers
- Display output over HDMI

Stay tuned.
