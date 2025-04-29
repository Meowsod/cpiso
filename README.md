# cpiso
These bash scripts are for copying an ISO with md5 checking and log writing from a block device, only requiring linux coreutils.

# Installation

```bash
$ git clone git@github.com/Meowsod/cpiso.git
$ cd cpiso
```

```bash
$ sudo mkdir -p /usr/local/bin/
$ chmod +x src/*
$ sudo ln -s "$(pwd)/src/"* /usr/local/bin/
```

# Explanations

The `cpiso` script is a frontend using and writing logs of `cpiso_base` and ejecting the drive.
`cpiso_check` is for checking the quality of an existing log file.

## Copying a disc

```bash
$ cpiso /dev/sr0 output/path
```

or

```bash
$ export DRIVE="/dev/sr0"; export DIRECTORY="output/path"
$ cpiso
```

## Without frontend

```bash
$ cpiso_base /dev/sr0
```

## Checking logs

```bash
$ cpiso_check LABEL
```

# Future

Adding sha256 checks to the logs could be easily implemented.

