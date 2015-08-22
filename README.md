# nokia-n900

App manager -> install rootsh
`sudo gainroot` or `root` in the console will open root shell

The firmware is compressed into a multipart 7z so that I can push it to github.

```
apt-get install libusb-1.0-0-dev
dpkg -i --force-architecture maemo_flasher-3.5_2.5.2.2_i386.deb

flasher-3.5 -F RX-51_2009SE_21.2011.38-1_PR_COMBINED_MR0_ARM.bin -f
```

If there's an unknown lockcode, flash to an older firmware and crack it.

On the n900 (or ssh in)

```
echo root:$(grep -A 13 lock_code /dev/mtd1|tail -1):
```
Save to file on a machine that can run john the ripper.

On PC:

```
john -format:DES -i:digits /path/to/file
```

