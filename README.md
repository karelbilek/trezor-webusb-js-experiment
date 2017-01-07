# trezor-webusb-js-experiment

How to run

1. Enable webusb everywhere by by going to chrome://flags and enable "Experimental Web Platform features" and "WebUSB". Both are needed. Chrome will probably offer to restart chrome.

2. build trezor-mcu#webusb-wip

3. serve this file on https://localhost:8000 (no github pages etc, just localhost; the pages are whitelisted)

For example, by

````
sudo npm install http-server -g
openssl req \
    -x509 \
    -newkey rsa:2048 \
    -sha256 \
    -keyout key.pem \
    -out cert.pem \
    -nodes
http-server -S -p 8000
````

https is necessary.

4. go to https://localhost:8000

5. connect trezor, ignore/close the chrome webusb message

6. Open console

7. Click on button

There will be initialize sent and result received and dumped on screen. If there are "bitcoiny looking" strings in the result visible, it's probably correct.
