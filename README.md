# Sigfox Connected Target

##Description

Arduino code for the Instructable tutorial Sigfox Connected Target for Nerfs.

It shows how to send a Sigfox message using the airboard with sigfox shield SigBee (Atim module) when the connected target has been hit. 


##Get hardware
[The AirBoard](http://sales.theairboard.cc/)

[Atim SigBee shield](http://www.atim.com/fr/produits/catalogue/modules-shields/sigbeelorabee/)

[Piezo sensor](http://www.meas-spec.com/product/t_product.aspx?id=2478)

Note: The AirBoard has been designed to be wirelessly reprogrammable. The microUSB connector is used for battery charging only. To upload a new program, you will need additional wireless shields such as XBee or BLE and their associated USB dongle, or an external serial connection over FTDI.

##Installation

Install Arduino IDE

Get the Arduino library from [API for ARM modules](http://atim-radiocommunications.github.io/armapi/)

Copy/Past the armapi folder under Arduino/libraries

##Run the code

- plug the piezo sensor between the A4 and 3.3V pins
- repeatedly read the sensor from analog pin A4
- send the value through the SIGFOX network when the target has been hit
Note that the ETSI limitation allows a maximum of 140 messages per day.
   
1. upload this program to The AirBoard via the BLE-LINK/XBee shield
2. replace the BLE-LINK/XBee shield by the SIGFOX shield
3. connect to the SIGFOX backend: http://backend.sigfox.com
