# Video Splitter

**This design is UNTESTED - the pcb was sent to the fab house 16.10.2016.**

This is a simple 2 channel video splitter for FPV use (but can be use with any analog signal).
It uses servo connectors for video in/out but you can solder wires directly to
the pads. Power pin is just a passthru between the 3 connectors (and it powers
the regulator). 

## Design

This is really a mashup of 2 reference designs - IA171 and LP2985 so no big
innovation here.

## Power supply

It can be powered by 5-16v if a voltage regulator is used (LP2985 or mic5205). The IA171 can be 
powered by 2.8 - 5.5V so its possible to use it without any voltage regulator if you have a stable 
power supply in that range  - bridge pins 1 and 5 (top pins) of the VREG.
