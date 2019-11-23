# ZTE MF910Z - Telstra 4GX WiFi Modem/Dongle (android_root)
Root for ZTE MF910Z (Telstra 4GX WiFi Dongle/Modem)

### Disclaimer
I am not responsible for your device or anything that may happen to your device. By following these steps, you accept full responsibility for your device and are aware that these steps may void any standing warranties.

## Step 1 - Prepare your device

Connect to the dongle wifi hotspot.

1. Disconnect from the mobile network.
  a. Go to http://192.168.0.1/
  b. Login (Default pasword is "password").
  c. On the 'Home' tab, at the bottom press the 'disconnect' button.
2. (MAC/LINUX) On the terminal enter:

``

curl -i --referer http://192.168.0.1/ "http://192.168.0.1/goform/goform_set_cmd_process?isTest=false&goformId=SET_DEVICE_MODE&debug_enable=1"

``

You should recive something like this:

``

HTTP/1.1 200 OK
Server: WebServer-Webs
Pragma: no-cache
Cache-Control: no-store
Content-Type: text/html
X-Frame-Options: sameorigin
X-XSS-Protection: 1; mode=block

{"result":"success"}%   

``

If you recieve a fail status, reboot your dongle and the last step again try again.
