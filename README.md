# openvpn-for-router
## Enabling VPN on router using openvpn configuraition

I was trying to enable openvpn on my router using operwrt firmware. I ran into few roadblockers so decided to document it here for reference.

#### Step # 1 - Flash router with openwrt official image.

go to URL - https://openwrt.org/toh/start

You will see the list of images available. Select and download the correct image based on your router model.
![GitHub Logo](https://github.com/vikasmca05/openvpn-for-router/blob/master/Screenshot%20from%202020-04-20%2000-04-41.png)
Format: ![Download builds]

Go to Luci GUI of your router and flash the image on your router.
![GitHub Logo](https://github.com/vikasmca05/openvpn-for-router/blob/master/Screenshot%20from%202020-04-20%2000-04-41.png)
Format: ![Flash Image]

#### Step # 2 - Enable openvpn in the router.
Connect to the router using SSH and execute below commands - 

* opkg update
* opkg install openvpn-openssl luci-app-openvpn
* openvpn –version

Once openvpn is installed, then VPN tab will be show in the home screen of the Luci router interface.
![GitHub Logo](https://github.com/vikasmca05/openvpn-for-router/blob/master/VPNOption.png)
Format: ![Flash Image]

#### Step # 3 - Download openvpn configuration from your vpn provider and upload to Router

 * Your VPN provider will provide the openvpn configuration file. Download the file. Along with openvpn config file, you will also get the username and password required for authentication.
 * Upload the openvpn config file here
![GitHub Logo](https://github.com/vikasmca05/openvpn-for-router/blob/master/UploadOpenVPNConfigFile.png)
Format: ![Upload Config]

#### Step # 4 - Copy credentials from vpn provider. Link auth credential file location to openvpn.


#### Step # 5 - Change access mode on the custom auth file.

#### Step # 6 - Change DNS Settings.

#### Step # 7 - Verify.
