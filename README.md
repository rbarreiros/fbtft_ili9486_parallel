# fbtft_ili9486_parallel
ILI9486 8080 8bit parallel mode to be used with FBTFT kernel modules

This LCD version doesn't have a touch controller, although it supports touch. It multiplexes the touch lines with the LCD lines in LCD_CS, LCD_CD, LCD_D0 and LCD_D1, but unfortunately, since Raspberry Pi doesn't have an analog input, touch doesn't worki with Raspberry Pi without external hardware like a touch controller, even so, logic need to be handled within the fbtft module (this would require a new module) to handle the switching between LCD and Touch reading. On another SBC's with analog inputs, it needs a new module to extend the LCD functionality, switch between the touch reading and LCD display and send the touch events to the kernel event system. 
