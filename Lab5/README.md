# Lab 5- Full Adder

The purpose of this lab is to construct the necessary gates for a full adder, then build a full layout for it. 

## NAND

### Schematic/Icon

<img width="1109" height="679" alt="image" src="https://github.com/user-attachments/assets/666215f6-ac10-48fe-9364-a19c684fa8fc" />

### Layout

<img width="431" height="675" alt="image" src="https://github.com/user-attachments/assets/2470a7ae-e9cd-4893-9583-758065f24427" />

### Simulation

Switching point characteristics:

<img width="1092" height="572" alt="image" src="https://github.com/user-attachments/assets/57f70c72-36e1-42f6-8d9d-299b274ed957" />

<img width="1413" height="319" alt="image" src="https://github.com/user-attachments/assets/07f40041-a5d1-48aa-a1a1-5b6d9bbf75f2" />

The NAND gate switches roughly at 2.5V. 

Truth table graph:

<img width="958" height="546" alt="image" src="https://github.com/user-attachments/assets/cc673717-2f7b-4ba7-aaea-8459beaa5858" />

<img width="1384" height="350" alt="image" src="https://github.com/user-attachments/assets/247f2c9c-b2eb-4277-9577-6221a2680efc" />

Behaves as expected.

## NOT

### Schematic/Icon

<img width="1031" height="712" alt="image" src="https://github.com/user-attachments/assets/f2a4338a-c01e-453a-b613-c9bed451593b" />

### Layout

<img width="496" height="679" alt="image" src="https://github.com/user-attachments/assets/7e7a3ab6-9244-4633-9172-a52cd0615b83" />

### Simulation

Switching point characteristics:

<img width="1056" height="677" alt="image" src="https://github.com/user-attachments/assets/523bcc79-5870-4f43-8b93-7e2999ca93b4" />

<img width="1391" height="271" alt="image" src="https://github.com/user-attachments/assets/2e6252ec-f776-4589-8dee-5def4f4063bb" />

Switches at roughly 2.5V.

## XOR

### Schematic/Icon

<img width="1097" height="694" alt="image" src="https://github.com/user-attachments/assets/fc40a67d-0188-42aa-ba78-b14c3e9346b2" />

### Layout

<img width="1123" height="693" alt="image" src="https://github.com/user-attachments/assets/57b8790b-29ec-450a-9d44-9cd1f2f0e17d" />

### Simulation

Switching point characteristics:

<img width="1147" height="612" alt="image" src="https://github.com/user-attachments/assets/98be7790-3e88-4f09-bd5a-a3b50aba118d" />

<img width="1393" height="269" alt="image" src="https://github.com/user-attachments/assets/d3b5ae18-ef6b-4006-8956-479d973d07ab" />

Once again switches around 2.5V.

Truth table graph:

<img width="1161" height="601" alt="image" src="https://github.com/user-attachments/assets/4fa9669d-f8d0-43f0-9157-3306982d7276" />

<img width="1403" height="412" alt="image" src="https://github.com/user-attachments/assets/f8a7d53e-838e-4371-a222-bd809184883c" />

## Bringing It All Together (Full Adder)

### Schematic/Icon

<img width="1080" height="653" alt="image" src="https://github.com/user-attachments/assets/37462b91-0627-43f7-b880-476088a03b52" />

### Layout

<img width="1163" height="447" alt="image" src="https://github.com/user-attachments/assets/55625f95-6e5a-4477-85e3-4c98c1a2a86c" />

The layout exists within the standard cell layout except for the input wires, and all inputs can be accessed on metal 1. 

### Simulation

There arises an interesting glitch in the carry out bit due to transition delay:

<img width="1047" height="631" alt="image" src="https://github.com/user-attachments/assets/83ed37b7-d049-42ff-b482-30095c70a873" />

<img width="1406" height="577" alt="image" src="https://github.com/user-attachments/assets/6be4d37a-551d-4ea1-9234-5306ce4844dd" />
