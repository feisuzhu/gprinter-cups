# Linux CUPS Driver for Gprinter GP-1324D

## Driver Setup Instructions

1. Copy `rastertotspl` to `/usr/lib/cups/filter`
2. Make `rastertotspl` executable and owned by root (`sudo chown root:root rastertotspl && sudo chmod 755 rastertotspl`)
3. Edit `/usr/share/cups/usb/org.cups.usb-quirks` and add the text in this repository's `org.cups.usb-quirks` to the bottom.
4. Plug in the printer with USB.
5. Visit http://localhost:631, click Administration at the top, then click Add Printer.
6. Enter your login username and password if prompted. If it doesn't work, add your user to the `lp` and `lpadmin` groups, reboot, and try again.
7. Select the found printer in the list under Local Printers, fill in printer name and other info.
8. When asked to choose the make and model, use the "Provide a PPD file" option and open `Gprinter.ppd` from this repository.

# 热敏小票打印机 CUPS 驱动（Linux）

在 Gprinter GP1324D 上测试成功

抄袭了 https://tifan.net/blog/2018/03/27/gprinter-thermal-printer-unix-driver/
