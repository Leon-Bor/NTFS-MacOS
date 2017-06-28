# Enable NTFS READ/WRITE MacOS 
Enable writing to NTFS hard drives for free in Mac OS X.

## What we need:

Get and Install Homebrew from [Homebrew Website](https://brew.sh/index_de.html)

## Get it done:

### 1. Install osxfuse and ntfs-3g 

```bash
$ brew cask install osxfuse
```

```bash
$ brew install ntfs-3g
```

### 2. Restart your macbook in recovery mode

Restart your macbook and press `COMMAND + R` to get into the recovery mode.

Open the terminal while in recovery mode and type

```bash
$ csrutil disable
```

### 4. Restart Macbook

After disabling csrutil, reboot your macbook normally. When done open terminal and enter the following commands:

```bash
$ sudo mv /sbin/mount_ntfs /sbin/mount_ntfs.original 
```

```bash
$ sudo ln -s /usr/local/sbin/mount_ntfs /sbin/mount_ntfs
```

### 5. Restart your macbook in recovery mode

Restart your macbook and press `COMMAND + R` to get into the recovery mode.

Open the terminal while in recovery mode and type

```bash
$ csrutil enable
```

### 6. Done

Restart your macbook normally. You should be able to write and read NTFS diks.


Tested with: OSX El Capitan - Version 10.11.4

