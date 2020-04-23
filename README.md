# openvpn-for-router
## Enabling VPN on router using openvpn configuraition

I was trying to enable openvpn on my router using operwrt firmware. I ran into few roadblockers so decided to document it here for reference.

#### Step # 1 - Flash router with openwrt official image.

* go to URL - https://openwrt.org/toh/start

* You will see the list of images available. Select and download the correct image based on your router model.

![GitHub Logo](https://github.com/vikasmca05/openvpn-for-router/blob/master/Screenshot%20from%202020-04-20%2000-04-41.png)


* Go to Luci GUI of your router and flash the image on your router.

![GitHub Logo](https://github.com/vikasmca05/openvpn-for-router/blob/master/FlashOperation.png)


#### Step # 2 - Enable openvpn in the router.
Connect to the router using SSH and execute below commands - 

* opkg update
* opkg install openvpn-openssl luci-app-openvpn
* openvpn –version

Once openvpn is installed, then VPN tab will be show in the home screen of the Luci router interface.
![GitHub Logo](https://github.com/vikasmca05/openvpn-for-router/blob/master/VPNOption.png)


#### Step # 3 - Download openvpn configuration from your vpn provider and upload to Router

 * Your VPN provider will provide the openvpn configuration file. Download the file. Along with openvpn config file, you will also get the username and password required for authentication.
 
 * Upload the openvpn config file here from Luci GUI
![GitHub Logo](https://github.com/vikasmca05/openvpn-for-router/blob/master/UploadOpenVPNConfigFile.png)


#### Step # 4 - Copy credentials from vpn provider. Link auth credential file location to openvpn.
 * Copy the username and password as obtained from your vpn vendor to auth.txt file in new lines.
 * Copy the file to /etc/openvpn/custom/auth.txt in router using ssh.
 * Update the file access in the openvpn configuration file - auth-user-pass /etc/openvpn/custom/auth.txt
  /etc/openvpn/custom/auth.txt
![GitHub Logo](https://github.com/vikasmca05/openvpn-for-router/blob/master/custom%20auth%20file.png)


#### Step # 5 - Change access mode on the custom auth file.

#### Step # 6 - Change DNS Settings.

#### Step # 7 - Verify.
