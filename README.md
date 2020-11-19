# rpi-kernel

A tool to build the Raspberry Pi Foundation kernel on your Raspberry Pi.

## Dependencies

```bash
sudo apt-get install wget git make gcc bc flex
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
