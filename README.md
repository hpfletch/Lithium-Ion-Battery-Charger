# Lithium Ion Battery Charger

This simple device charges single cell lithium ion batteries for use with battery powered devices. It's based on a Microchip MCP73833 linear charge controller which offers features such as programmable charge current, charge status indication and automatic end-of-charge control, to name a few. 

![alt text](https://github.com/hpfletch/Images/blob/master/Schematic.PNG)

Power is supplied to the device from any 5V USB cell phone charging brick or USB power port. I have designed and tested a small form factor PCB which is assembled with SMD components to reduce the overall footprint. A simple switching circuit allows the battery to power a 3.3V load after charging is complete. The following two images displays the designs iterations.

### Version 1

![alt text](https://github.com/hpfletch/Images/blob/master/V2%20Drawing.png)


### Version 2

![alt text](https://github.com/hpfletch/Images/blob/master/V3%20Drawing.png)

Testing the device shows it can successfully charge a single cell lithium ion battery by cycling through the following charge modes.
  1. Preconditioning: If the battery voltage is less than threshold of 3.99V a regulated 100mA charging current flows into the battery.        The controller switches status 1 output low to indicate charging has started. 
  2. Fast Charge: After the battery voltage has exceeded the threshold value, the fast charge current of 1A flows.
  3. Constant Voltage: Once battery voltage has reached 4.2V, a regulated voltage of 4.2V is outputted by the charge controller. A small        charge current will flow as battery voltage fluctuates.
  4. Charge Complete: After the charge timer has expired or the charging current is less than 37.5mA the controller will enter charge          complete mode and the charge current will be set to 0. The status 2 output is switched low, lighting an indicator LED.
 
 The following image shows a test device switching the status outputs of the MCP73833, indicating the charge status.
 
![alt text](https://github.com/hpfletch/Images/blob/master/modes.png)
