# firmware_mill
How to use

--Trace and pad cutting
Resize the autoleveling area in the firmware
Plot the autoleveling probs with the sharpy
find holes to add screws inorder to hold the board flat and remove any spring
attach the homeing prob and home
start cut
	cut depth of .15
	travel hight of 5
	feed of 1 (check in gcode)
	Starting code
		G28
		G29
		M42 P8 S255

--Cutting holes
Import holes as excellon
select all holes
home use clicky switch to triger close to the copper clad
start cut
	cut depth of 3
	travel hight of 5
	feed of 3
	Starting code
		M42 P8 S255
		
--Laser pads
clean board with rubbing achohol
cover the board in painters tape
import silkscreen
generate geometry
home and focus laser
start burn
	cut depth of 0
	travel hight of 5
	feed of 3
	Starting code
		Nothing
	After code is generated open
		replace all G00 Z5.0000 with M107 (off)
		replace all G01 Z0.0000 with M106 (on)
		
--Paint board and pull off pad covers
	