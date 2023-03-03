# Merlin TCP BBR
Merlin firmware TCP BBR Linux kernel module

## Prerequisite
Since TCP BBR requires Linux kernel 4.9+, only 5.04axhnd devices are supported.
Namely, GT-AX11000 Pro, GT-AX6000, GT-AXE16000, RT-AX86U Pro, RT-AX88U Pro, ZenWiFi Pro XT12.

## Installation
```shell
# Upload the module to /jffs
scp -O admin@192.168.50.1:tcp_bbr.ko /jffs

# Login to the router and load the module
insmod /jffs/tcp_bbr.ko

# Enable TCP BBR
echo bbr > /proc/sys/net/ipv4/tcp_congestion_control
```
If you want to enable bbr by default, you can put the last two commands in ```/jffs/scripts/services-start```
and enable jffs scripts from the WebUI.

## Sponsor
It takes a lot of time to create and maintain a project.  If you think it helped you, could you buy me a cup of coffee? 😉  
You can use any of the following methods to donate:

| [![PayPal](/images/paypal.svg)](https://www.paypal.com/paypalme/tianchentang)<br/>Click [here](https://www.paypal.com/paypalme/tianchentang) to donate | ![Wechat Pay](/images/wechat.jpg)<br/>Wechat Pay | ![Alipay](/images/alipay.jpg) Alipay |
|--------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|--------------------------------------|
