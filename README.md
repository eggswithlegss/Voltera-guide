# Voltera-guide
Voltera and Eagle guide for Instrumental Design Final 

The goal of this project is to document the process of using the Voltera V1 PCB printer and drill. This will include a step by step process starting with the initial circuit design and ending with the final PCB. 

## Contents ##
* Eagle
  * Schematic
  * Board
    * Layers
    * Drill Holes
    * Exporting
* Voltera 
  * Drilling 
    * Drill Bit
    * Drill Depth
  * Printing
    * Baking 
    * Rivits 
    * Placing Parts 
  * Soldering 
    * Reflow
  * Other
* Example

## Eagle ##
[Install Eagle](https://www.autodesk.com/products/eagle/free-download)
#### Schematic ####
The basic flow of Eagle is to start with a schematic, add all the parts and the connections, and then move to board to set up the final design to send to voltera. Add parts by clicking the add parts icon <img src="Add Parts Icon.png" alt="drawing" width="30"/> this will open a library to search the different possible parts. The search bar is not predictive so you must search name of the part exactly. You can use an * after letters/words to search all parts with containing those letters or word. If your part is not included in the basic parts library, there are two options: [import the part to eagle](https://www.snapeda.com), or create a pad of soldering paste on the board to attach the part later. After the part has been downloaded import it to the library by opening the library tab in task bar and clicking update library. Once all the parts are in the schematic, you connect them by the bus icon parts <img src="Connect_Parts_Icon.png" alt="drawing" width="30"/>. This tells the board what parts should be connect. Finally when the schematic is complete, it is time to switch to the board mode, by pressing the generate board from schematic icon <img src="SCH_BRD.png" alt="drawing" width="30"/>.



#### Board ####
When the board window opens make sure all parts are present, if they are not go back to the schematic and make sure all parts have a footprint when choosing in the library. Below is an example of parts with/without footprint. The main thing to do in the board window is to connect all the parts with wires and make the final design placement. 

<img src="Part_With_Footprint.png" alt="drawing" width="500"/>    <img src="Part_Without_Footprint.png" alt="drawing" width="500"/>
##### Layers #####
Layers in Eagle are often auto generated, for the most part you only need to work on the top layer. If you are drilling adding holes on the top layer will automatically edit the 'Holes' layer. The only time when it is important to look at layers is if you need to print on the bottom of your PCB board. In this case switch layers and draw on the bottom layer instead. 
##### Holes #####
Adding holes is done with the hole tool, it is import to get the sizing correct. Setting the size is done in a text box that pops up next to the layers at the top of the window. 
##### Export #####
Export the the infomation from eagle via File, Generate CAM data. Before importing this data into Voltera it is important to change the file extension for the bottom layer (from .gbr to .gbl) this will insure that the bottom layer is mirrored in eagle.  
## Voltera ##
[Install Voltera](https://support.voltera.io/desktop-application)
The Voltera app does a sufficient job of walking users through each step, but these are points to remember when going through this process.
#### Drilling ####
If you are planning to drill holes in your board, drill the holes PRIOR to adding the conductive ink or solder.
Prior to drilling ensure you have the sacrificial board secured to the V-one to prevent damaging the main system and you are using a drilling surrogate board (these have the letters KB printed on them)

When selecting the drill option in the voltera menu you will then be prompted to upload a circuit and drill file. The circuit file will be a .gbr or .gbl file depending on which side of the board you are using, but the drill file will always remain the same .xln or .txt file.

You will then be prompted to use the probe to measure where the circuit will be printed on the surrogate board,to measure its height and align the circuit. If there is an error with the probe calibration try rerunning the section you are on to see if it recalibrates itself. If this does not work, take a Q-tip or other small piece of cloth and lightly wipe down the sensors in the back right of the V-one right in front of the probe base.

Then you will be prompted to use the drill component. Take your desired drill bit (If you are using rivets check the intended hole size for your rivets), there are two bits for each listed size as they go from the smallest size on the left to the largest on the right when the size label is facing you. Use the supplied hex key to loosen the fastening nut at the front of the drill. The fastening nut is small so ensure to not completely remove it, but if you do place it in a secure location. There should be extras in the drill kit box set in case it is lost. Tighten the drill bit so only the drill head and beveled section are visible. Here is a visual for reference ().

<img src="drill bit setup.jpg" alt="drawing" width="500"/> 

Then plug in the drill motor to its power supply and attach it to the mount housing. It should play a tune when connected correctly. Then you should be able to run through the rest of the Voltera prompts to finish the drill section. Please note that drilling does create a lot of shaving bits so please sweep or vacuum them up as to keep our work space as clean as possible. 

Now check the board to ensure the drill went through the board completely. If it has not you will need to change your drill depth in the advanced settings section after the probing section, but before the drill starts to drill into the board. This is similar to the structure of the printing or soldering sections before they begin to print their respective cartridges.


#### Printing ####
The printing section is also a step by step process in the voltera app. For new users you will be prompted to select what the name of the conductive ink cartridge you are using. The name for the cartridge can be found under the word conductor (Note: if the cartridge is in the black dispenser it will need to be removed to see the ink's name)

Leaving the ink cartridge out of the fridge for 15 minutes does allow for a smoother dispensing process.

If there are issues with flow rate when priming the ink cartridge, try to use a paper towel to clear off the dispensing tip. If that does not work you can either switch dispensing tips or use a bread board component such as a wire and clearing out the hole. NOTE: doing the second method will increase the dispensing tip's diameter such that very compact or detailed circuits will result in the lining flowing into one another while printing.

After printing, then follows the baking phase which typically takes an hour so try to start the PCB process early to ensure time for troubleshooting and testing.

After your circuit is printed you will then begin to rivet your rivets into their holes if you are planning to use the hand soldering technique. Check the rivets hole size on their container to ensure they will fit in the holes you have drilled. If the holes are too small you can redrill the holes by going through the steps in the drill section but choosing the aligned section within the drill section.
#### Soldering ####
The soldering section can be done one of two ways either through the use of the solder paste or by using solder wire to attach components yourself. It is recommended that you use drilled holes and rivets if you are using solder wire. This gives stronger connections and helps prevent silver scavenging.

If you are using either method you still need to wipe your circuit with the brandishing pad to remove some of the oxidized layers on your lining which gives a stronger connection to between the solder and lining. 

The soldering paste method is similar to the print method so any tips from that method should translate to this section as well.

When hand soldering the best tips are to keep your soldering iron at a low temperature and do not heat the solder for too long. You want to place your component through your riveted hole and apply solder on both sides of your board, trying to secure the component to the rivet. Securing the component to the rivet is a bit difficult so just ensuring it remains in place with solder on both ends should be sufficient.

#### Other #### 

Silver scavenging is when solder is too hot and begins to eat away at the silver lining on your pcb board. To prevent this ensure you are using the voltera soldering wire and your soldering iron is around 356 °F (180 °C).

## Example ##
