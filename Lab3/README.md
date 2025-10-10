# Lab 3

The end goal of this lab is to create a pad connected NMOS with ESD protection. 

## Diodes

### Schematic

<img width="1087" height="328" alt="image" src="https://github.com/user-attachments/assets/19652e93-32dc-4e64-8926-a76d7561f245" />

<img width="1131" height="379" alt="image" src="https://github.com/user-attachments/assets/77633cdb-1dd7-44c5-9636-5ba2dedc8dd0" />

The two diodes will be used to build the basic ESD protection for the pads.

### Layout

<img width="406" height="682" alt="image" src="https://github.com/user-attachments/assets/62cfadf9-6575-4ccc-9f3b-deb9e28c5da4" />
<img width="427" height="677" alt="image" src="https://github.com/user-attachments/assets/f6634194-b335-405e-bfff-5b1f375e5eb2" />

The layout is as simple as creating the pActive/nWell (nActive/pWell) and providing outputs. 

## Pads with ESD Protection

The pad with ESD protection is similar to a normal pad, but with the additional diode circuit:

### Schematic

<img width="546" height="776" alt="image" src="https://github.com/user-attachments/assets/d4c1e59b-abec-404a-9842-58d27b8a5052" />

### Layout

<img width="526" height="783" alt="image" src="https://github.com/user-attachments/assets/b27defb7-cb67-48bd-8f3a-6f40247dcb35" />

The layout was designed with vdd and gnd rails for ease of connection once the padframe needs to be constructed.

## Padframe with ESD Protection

The padframe is simply the pad_esd cell connected together as many times as is necessary to handle the pinout of the NMOS. In this case, the NMOS only has four pins, but vdd and gnd now need a pin to attach to because of the ESD protection, so an 8-pad padframe is used.

### Schematic

<img width="1139" height="712" alt="image" src="https://github.com/user-attachments/assets/5e8d3ad8-b10b-4825-ab2f-124511ebe5c7" />

*(Similar to the pad schematic, but with an 8-wide bus)*

### Layout

<img width="710" height="654" alt="image" src="https://github.com/user-attachments/assets/25981e94-d15f-455b-b4c4-4f3feb560b37" />

The vdd and gnd rails are all connected to each other, and the pads are exported with pin numbers.

## Final IC

Now the NMOS needs to be placed inside of the padframe. 

### Schematic

<img width="1074" height="533" alt="image" src="https://github.com/user-attachments/assets/c396404d-fa7c-4105-b15d-0f5984951974" />

The pins were chosen because of where the layout will have to route:

### Layout

<img width="825" height="649" alt="image" src="https://github.com/user-attachments/assets/f17d69d7-9799-4185-831e-9ad44da61cce" />

### Final 3D View

<img width="1149" height="728" alt="image" src="https://github.com/user-attachments/assets/63677fa1-4c45-4341-8d05-ac76696b29df" />

