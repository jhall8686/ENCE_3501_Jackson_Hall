# Lab 1

The project is to design a 5-bit R-2R ladder DAC for an IC.

## Part 1- Voltage Divider
The first step is to design a voltage divider that can be duplicated to create the ladder.

### Schematic

Before the schematic can be drawn, the length and width of the resistor must be calculated. Taking an R<sub>sq</sub> of 855 Ω/sq and a minimum width of 12sq, the ratio between length and width can be found as $\dfrac{10 \text{k}\Omega}{855 \Omega/sq} = 11.7 sq$. Therefore the length should be $(14)(11.7) = 163.8sq$ (14 chosen so as to not be at the absolute minimum). So, the voltage divider schematic with the n-well resistors at that length and width looks as follows:

<img width="925" height="536" alt="image" src="https://github.com/user-attachments/assets/c9ae6929-3535-4671-a8e4-d102315e140c" />

Each node is exported as their visible label, so when the layout is built, they can be associated with each other.

### Icon
Once this is constructed, an icon can be created for the voltage divider through the view menu:

<img width="593" height="571" alt="image" src="https://github.com/user-attachments/assets/c5d366c9-29a2-4def-a417-d6ed75d73b90" />

A few changes were made to the generated icon to reach the icon above. 

### Layout

For the layout, the same resistor size as above must also be implemented. After this, it is a matter of placing the resistors as close as possible to each other, then connecting them with Metal 1 connectors. Three Metal 1 pins are also created, with exports that match the location and functionality of the schematic.

<img width="1139" height="606" alt="image" src="https://github.com/user-attachments/assets/c644a24c-761f-46dd-9267-6b30c638c3ca" />

Picking up the icon and running Spice code in the following configuration, it outputs the following results:

<img height="300" alt="image" src="https://github.com/user-attachments/assets/f868ba5e-e5c3-4413-aafc-33dbd576f437" />
<img height="300" alt="image" src="https://github.com/user-attachments/assets/2bd16373-fac7-4e0d-bf04-dbd7e65cb896" />

This is the expected outcome because of the 2-to-1 ratio of the voltage divider.

## Part 2- 5-bit DAC

Now the voltage divider must be utilized to create the DAC.

### Schematic

The schematic must simply be a series of the voltage dividers, but with an additional 10kΩ resistor with the same length/width as the previous ones:

<img width="459" height="767" alt="image" src="https://github.com/user-attachments/assets/7cdf2f13-7605-4796-a174-5d74119aea8d" />


