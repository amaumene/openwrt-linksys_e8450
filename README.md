![Build OpenWrt](https://github.com/amaumene/openwrt-linksys_e8450/workflows/Build%20OpenWrt/badge.svg)
# Latest OpenWrt image for [Linksys E8450](https://www.linksys.com/dual-band-ax3200-wifi-6-router/E8450.html)

This GitHub action is to build fresh image of latest OpenWrt snapshot using imagebuilder so I can automatically update my router at home.

What's added compared to snapshot:
* softethervpn-bridge (my ISP throttle everything except TCP 80/443 so I route all my traffic with SoftEther protocol)
* luci
* iperf3
* mtr
* iwinfo
* kmod-tcp-bbr
* libustream-wolfssl
* ca-bundle

What's removed compared to snapshot:
* Everything related to ppp(oe) (luci-proto-ppp, ppp, ppp-mod-pppoe, kmod-pppox, kmod-pppoe, kmod-ppp)

If you want to flash your router with latest image:

```sysupgrade "https://github.com/amaumene/openwrt-linksys_e8450/releases/latest/download/linksys_e8450-ubi-squashfs-sysupgrade.itb"```

/!\ Please note that I might change the packages included without notice. This image is built for my personnal use first.
