# rpi-kernel
A tool to build the Raspberry Pi Foundation kernel on your Raspberry Pi.

## Dependencies
```
$ sudo apt-get install wget git make gcc bc
```

## Execution
#### Automatic:
```
$ ./rpi-kernel
```

#### Advanced:
```
$ ./rpi-kernel [-b <branch>] [-v <expected_kernel_version>] [make targets]
```

#### Advanced Examples:
```
$ ./rpi-kernel -b rpi-4.2.y
$ ./rpi-kernel -b rpi-4.3.y -v 4.3.3
$ ./rpi-kernel -b rpi-4.4.y modules
```
