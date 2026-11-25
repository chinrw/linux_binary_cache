# linux_binary_cache

## Overview

This repository publishes single-file Linux kernel images (`vmlinuz`) for Asterinas benchmarks and Linux regression baselines. It does not ship `/lib/modules`, so options configured as loadable modules (`=m`) are unavailable at runtime unless built in (`=y`).

`6.16.0/vmlinuz` is built from upstream Linux 6.16.0 (`linux-6.16.tar.xz`) with TDX host/guest support, Ext2, and built-in `virtio-fs` for benchmarks. It also builds in exFAT, Ext2 xattr/ACL/security, OverlayFS, Yama LSM, `vsock` (`virtio-vsock` and loopback), and Bochs/VirtIO-GPU DRM with fbdev emulation for single-VM Linux regression testing. Its full kernel configuration is stored in `6.16.0/.config`.
