# rpi-kernel
A tool to build an official kernel on your Raspberry Pi.

## Dependencies
```
$ apt-get install wget git make gcc bc screen ncurses-dev
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

#### Examples:
```
$ ./rpi-kernel -b rpi-4.2.y
$ ./rpi-kernel -b rpi-4.3.y -v 4.3.3
$ ./rpi-kernel -b rpi-4.4.y modules
```
