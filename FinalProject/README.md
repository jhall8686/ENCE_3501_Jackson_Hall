# Final Project- Accumulator A

<img width="1423" height="1125" alt="image" src="https://github.com/user-attachments/assets/3151170a-efa3-4f7b-8b9c-41a077e6f5a1" />

The Very Simple Microprocessor has lots of parts, and having selected Accumulator A to design in VLSI, there are a few needed building blocks.

<img width="1282" height="1125" alt="image" src="https://github.com/user-attachments/assets/3e0c7781-32c5-48ad-821d-4c716008b93b" />

## Building Blocks

Namely, DFFs, NAND gates, and tri-state buffers are needed to construct the Accumulator.

Thankfully, there is a library-- `MuddLib07.jelib`-- that contains most of these. *(notably, the transistors are without SPICE models-- I will be using cmosedu_models.txt and adding those models to the library gates)*

<img width="1987" height="860" alt="image" src="https://github.com/user-attachments/assets/d5535352-3242-44f5-b8e6-c68c5e534f7a" />

Here are both NAND2 and NAND3 (it will become obvious why the NAND3 is necessary in a moment).

And here is the tri-state buffer (inverted to match the Logisim circuit above):

<img width="1135" height="896" alt="image" src="https://github.com/user-attachments/assets/f61d3ff4-6513-42f5-9794-57713fddf4e0" />

And now for the DFF-- MuddLib did not have any DFFs that I considered to be worth using (they were either confusing or inadequate) so I built my own:

<img width="1007" height="780" alt="image" src="https://github.com/user-attachments/assets/edfaf36c-52f9-4178-9af1-8f0fedca0f59" />

This is based off of a schematic found online, but it works according to this transient analysis:

<img width="1332" height="741" alt="image" src="https://github.com/user-attachments/assets/4b84778a-f8d0-4367-aef2-011d48daca74" />

<img width="2000" height="871" alt="image" src="https://github.com/user-attachments/assets/7969ffbb-d5fc-4b99-aace-89d0c0c0ce3f" />

The output of the DFF changes to the input on the rising edge of the clock, and otherwise latches to its previous value. The reset (active low) sets the gate to 0V.

## Accumulator A

<img width="1984" height="828" alt="image" src="https://github.com/user-attachments/assets/c45ab7dc-0b27-4eb3-8c4e-4d77eae378d6" />

(Essentially just a copy-paste of the Logisim circuit within Electric VLSI with the aforementioned building blocks).

But does it work? Here is a transient analysis to find out:

<img width="1333" height="875" alt="image" src="https://github.com/user-attachments/assets/af6a7a6e-3a1d-493e-8255-4f14a91285f7" />

<img width="2000" height="1027" alt="image" src="https://github.com/user-attachments/assets/d405cc52-ec74-43a1-9d0b-cd79af3a16df" />

As can be seen above, with EnableA high and LatchA/Clear high, the signals from A propagate through to the bus. LatchA causes the signal to preictably latch to its previous value, while clear resets the whole register to 0V. When EnableA is turned off, the IB outputs end up floating-- this is the reason for the strange waveforms and delay. When connected to a bus, this would allow through another signal rather than passing the AccumulatorA signal. 
