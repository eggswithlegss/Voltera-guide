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

## Eagel ##
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
#### Drilling ####
#### Printing ####
#### Soldering ####
#### Other ####

## Example ## 
