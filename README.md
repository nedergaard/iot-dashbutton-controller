# iot-dashbutton-controller
Simple ESP8266 controller sends EnigmaIOT message on start up and goes to sleep

Intended for a schematic similar to [this](https://imgur.com/tHOaPzJ)

Sets IO 0 high to keep the controller enabled until a message has been sent. Then it is set low to allow the controller to be disabled. This state uses very little power, around 4 uA.

Message sent. Value is always 1.
```
<Network_name>/<node_name or node_address>/data  {"button_pushed":1}
```
