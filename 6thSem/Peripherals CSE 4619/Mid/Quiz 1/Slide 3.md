#lecture 
# Slide 3| Microprocessors
***
## AVR
![[Pasted image 20220213232219.png]]

| Series name | # of pins | Flash Memory | Special Features           |
| ----------- | --------- | ------------ | -------------------------- |
| TinyAVR     | 6-32      | 0.5 - 8 kB   | Small in size              |
| MegaAVR     | 28-100    | 4 - 256 kB   | Extended Peripherals       |
| XmegaAVR    | 44-100    | 16 - 384 kB  | Event system included, DMA | 

#### ATMega16
> 1. 16 kB self-programmable flash program memory
2. 512 Bytes of EEPROM
3. 1 Kbyte internal SRAM
4. 32 8-bit general purpose working register
5. 32 programmable IO lines out of total 40 pins DIP
6. 8 channel 10-bit ADC
7. Two 8-bit timer/counter
8. One 16 bit timer/counter
9. USART
10. Operating Voltages 4.5 V - 5.5 V
11. 0 - 16 MHz

##### Port A
Analog inputs to the ADC

Also 8 bit bi-directional IO port when ADC is not being used.

##### Port B, C, D
Bi-directional 8 bit IO Ports

##### Oscillator
> 1, 2, 4, 8 Mhz programmable internal clock. Maximum 8 MHz

##### Status Registers
![[Pasted image 20220214001937.png]]
Ishmam Tashdeed High School Viq Nessa Zunior College

**V:** Two's complement Overflow Flag
**S:** Sign Bit Flag (S = N *XOR* V)
**H:** Half-carry Flag
**T:** Bit Carry Flag
**I:** Global Interrupt Enable Flag

##### USART
Universal Synchronous Asynchronous Receiver Transmitter

##### Serial Peripheral Interface
Common Clock sourse
Faster transmission than USART