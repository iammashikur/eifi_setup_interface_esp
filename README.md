This code is for an ESP8266 WiFi module that creates a soft access point (AP) and allows a user to connect to it and configure the ESP8266 to connect to a different WiFi network. The ESP8266 uses a web server and DNS server to serve a captive portal, which is a webpage that allows the user to enter the credentials of the network they want to connect to. The code also includes a function to check if a string is an IP address and another function to convert an IPAddress object to a string.

### The first part of the code includes necessary libraries for the ESP8266 module.
### The next part define the default SSID and PASSWORD for the soft AP.
### The struct 'settings' is used to store the user entered wifi credentials.
### The softAP_ssid and softAP_pass are defined using the pre-defined SSID and PASSWORD.
### The next part defines the IP address and net mask for the access point.
### DNS server is defined next, and the server port is set to 53
### The web server object is created on port 80
### The function 'isIp' is used to check if a given string is a valid IP address or not.
### The function 'toStringIp' is used to convert an IPAddress object to a string.
### The function 'captivePortal' is used to check if the request is for the controllers IP or not. If not, redirect to the captive portal.
### The function 'handleRoot' is called when the root of the web server is requested. This function first checks for the captive portal, then checks if the ssid and password arguments are present in the request. If present, it tries to connect to the wifi network with the provided credentials. If the connection is successful, it saves the wifi credentials to the EEPROM and sends a success message. If the connection fails, it sends an error message. If the ssid and password arguments are not present, it sends a setup message.
