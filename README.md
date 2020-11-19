# rpi-kernel

A tool to build the Raspberry Pi Foundation kernel on your Raspberry Pi.

## Dependencies

Install `wget` plus the kernel [building dependencies](https://www.raspberrypi.org/documentation/linux/kernel/building.md):

```bash
sudo apt-get install wget git bc bison flex libssl-dev make
```

## Execution

### Automatic

```bash
./rpi-kernel
```

### Advanced

```bash
./rpi-kernel [-b <branch>] [-v <expected_kernel_version>] [make targets]
```

### Advanced Examples

```bash
./rpi-kernel -b rpi-5.2.y
```

```bash
./rpi-kernel -b rpi-5.3.y -v 5.3.18
```

```bash
./rpi-kernel -b rpi-5.4.y modules
```
