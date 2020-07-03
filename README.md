## System Information

#### sudo lshw -short

```
H/W path                 Device     Class          Description
==============================================================
                                    system         UX461UA
/0                                  bus            UX461UA
/0/0                                memory         64KiB BIOS
/0/8                                memory         8GiB System Memory
/0/8/0                              memory         4GiB Row of chips LPDDR3 Synchronous Unbuffered (Unregistered) 2133 MHz (0.5 ns)
/0/8/1                              memory         4GiB Row of chips LPDDR3 Synchronous Unbuffered (Unregistered) 2133 MHz (0.5 ns)
/0/d                                memory         256KiB L1 cache
/0/e                                memory         1MiB L2 cache
/0/f                                memory         6MiB L3 cache
/0/10                               processor      Intel(R) Core(TM) i5-8250U CPU @ 1.60GHz
/0/100                              bridge         Xeon E3-1200 v6/7th Gen Core Processor Host Bridge/DRAM Registers
/0/100/2                            display        UHD Graphics 620
/0/100/4                            generic        Xeon E3-1200 v5/E3-1500 v5/6th Gen Core Processor Thermal Subsystem
/0/100/13                           generic        Sunrise Point-LP Integrated Sensor Hub
/0/100/14                           bus            Sunrise Point-LP USB 3.0 xHCI Controller
/0/100/14/0              usb1       bus            xHCI Host Controller
/0/100/14/0/2                       input          USB Receiver
/0/100/14/0/5                       multimedia     USB2.0 HD UVC WebCam
/0/100/14/0/8                       communication  Bluetooth wireless interface
/0/100/14/1              usb2       bus            xHCI Host Controller
/0/100/14.2                         generic        Sunrise Point-LP Thermal subsystem
/0/100/15                           generic        Sunrise Point-LP Serial IO I2C Controller #0
/0/100/15.1                         generic        Sunrise Point-LP Serial IO I2C Controller #1
/0/100/16                           communication  Sunrise Point-LP CSME HECI #1
/0/100/17                           storage        Sunrise Point-LP SATA Controller [AHCI mode]
/0/100/1c                           bridge         Sunrise Point-LP PCI Express Root Port #7
/0/100/1c/0              wlp1s0     network        Wireless 8265 / 8275
/0/100/1e                           generic        Sunrise Point-LP Serial IO UART Controller #0
/0/100/1e.2                         generic        Sunrise Point-LP Serial IO SPI Controller #0
/0/100/1f                           bridge         Intel(R) 100 Series Chipset Family LPC Controller/eSPI Controller - 9D4E
/0/100/1f.2                         memory         Memory controller
/0/100/1f.3                         multimedia     Sunrise Point-LP HD Audio
/0/100/1f.4                         bus            Sunrise Point-LP SMBus
/0/1                     scsi2      storage        
/0/1/0.0.0               /dev/sda   disk           256GB Micron_1100_MTFD

```



#### lspci

```
00:00.0 Host bridge: Intel Corporation Xeon E3-1200 v6/7th Gen Core Processor Host Bridge/DRAM Registers (rev 08)
00:02.0 VGA compatible controller: Intel Corporation UHD Graphics 620 (rev 07)
00:04.0 Signal processing controller: Intel Corporation Xeon E3-1200 v5/E3-1500 v5/6th Gen Core Processor Thermal Subsystem (rev 08)
00:13.0 Non-VGA unclassified device: Intel Corporation Sunrise Point-LP Integrated Sensor Hub (rev 21)
00:14.0 USB controller: Intel Corporation Sunrise Point-LP USB 3.0 xHCI Controller (rev 21)
00:14.2 Signal processing controller: Intel Corporation Sunrise Point-LP Thermal subsystem (rev 21)
00:15.0 Signal processing controller: Intel Corporation Sunrise Point-LP Serial IO I2C Controller #0 (rev 21)
00:15.1 Signal processing controller: Intel Corporation Sunrise Point-LP Serial IO I2C Controller #1 (rev 21)
00:16.0 Communication controller: Intel Corporation Sunrise Point-LP CSME HECI #1 (rev 21)
00:17.0 SATA controller: Intel Corporation Sunrise Point-LP SATA Controller [AHCI mode] (rev 21)
00:1c.0 PCI bridge: Intel Corporation Sunrise Point-LP PCI Express Root Port #7 (rev f1)
00:1e.0 Signal processing controller: Intel Corporation Sunrise Point-LP Serial IO UART Controller #0 (rev 21)
00:1e.2 Signal processing controller: Intel Corporation Sunrise Point-LP Serial IO SPI Controller #0 (rev 21)
00:1f.0 ISA bridge: Intel Corporation Intel(R) 100 Series Chipset Family LPC Controller/eSPI Controller - 9D4E (rev 21)
00:1f.2 Memory controller: Intel Corporation Sunrise Point-LP PMC (rev 21)
00:1f.3 Audio device: Intel Corporation Sunrise Point-LP HD Audio (rev 21)
00:1f.4 SMBus: Intel Corporation Sunrise Point-LP SMBus (rev 21)
01:00.0 Network controller: Intel Corporation Wireless 8265 / 8275 (rev 78)

```



## Current Status

1. 2020-07-03: Basic setup done!
2. Require external wifi adapter or experiment with AppleIntelKext: Currently not complete [1](https://github.com/AppleIntelWifi/adapter)
3. Experimenting with touchpad lag issue: Need to configure GPIO pinning [1](https://github.com/VoodooI2C/VoodooI2C/blob/master/Documentation/GPIO%20Pinning.md) [2](https://voodooi2c.github.io/#GPIO%20Pinning/GPIO%20Pinning) [3](https://www.reddit.com/r/hackintosh/comments/fryffu/partially_successful_hackintosh_asus_zenbook/)