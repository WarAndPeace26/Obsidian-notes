#lecture
# Slide 2| Basic I/O System Design
***
![[1.excalidraw]]

## Microcomputer
![[2.excalidraw]]

## Basic IO System
#### Purpose
1. Communicate with outside world
2. Store data

#### IO Controller Chip (8255)
1. Handles low level details
2. Takes care of electrical interface

#### IO Controller chip registers
1. Data
2. Command
3. Status

![[Pasted image 20220213013622.png]]
```ad-note
title: Block Diagram Basic IO

**Serial Interfacing:** Access one port at a time.
```
| Action   | Process                                                                                                                         |
| -------- | ------------------------------------------------------------------------------------------------------------------------------- |
| To Read  | MPU sends address of the reading port with address bus and with an RD signal, enables Input port. Data is read through Data bus |
| To Write | WR enables output port. Data bus sends data                                                                                     |

## IO Instructions
##### 1. IN
##### 2. OUT
```ad-note
title: Deets

Transfer takes place between Accumulator (AL/AX) and IO device.

IO device is identified using two methods.
1. **FIXED ADDRESS:** p8 byte that follows opcode stores an 8 bit IO address. This is called fixed because it's stored with the OPCODE in the ROM
2. **VARIABLE ADDRESS:** Register DX holds a 16 bit IO address
```

***
## [[Accessing IO Devices]]

***
## [[Data Transfer Techniques]]