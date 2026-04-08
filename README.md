32 Wavelength Toy
==========================
The Powder Toy's wavelengths are limited to 30 bits, even though they could store 32.  
This fork plans to change it so that 32 bits are available.  
Saves from this fork are still compatible with saves from master, although note that behaviour will of course be different.  
Some other changes have been made:  
- Photons and BRAY are not deleted when their wavelengths are all off.  They just appear white instead.  
- FILT with a tmp2 of 1 and a ctype of 0 will act with the frequency 0x00000000, not based on temperature.  
- FILT with a tmp2 of 2 will always change based on temperature, regardless of ctype.  
