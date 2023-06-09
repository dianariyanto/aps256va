# APS256VA Firmware
Full dump APS256VA original firmware based on OpenWrt 14.07 a.k.a Barrier Breaker
## Thread
https://forum.openwrt.org/t/aps-256va-help-for-identification/143653
## Bootlog
```
*********************************************
*   U-Boot 1.1.4  (May 22 2015, 15:41:49)   *
*********************************************

LONGDATA U-Boot for LONGDATA APS256

DRAM:   128 MB DDR2 32-bit
FLASH:  Winbond W25Q128 (16 MB)
CLOCKS: 560/450/225/28 MHz (CPU/RAM/AHB/SPI)

LED on during eth initialization...

Hit any key to stop autobooting:  0

Booting image at: 0x9F020000

   Image name:   MIPS OpenWrt Linux-3.10.49
   Created:      2015-04-01   1:49:23 UTC
   Image type:   MIPS Linux Kernel Image (lzma compressed)
   Data size:    1218057 Bytes = 1.2 MB
   Load address: 0x80060000
   Entry point:  0x80060000

Uncompressing kernel image... OK!
Starting kernel...

[    0.000000] Linux version 3.10.49 (longdata@build) (gcc version 4.8.3 (OpenWrt/Linaro GCC 4.8-2014.04 unknown) ) #3 Wed Apr 1 09:49:07 CST 2015
[    0.000000] bootconsole [early0] enabled
[    0.000000] CPU revision is: 0001974c (MIPS 74Kc)
[    0.000000] SoC: Atheros AR9344 rev 2
[    0.000000] Clocks: CPU:560.000MHz, DDR:450.000MHz, AHB:225.000MHz, Ref:40.000MHz
[    0.000000] Determined physical RAM map:
[    0.000000]  memory: 08000000 @ 00000000 (usable)
[    0.000000] Initrd not found or empty - disabling initrd
[    0.000000] Zone ranges:
[    0.000000]   Normal   [mem 0x00000000-0x07ffffff]
[    0.000000] Movable zone start for each node
[    0.000000] Early memory node ranges
[    0.000000]   node   0: [mem 0x00000000-0x07ffffff]
[    0.000000] Primary instruction cache 64kB, VIPT, 4-way, linesize 32 bytes.
[    0.000000] Primary data cache 32kB, 4-way, VIPT, cache aliases, linesize 32 bytes
[    0.000000] Built 1 zonelists in Zone order, mobility grouping on.  Total pages: 32512
[    0.000000] Kernel command line:  board=APS256 console=ttyS0,115200 mtdparts=spi0.0:128k(u-boot),1408k(kernel),14784k(rootfs),64k(art),16192k@0x20000(firmware) rootfstype=squashfs,jffs2 noinitrd
[    0.000000] PID hash table entries: 512 (order: -1, 2048 bytes)
[    0.000000] Dentry cache hash table entries: 16384 (order: 4, 65536 bytes)
[    0.000000] Inode-cache hash table entries: 8192 (order: 3, 32768 bytes)
[    0.000000] Writing ErrCtl register=00000000
[    0.000000] Readback ErrCtl register=00000000
[    0.000000] Memory: 125736k/131072k available (2641k kernel code, 5336k reserved, 666k data, 272k init, 0k highmem)
[    0.000000] SLUB: HWalign=32, Order=0-3, MinObjects=0, CPUs=1, Nodes=1
[    0.000000] NR_IRQS:51
[    0.000000] Calibrating delay loop... 278.93 BogoMIPS (lpj=1394688)
[    0.070000] pid_max: default: 32768 minimum: 301
[    0.070000] Mount-cache hash table entries: 512
[    0.080000] NET: Registered protocol family 16
[    0.080000] MIPS: machine is LONGDATA APS256
[    0.490000] ar724x-pci ar724x-pci: PCIe link is down
[    0.490000] registering PCI controller with io_map_base unset
[    0.510000] bio: create slab <bio-0> at 0
[    0.510000] PCI host bridge to bus 0000:00
[    0.520000] pci_bus 0000:00: root bus resource [mem 0x10000000-0x13ffffff]
[    0.520000] pci_bus 0000:00: root bus resource [io  0x0000]
[    0.530000] pci_bus 0000:00: No busn resource found for root bus, will use [bus 00-ff]
[    0.530000] Switching to clocksource MIPS
[    0.540000] NET: Registered protocol family 2
[    0.540000] TCP established hash table entries: 1024 (order: 1, 8192 bytes)
[    0.550000] TCP bind hash table entries: 1024 (order: 0, 4096 bytes)
[    0.560000] TCP: Hash tables configured (established 1024 bind 1024)
[    0.560000] TCP: reno registered
[    0.570000] UDP hash table entries: 256 (order: 0, 4096 bytes)
[    0.570000] UDP-Lite hash table entries: 256 (order: 0, 4096 bytes)
[    0.580000] NET: Registered protocol family 1
[    0.600000] squashfs: version 4.0 (2009/01/31) Phillip Lougher
[    0.610000] jffs2: version 2.2 (NAND) (SUMMARY) (LZMA) (RTIME) (CMODE_PRIORITY) (c) 2001-2006 Red Hat, Inc.
[    0.620000] msgmni has been set to 245
[    0.620000] io scheduler noop registered
[    0.630000] io scheduler deadline registered (default)
[    0.630000] Serial: 8250/16550 driver, 1 ports, IRQ sharing disabled
[    0.660000] serial8250.0: ttyS0 at MMIO 0x18020000 (irq = 11) is a 16550A
[    0.670000] console [ttyS0] enabled, bootconsole disabled
[    0.670000] console [ttyS0] enabled, bootconsole disabled
[    0.680000] ath79-spi ath79-spi: master is unqueued, this is deprecated
[    0.690000] m25p80 spi0.0: found w25q128, expected m25p80
[    0.690000] m25p80 spi0.0: w25q128 (16384 Kbytes)
[    0.700000] 5 cmdlinepart partitions found on MTD device spi0.0
[    0.700000] Creating 5 MTD partitions on "spi0.0":
[    0.710000] 0x000000000000-0x000000020000 : "u-boot"
[    0.710000] 0x000000020000-0x000000180000 : "kernel"
[    0.720000] 0x000000180000-0x000000ff0000 : "rootfs"
[    0.730000] mtd: device 2 (rootfs) set to be root filesystem
[    0.730000] 1 squashfs-split partitions found on MTD device rootfs
[    0.740000] 0x000000740000-0x000000ff0000 : "rootfs_data"
[    0.750000] 0x000000ff0000-0x000001000000 : "art"
[    0.750000] 0x000000020000-0x000000ff0000 : "firmware"
[    0.770000] libphy: ag71xx_mdio: probed
[    1.330000] ag71xx ag71xx.0: connected to PHY at ag71xx-mdio.1:04 [uid=004dd042, driver=Generic PHY]
[    1.340000] eth0: Atheros AG71xx at 0xb9000000, irq 4, mode:MII
[    1.900000] ag71xx-mdio.1: Found an AR934X built-in switch
[    2.930000] eth1: Atheros AG71xx at 0xba000000, irq 5, mode:GMII
[    2.940000] TCP: cubic registered
[    2.940000] NET: Registered protocol family 17
[    2.940000] 8021q: 802.1Q VLAN Support v1.8
[    2.950000] VFS: Mounted root (squashfs filesystem) readonly on device 31:2.
[    2.960000] Freeing unused kernel memory: 272K (8039c000 - 803e0000)
procd: Console is alive
procd: - watchdog -
[    5.400000] usbcore: registered new interface driver usbfs
[    5.410000] usbcore: registered new interface driver hub
[    5.420000] usbcore: registered new device driver usb
[    5.430000] SCSI subsystem initialized
[    5.440000] ehci_hcd: USB 2.0 'Enhanced' Host Controller (EHCI) Driver
[    5.450000] ehci-platform: EHCI generic platform driver
[    5.450000] ehci-platform ehci-platform: EHCI Host Controller
[    5.460000] ehci-platform ehci-platform: new USB bus registered, assigned bus number 1
[    5.470000] ehci-platform ehci-platform: irq 3, io mem 0x1b000000
[    5.500000] ehci-platform ehci-platform: USB 2.0 started, EHCI 1.00
[    5.500000] hub 1-0:1.0: USB hub found
[    5.510000] hub 1-0:1.0: 1 port detected
[    5.510000] ohci_hcd: USB 1.1 'Open' Host Controller (OHCI) Driver
[    5.520000] uhci_hcd: USB Universal Host Controller Interface driver
[    5.530000] usbcore: registered new interface driver usb-storage
procd: - preinit -
[    5.940000] usb 1-1: new high-speed USB device number 2 using ehci-platform
Press the [f] key and hit [enter] to enter failsafe mode
Press the [1], [2], [3] or [4] key and hit [enter] to select the debug level
[    6.140000] hub 1-1:1.0: USB hub found
[    6.140000] hub 1-1:1.0: 4 ports detected
[    6.430000] usb 1-1.1: new high-speed USB device number 3 using ehci-platform
[    6.540000] usb-storage 1-1.1:1.6: USB Mass Storage device detected
[    6.550000] scsi0 : usb-storage 1-1.1:1.6
[    7.550000] scsi 0:0:0:0: Direct-Access     MEDIATEK  FLASH DISK      6225 PQ: 0 ANSI: 0 CCS
[    7.560000] scsi 0:0:0:1: Direct-Access     MEDIATEK  FLASH DISK      6225 PQ: 0 ANSI: 0 CCS
[    7.570000] sd 0:0:0:0: [sda] Attached SCSI removable disk
[    7.580000] sd 0:0:0:1: [sdb] 65536 512-byte logical blocks: (33.5 MB/32.0 MiB)
[    7.580000] sd 0:0:0:1: [sdb] Write Protect is off
[    7.590000] sd 0:0:0:1: [sdb] No Caching mode page found
[    7.600000] sd 0:0:0:1: [sdb] Assuming drive cache: write through
[    7.600000] sd 0:0:0:1: [sdb] No Caching mode page found
[    7.610000] sd 0:0:0:1: [sdb] Assuming drive cache: write through
[    7.620000]  sdb:
[    7.620000] sd 0:0:0:1: [sdb] No Caching mode page found
[    7.630000] sd 0:0:0:1: [sdb] Assuming drive cache: write through
[    7.630000] sd 0:0:0:1: [sdb] Attached SCSI removable disk
[    8.390000] eth0: link up (100Mbps/Full duplex)
jffs2 is ready
jffs2 is ready
[    9.340000] jffs2: notice: (356) jffs2_build_xattr_subsystem: complete building xattr subsystem, 1 of xdatum (1 unchecked, 0 orphan) and 37 of xref (0 dead, 19 orphan) found.
switching to overlay
[    9.380000] eth0: link down
procd: - early -
procd: - watchdog -
Failed to connect to ubus
procd: - ubus -
procd: - init -
Please press Enter to activate this console.
[   11.870000] NET: Registered protocol family 10
[   11.890000] gre: GRE over IPv4 demultiplexor driver
[   11.900000] ip_gre: GRE over IPv4 tunneling driver
[   11.910000] nf_conntrack version 0.5.0 (1968 buckets, 7872 max)
[   11.930000] ip6_tables: (C) 2000-2006 Netfilter Core Team
[   11.980000] usbcore: registered new interface driver cdc_acm
[   11.980000] cdc_acm: USB Abstract Control Model driver for USB modems and ISDN adapters
[   12.000000] Loading modules backported from Linux version master-2014-05-22-0-gf2032ea
[   12.000000] Backport generated by backports.git backports-20140320-37-g5c33da0
[   12.020000] ip_tables: (C) 2000-2006 Netfilter Core Team
[   12.060000] usbcore: registered new interface driver ums-alauda
[   12.080000] usbcore: registered new interface driver ums-cypress
[   12.080000] usbcore: registered new interface driver ums-datafab
[   12.100000] usbcore: registered new interface driver ums-freecom
[   12.110000] usbcore: registered new interface driver ums-isd200
[   12.110000] usbcore: registered new interface driver ums-jumpshot
[   12.130000] usbcore: registered new interface driver ums-karma
[   12.130000] usbcore: registered new interface driver ums-sddr09
[   12.160000] usbcore: registered new interface driver ums-sddr55
[   12.180000] usbcore: registered new interface driver ums-usbat
[   12.200000] usbcore: registered new interface driver usbserial
[   12.210000] usbcore: registered new interface driver usbserial_generic
[   12.220000] usbserial: USB Serial support registered for generic
[   12.260000] xt_time: kernel timezone is -0000
[   12.290000] cfg80211: Calling CRDA to update world regulatory domain
[   12.290000] cfg80211: World regulatory domain updated:
[   12.300000] cfg80211:  DFS Master region: unset
[   12.300000] cfg80211:   (start_freq - end_freq @ bandwidth), (max_antenna_gain, max_eirp), (dfs_cac_time)
[   12.310000] cfg80211:   (2402000 KHz - 2472000 KHz @ 40000 KHz), (N/A, 2000 mBm), (N/A)
[   12.320000] cfg80211:   (2457000 KHz - 2482000 KHz @ 40000 KHz), (N/A, 2000 mBm), (N/A)
[   12.330000] cfg80211:   (2474000 KHz - 2494000 KHz @ 20000 KHz), (N/A, 2000 mBm), (N/A)
[   12.340000] cfg80211:   (5170000 KHz - 5250000 KHz @ 160000 KHz), (N/A, 2000 mBm), (N/A)
[   12.340000] cfg80211:   (5250000 KHz - 5330000 KHz @ 160000 KHz), (N/A, 2000 mBm), (0 s)
[   12.350000] cfg80211:   (5490000 KHz - 5730000 KHz @ 160000 KHz), (N/A, 2000 mBm), (0 s)
[   12.360000] cfg80211:   (5735000 KHz - 5835000 KHz @ 80000 KHz), (N/A, 2000 mBm), (N/A)
[   12.370000] cfg80211:   (57240000 KHz - 63720000 KHz @ 2160000 KHz), (N/A, 0 mBm), (N/A)
[   12.440000] PPP generic driver version 2.4.2
[   12.450000] PPP MPPE Compression module registered
[   12.460000] NET: Registered protocol family 24
[   12.460000] PPTP driver version 0.8.5
[   12.500000] usbcore: registered new interface driver option
[   12.510000] usbserial: USB Serial support registered for GSM modem (1-port)
[   12.510000] option 1-1.1:1.0: GSM modem (1-port) converter detected
[   12.530000] option 1-1.1:1.1: GSM modem (1-port) converter detected
[   12.530000] option 1-1.1:1.2: GSM modem (1-port) converter detected
[   12.540000] usb 1-1.1: GSM modem (1-port) converter now attached to ttyUSB2
[   12.550000] option 1-1.1:1.3: GSM modem (1-port) converter detected
[   12.560000] usb 1-1.1: GSM modem (1-port) converter now attached to ttyUSB3
[   12.560000] option 1-1.1:1.4: GSM modem (1-port) converter detected
[   12.570000] usb 1-1.1: GSM modem (1-port) converter now attached to ttyUSB4
[   12.580000] option 1-1.1:1.5: GSM modem (1-port) converter detected
[   12.600000] usb 1-1.1: GSM modem (1-port) converter now attached to ttyUSB5
[   12.660000] cfg80211: Calling CRDA for country: US
[   12.670000] cfg80211: Regulatory domain changed to country: US
[   12.670000] cfg80211:  DFS Master region: FCC
[   12.680000] cfg80211:   (start_freq - end_freq @ bandwidth), (max_antenna_gain, max_eirp), (dfs_cac_time)
[   12.690000] cfg80211:   (2402000 KHz - 2472000 KHz @ 40000 KHz), (N/A, 3000 mBm), (N/A)
[   12.690000] cfg80211:   (5170000 KHz - 5250000 KHz @ 80000 KHz), (N/A, 1700 mBm), (N/A)
[   12.700000] cfg80211:   (5250000 KHz - 5330000 KHz @ 80000 KHz), (N/A, 2300 mBm), (0 s)
[   12.710000] cfg80211:   (5735000 KHz - 5835000 KHz @ 80000 KHz), (N/A, 3000 mBm), (N/A)
[   12.720000] cfg80211:   (57240000 KHz - 63720000 KHz @ 2160000 KHz), (N/A, 4000 mBm), (N/A)
[   12.730000] ieee80211 phy0: Atheros AR9340 Rev:0 mem=0xb8100000, irq=47
[   22.580000] IPv6: ADDRCONF(NETDEV_UP): eth1: link is not ready
[   22.580000] device eth1 entered promiscuous mode
[   22.590000] IPv6: ADDRCONF(NETDEV_UP): br-lan: link is not ready
[   22.600000] IPv6: ADDRCONF(NETDEV_UP): eth0: link is not ready
[   22.640000] IPv6: ADDRCONF(NETDEV_UP): br-ra: link is not ready
[   23.590000] eth0: link up (100Mbps/Full duplex)
[   23.590000] IPv6: ADDRCONF(NETDEV_CHANGE): eth0: link becomes ready
[   23.740000] eth1: link up (1000Mbps/Full duplex)
[   23.740000] br-lan: port 1(eth1) entered forwarding state
[   23.750000] br-lan: port 1(eth1) entered forwarding state
[   23.750000] IPv6: ADDRCONF(NETDEV_CHANGE): eth1: link becomes ready
[   23.790000] IPv6: ADDRCONF(NETDEV_CHANGE): br-lan: link becomes ready
[   24.550000] IPv6: ADDRCONF(NETDEV_UP): wlan0: link is not ready
[   24.710000] device wlan0 entered promiscuous mode
[   25.050000] br-ra: port 1(wlan0) entered forwarding state
[   25.050000] br-ra: port 1(wlan0) entered forwarding state
[   25.060000] IPv6: ADDRCONF(NETDEV_CHANGE): wlan0: link becomes ready
[   25.100000] IPv6: ADDRCONF(NETDEV_CHANGE): br-ra: link becomes ready
[   25.750000] br-lan: port 1(eth1) entered forwarding state
[   27.050000] br-ra: port 1(wlan0) entered forwarding state
procd: - init complete -
```
