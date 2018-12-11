1) Determine your device IP address - by visiting your router web panel then go to list of connected devices. The best option is to set nanoleaf to have static IP address.
2) Download https://chrome.google.com/webstore/detail/advanced-rest-client/hgmloofddffdnphfgcellkdfbfbjeloo/related and run that app 
3) Hold down the ON button on the Panel for 5 seconds; the LED will start flashing
4) Send POST request to http://IP:16021/api/v1/new to get token (example below):
<img src="https://i.imgur.com/HlN7abh.png">
5) Configure your widget using those details (IP Address without `http://` and `:16021`). Remember that effects names are case sensitive
6) Edit OBS shortcut - add a variable that will allow it to connect to Nanoleaf device: add parameters:
 `--allow-running-insecure-content --disable-web-security` 
 
    So it looks like that:
 `"C:\Program Files (x86)\obs-studio\bin\64bit\obs64.exe" --allow-running-insecure-content --disable-web-security`
 May vary depending on your install path
    <img src="https://i.imgur.com/UZdBS9C.png">
Note: this widget will not work directly from browser, so you need to add it to OBS in order to test it 