# Lab 2

The project is to design a padframe for the DAC designed in Lab 1.

### Loading the DAC and adding new cells

<img width="213" height="123" alt="image" src="https://github.com/user-attachments/assets/d2f90873-cd1f-4696-85e8-3d3db0d61499" />

The DAC needs to be included, along with the voltage divider, so that they can be built off of in pad, padframe, and final_ic.

### The Pad

#### Schematic/Icon

The pad on the schematic level is a simple GPIO pin, so it is designed accordingly:

<img width="1130" height="536" alt="image" src="https://github.com/user-attachments/assets/815a4414-159f-4b54-821f-1c27a0d32896" />

The name pin is an export and will be used later.

#### Layout

The pad requires a 250x250 contact and a 200x200 overglass, which will allow metals to connect with the pad. 

<img width="803" height="686" alt="image" src="https://github.com/user-attachments/assets/9610bb41-fc68-4791-891a-1b17bacb3ed4" />

The contact needs to be exported to match the pin export.

### The Padframe

The padframe simply requires as many pads as are needed to work with the DAC and also occupy a square formation, which happens to be 8.

#### Schematic/Icon

<img width="1160" height="523" alt="image" src="https://github.com/user-attachments/assets/ea8ea976-e8d5-4bb9-8de0-7bd5ac066cc7" />

As can be seen above, the padframe in the schematic is simply an array of pins connecting to an array of pads. The green wire coming off is an 8-signal bus, and connects all 8 pads to their respective exports.

#### Layout

Using the multiply function, the 4x4 square can be made with a single pad layout. Once the extra pads are deleted from this, you are left with:

<img width="923" height="683" alt="image" src="https://github.com/user-attachments/assets/db1d8894-6de6-4ef8-8f15-55aa15d1fe83" />

For each pad, the contact was exported to connect to pin[x]. The order was chosen based on the orientation of the DAC within the padframe.

### Final IC

Once the padframe is designed, all that needs to be done is to connect the padframe with the DAC.

#### Schematic

<img width="1182" height="564" alt="image" src="https://github.com/user-attachments/assets/ba5cd642-1aa5-4b14-a2ba-738b19223355" />

The order of connections was decided based on the orientation of the layout; it can be seen that the seemingly out of order connections will function quite nicely when connected in the layout.

#### Layout

<img width="810" height="677" alt="image" src="https://github.com/user-attachments/assets/fdcf414f-a4ca-4b69-aba6-3b41aed83074" />

There are a few things to discuss with this layout-- the first is that the voltage divider layout takes outputs from specific places, so the pinout was chosen carefully for ease of routing. The second is that the pads connect Metal 2 to Metal 3, so the Metal 1 connections on the DAC need to have a via to Metal 2. This is why the wires turn pink. 

