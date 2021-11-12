# CFAF128128B1-0145T Demonstration Code
This code is intended to be used the CFAF128128B1-0145T display from Crystalfontz. This 128x128 TFT display has a 1.45" diagonal dimensions and is driven by the commonly used [ST7735S Sitronix controller](https://www.crystalfontz.com/controllers/Sitronix/ST7735S/437). 

This code can, in general, be  used with other displays that use the ST7735 family of controllers with some slight modifications.

### LCD Pinnout
|   ARD   | Port | LCD  | Pin Desc                      
| --------|------|------|---------------------
|         |  PB2 | 1    | Anode for Backlight
|         |  PB2 | 2    | Cathode for Backlight
|         |  PB2 | 3    | Interface Select (0 = 3-wire SPI, 1 = 4-wire)
|         |  PB2 | 4    | Vdd              (3.0-3.6V)
|         |  PB2 | 5    | Ground           (0V)
| #10/D10 |  PB2 | 6    | Chip Select      (CS)
|  #9/D9  |  PB1 | 7    | Reset            (RES) 
| #11/D11 |  PB3 | 8    | Serial Data      (SDA/MOSI)
| #13/D13 |  PB5 | 9    | Serial Clock     (SCL)   
|  #8/D8  |  PB0 | 10   | Command/Data bit (CD/RS) (register select)

### Backlight Control
For proper backlight control, source an appropriate LED driver that restricts the current to 20mA.