-----------------------------------------------------------
# I2S to TDA1540
[Project download](https://github.com/c2titan/I2S-TDA1540)

VHDL code for converting standard I2S data (64fs) to the offset-binary data needed for TDA1540 DAC (I2S to simultaneous for TDA1540).
"I2S 2x32=64-bit = 64fs" to "14-bit offset-binary" with inverted MSB and inverted stop-clocked BCK) for TDA1540 DAC (stereo) without the use of MCLK (= even less digital work)
- basic data synchronisation is incorporated on LRCK signal
- the sound is nice, very musical, clean, without digital interference
- my VHDL code is very simple, without advanced techniques, based mostly on standard logic
- therefore inexperienced users can understand and modify it for other similar DACs
- it has low load on the CPLD and it takes up little memory
- only 3 signal wires (I2S) are needed for input (DATA, BCK, LRCK).
- output is true offset-binary specified for TDA1540: -- CL - stopped Left DAC clock -- DL - Left DAC data (inversed MSB) -- CR - stopped Right DAC clock -- DR - Right DAC data (inversed MSB) -- LL and LR - Latch for both channels (latched together)
- it flawlessly works with the cheap CPLD EPM240T100C5 from aliexpress and can be easily configured for others
- my VHDL code is open and free for all

-----------------------------------------------------------
# I2S to simultaneous for TDA1541A
[Project download](https://github.com/c2titan/I2S-simultaneous-TDA1541A)

VHDL code for converting standard I2S signal (64fs) to offset-binary (simultaneous) ("I2S 2x32=64-bit = 64fs" to "16-bit offset-binary" with inverted MSB and stop-clocked BCK) for TDA1541A DAC (stereo) without the use of MCLK.
- basic data synchronisation is incorporated on LRCK signal
- the sound is nice, clean, without digital interference
- my VHDL code is very simple, without advanced techniques, based mostly on standard logic
- therefore inexperienced users can understand and modify it for other similar DACs
- it has low load on the CPLD and it takes up little memory
- only 3 signal wires (I2S) are needed for input (DATA, BCK, LRCK).
- output is true offset-binary (simultaneous) specified for TDA1541A: 
- - CL - stopped DAC clock 
- - DL - Left DAC data (inversed MSB) 
- - DR - Right DAC data (inversed MSB)
- - LE - Latch for both channels (latched together)
- it flawlessly works with the cheap CPLD EPM240T100C5 from aliexpress and can be easily configured for others
- my VHDL code is open and free for all

-----------------------------------------------------------
# I2S to simultaneous for D20400 in the TDA1541A like mode
[Project download](https://github.com/c2titan/I2S-simultaneous-D20400)

VHDL code for converting standard I2S data (64fs) to the offset-binary data needed for 20-bit D20400 DAC (tested on DAC0013 module), configured in the TDA1541A like mode (ultraanalog-d20400-application-note-ap02-pdf - section: 4.5 Simultaneous / Inverted Clock / Inverted WS/LOAD).


-----------------------------------------------------------
# If you like my work and find it helpful, you can donate coffee for me :D 
- https://www.buymeacoffee.com/miro1360coffee  Thank you :)

miro1360
