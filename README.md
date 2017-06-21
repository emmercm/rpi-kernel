# rpi-kernel
A tool to build the Raspberry Pi Foundation kernel on your Raspberry Pi.

## Dependencies
```bash
$ sudo apt-get install wget git make gcc bc
```

## Execution
#### Automatic:
```bash
$ ./rpi-kernel
```

#### Advanced:
```bash
$ ./rpi-kernel [-b <branch>] [-v <expected_kernel_version>] [make targets]
```

#### Advanced Examples:
```bash
$ ./rpi-kernel -b rpi-4.2.y
$ ./rpi-kernel -b rpi-4.3.y -v 4.3.3
$ ./rpi-kernel -b rpi-4.4.y modules
```
