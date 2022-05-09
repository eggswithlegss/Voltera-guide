# Voltera-guide
Voltera and Eagle guide for Instrumental Design Final 

The goal of this project is to document the process of using the Voltera V1 PCB printer and drill. This will encoulde a step by step process starting with the initial circuit design and ending with the final PCB. 

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
The basic flow of Eagle is to start with a schematic, add all the parts and the connections, and then move to board to set up the final design to send to voltera. Add parts by clicking the add parts icon <img src="Add Parts Icon.png" alt="drawing" width="30"/> this will open a library to search the different possible parts. The search bar is not predicitve so you must search name of the part exactly. You can use an * after letters/words to serch all parts with containing those letters or word. If your part is not included in the basic parts library, there are two options: [import the part to eagle](https://www.snapeda.com), or create a pad of soldering paste on the board to attach the part later. After the part has been downloaded import it to the library by opening the library tab in task bar and clicking update library. Once all the parts are in the schematic, you connect them by the bus icon parts <img src="Connect_Parts_Icon.png" alt="drawing" width="30"/>. This tells the board what parts should be connect. Finally when the schematic is complete, it is time to switch to the board mode, by pressing the generate board from schematic icon <img src="SCH_BRD.png" alt="drawing" width="30"/>.



#### Board ####
When the board window opens make sure all parts are present, if they are not go bakc to the schematic and make sure all parts have a footprint when choosing in the library. Below is an example of parts with/without footprint. The main thing to do in the board window is to connect all the parts with wires and make the final design placement. 

<img src="Part_With_Footprint.png" alt="drawing" width="500"/>    <img src="Part_Without_Footprint.png" alt="drawing" width="500"/>
##### Layers #####
Layers in Eagle are often auto generated, for the molst part you only need to work on the top layer. If you are drilling adding holes on the top layer will automaticall edit the 'Holes' layer. The only time when it is important to look at layers is if you need to print on the bottom of your PCB board. In this case switch layers and draw on the bottom layer instead. 
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

When selecting the drill option in the voltera menu you will then be prompted to upload a circuit  and drill file. The circuit file will be a .gbr or .gbl file depending on which side of the board you are using, but the drill file will always remain the same .xln or .txt file.

You will then be prompted to use the probe to measure where the circuit will be printed on the surrogate board,to measure its height and align the circuit. If there is an error with the probe calibration try rerunning the section you are on to see if it recalbriates itself. If this does not work, take a Q-tip or other small piece of cloth and lightly wipe down the sensors in the back right of the V-one right in front of the probe base.

Then you will be prompted to use the drill component. Take your desired drill bit, there are two bits for each listed size as they go from the smallest size on the left to the largest on the right when the size label is facing you. Use the supplied hex key to loosen the fastening nut at the front of the drill. The fastening nut is small so ensure to not completelu remove it, but if you do place it in a secure location. There should be extras in the drill kit box set in case it is lost. Tighten the drill bit so only the drill head and beveled section are visible. Here is a visual for reference ().

<img src="drill bit setup.jpg" alt="drawing" width="500"/> 

Then plug in the drill motor to its power supply and attach it to the mount housing. It should play a tune when connected correctly. Then you should be able to run through the rest of the Voltera prompts to finish the drill section. Please note that drilling does create a lot of shaving bits so please sweep or vacuum them up as to keep our work space as clean as possible. 

#### Printing ####
The printing section is also a step by step process in the voltera app. For new users you will be prompted to select what the name of the conductive ink cartridge you are using. The name for the cartridge can be found under the word conductor (Note: if the cartridge is in the black dispensor it will need to be removed to see the ink's name)

#### Soldering ####
#### Other ####

## Example ## 
