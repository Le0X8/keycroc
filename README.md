# `@Le0X8/keycroc`

Scripts for the Hak5 Key croc

---

## Setting up Node.js

The Key Croc runs on Linux. To use the scripts I have created, you need to install Node.js onto it.

Here is a quick guide on how to do it:

1. Boot the Key Croc into `Arming Mode` (blue status LED) by pressing the hidden button.
2. Access the serial console, under Linux, type `sudo screen /dev/ttyACM0 115200` (you may have to install the `screen` package via apt). For other operating systems, please refer to the [official guide](https://docs.hak5.org/key-croc/basics/serial-console-access).
3. Log in into the Debian shell using the default credentials (user: `root`, password: `hak5croc`). If you already changed these, use your custom credentials instead.
4. Download a recent version of Node.js from the [official website](https://nodejs.org/en/download/prebuilt-binaries). Please download the prebuilt binaries for the ARMv7 CPU architecture, other versions won't work.
5. Copy the binaries into the root directory of the mounted Key Croc drive.
6. Mount the same drive that's connected to your PC to your Key Croc by executing `mkdir /mnt/croc && mount /dev/nandf /mnt/croc && cd /mnt/croc` in the serial shell.
7. Install Node: `tar -xf node-v*-linux-armv7l.tar.xz -C /opt && mv /opt/node-v*-linux-armv7l /opt/node && ln /opt/node/bin/* /usr/bin/`. This unpacks Node to a permanent path in the system and symlinks the binaries.
