# Inkscape-GCode-Extension
--------------------------

Put the contents of this .zip folder into the "inkscape\share\extensions" folder. Once it is there it will show up under the “extensions” tab in inkscape.

* Laser ON Command: The command for turning ON the laser.  For example, M03 or M106.
* Laser OFF Command: The command for turning OFF the laser.  For example, M05 or M107.
* Travel Speed: The speed of the machine when the laser is OFF in mm/min.
* Laser Speed: The speed of the machine when the laser is ON in mm/min.
* Laser Power: If you have PWM control, then you can adjust this.  For J Tech firmware and most 3D printers use a number between 0 and 255 (255 being full power). For GRBL 0.9 and 1 standard, use a number between 0 and 12000 (12000 being full power). If you don’t have PWM, keep at max power (either 255 or 12000).
* Power On Delay: This will turn on the laser and wait to move until the delay is complete. It is used to heat up the material and initiate the burning process. Delay in ms for 3D printers and seconds for GRBL.
* Passes:  If cutting, this will repeat the entire path by the number of passes. If engraving leave as 1.
* Pass Depth:  This will move Z axis down by this amount for each pass. For example, 3mm piece of material with 3 passes might use 1mm per pass to cut all the way through.
* Directory:  The directory to store the file.
* Filename:  Name of the file.
* Add numeric suffix to filename:  Adds a number to the name in case there already is a file with the same name in the directory.
* All Units: Change the units to either mm or inches. This will make everything in inches or mm.
* Live preview:  Shows the path being generated.
* Apply: Click to run the converter.

Drawing Text:
-------------
* Step 1:  Use the TEXT tool in inkscape to draw your text. The bottom left corner is you 0,0 location of you machine.
* You need to convert the object into a path. All items drawn in inkscape are a vector object.  You can convert them into a “path” that will actually "draw" the object.  The laser then takes this path to generate the G Code.
* Under "Extensions" click on "Generate G Code" and "Laser Tool".
