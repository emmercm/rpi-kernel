# rpi-kernel

A tool to build the Raspberry Pi kernel.

## Dependencies

Install `wget` plus the kernel [building dependencies](https://www.raspberrypi.org/documentation/linux/kernel/building.md):

```bash
sudo apt-get install wget gcc git bc bison flex libssl-dev make
```

## Execution

Usage:

```text
Usage: ./rpi-kernel [OPTIONS] [TARGETS]

Options:
  -a, --arch string        Architecture target (eg: arm)
  -b, --branch string      GitHub branch (eg: rpi-5.4.y)
  -p, --processor string   Processor target (eg: BCM2711)
  -v, --version string     Expected kernel version (eg: 5.4.77)

Architectures:
  arm     RPi 1-4, Zero/W, CM1, CM3, CM4
  arm64   RPi 3-4, CM3, CM4

Processors:
  BCM2835   RPi A, A+, B, B+, Zero/W, CM1
  BCM2836   RPi 2B
  BCM2837   RPi 2B, 3B, 3B+, 3A+, CM3, CM3+
  BCM2711   RPi 4B, CM4

Targets:
  zImage    Kernel image (32-bit)
  Image     Kernel image (64-bit)
  modules   Kernel modules
  dtbs      Device tree blobs
```

Build and install the current version:

```bash
./rpi-kernel
```

### Advanced Examples

Building and installing an expected version from a branch:

```bash
./rpi-kernel -b rpi-5.3.y -v 5.3.18
```

Building and installing only kernel modules from a branch:

```bash
./rpi-kernel -b rpi-5.4.y modules
```

Cross-compiling the current 32-bit Raspberry Pi 3 kernel:

```bash
./rpi-kernel -p BCM2837
```

Cross-compiling the current 64-bit Raspberry Pi 4 kernel:

```bash
./rpi-kernel -a arm64 -p BCM2711
```
