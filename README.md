# Lithium Ion Battery Charger

This simple device charges single cell lithium ion batterys for use with battery powered devices. It's based on a Microchip MCP73833 linear charge controller which offers features such as programmable charge current, charge status indication and automatic end-of-charge control, to name a few. 

![alt text](https://github.com/hpfletch/Images/blob/master/Schematic.PNG)

Power is supplied to the device from any 5V USB cell phone charging brick or USB power port. I have designed and tested a small form factor PCB which is assembled with SMD components to reduce the overall footprint. A simple switching circuit allows the battery to power a 3.3V load after charging is complete. The following two images displays the designs iterations.

#Version 1

![alt text](https://github.com/hpfletch/Images/blob/master/V2%20Drawing.png)


#Version 2

![alt text](https://github.com/hpfletch/Images/blob/master/V3%20Drawing.png)

Testing the device shows it can sucessfully charge a single cell lithium ion battery by cycling through the following charge modes.
  1. Preconditioning
  2. Fast Charge 
  3. Constant Voltage 
 
 The following image shows a test device switching the status ouputs of the MCP73833, indicating the charge status.
![alt text](https://github.com/hpfletch/Images/blob/master/V2%20Drawing.png)
