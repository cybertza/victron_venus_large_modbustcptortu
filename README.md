# Victron Large Modus Server
A modbus server instance to run on the the cerbo or venus on port 5020 and use a usb to 485 device to allow another service to use it as a modbus TCP server so that it can interigte what is on the other side, for me its a sunsynk inverter this is a node red flow


Instalation instructions
Enable SSH
Login via SSH

Execute 
```
/opt/victronenergy/swupdate-scripts/set-feed.sh candidate 
```
enables other packages that can be installed by opkg
```
opkg update
```
```
/opt/victronenergy/serial-starter/stop-tty.sh ttyUSB0 
```
# this allows you to use the USB port and stops the victron from polling it for other services.


### if i get some stars and downloads or sponsors on this i will prob put a bit more time into it. make it a serivce and make the code more robust
## at the stage this just read registers and will miss packets under heavy load, so need to make it more robust before adding write coils back in.
<img width="814" alt="image" src="https://github.com/cybertza/victron_venus_large_modbustcptortu/assets/20600538/0cde4666-54c9-4df3-8756-0240f12094c8">
