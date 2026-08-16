32 Wavelength Toy
==========================
The Powder Toy's wavelengths are limited to 30 bits, even though they could store 32.  
This fork plans to change it so that 32 bits are available.  
Saves from this fork are still compatible with saves from master, although note that behaviour will of course be different.  
Some other changes have been made:  
- Photons and BRAY are not deleted when their wavelengths are all off.  They just appear grey instead.  
- FILT works differently:  
  - FILT with a tmp2 of 0 will act normally.  
  - FILT with a tmp2 of 1 and a ctype of 0 will act with the wavelength 0x00000000, not based on temperature.  
  - FILT with a tmp2 of 2 will always change based on temperature, regardless of ctype.  
  - If you add 3 to these values, the FILT will act the same, but will still delete PHOT and BRAY that have no wavelengths.  
- BRAY can pass through INVS, but only if at least one bit is set in its wavelength.  
- New serialization:  
  - TSNS: tmp of 3 will serialize to a more precise value  
  - HSWC: tmp of 2 will deserialize from a more precise value  
  - PSNS: tmp of 3 is more precise  
  - PUMP: tmp of 2 is more precise  
  - VSNS: tmp of 3 will serialize more precisely, tmp of 4 deserializes more precisely.  
