# openvpn-for-router
## Enabling VPN on router using openvpn configuraition

I was trying to enable openvpn on my router using operwrt firmware. I ran into few roadblockers so decided to document it here for reference.

#### Step # 1 - Flash router with openwrt official image.

go to URL - https://openwrt.org/toh/start

![GitHub Logo](https://github.com/vikasmca05/openvpn-for-router/blob/master/Screenshot%20from%202020-04-20%2000-04-41.png)
Format: ![Download builds](url)

#### Step # 2 - Enable openvpn in the router.
opkg update
opkg install openvpn-openssl luci-app-openvpn
openvpn –version


Step # 3 - Download openvpn configuration from your vpn provider.

Step # 4 - Copy credentials from vpn provider. Link auth credential file location to openvpn.

Step # 5 - Change access mode on the custom auth file.

Step # 6 - Change DNS Settings.

Step # 7 - Verify.
