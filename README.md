# Video Splitter

**This design is UNTESTED - the pcb was sent to the fab house 16.10.2016.**

This is a simple 2 channel video splitter for FPV use (but can be use with any analog signal).
It uses servo connectors for video in/out but you can solder wires directly to
the pads. Power pin is just a passthru between the 3 connectors (and it powers
the regulator). 

## Design

This is really a mashup of 2 reference designs - IA171 and LP2985 so no big
innovation here. According to the datasheet the IA171 can drive to 75ohm loads.

## Power supply

The splitter was designed to be powered by 5-16v if a 3.3v voltage regulator is used (LP2985 or mic5205). 
The IA171 can be powered by 2.8-5.5V so its possible to use it without any voltage regulator if you have a stable 
power supply in that range - bridge pins 1 and 5 (top pins) of the VREG and
applu 2.8-5.5v to any of the 3 pin connectors (middle pin).

## [BOM](BOM.csv)


| "Qty" | "Value"         | "Device"                        | "Package"   | "Parts"             | "Description"         | "Link" |
|-------|-----------------|---------------------------------|-------------|---------------------|-----------------------|----|
| "3"   | ""              | "M03LOCK"                       | "1X03_LOCK" | "VIN, VOUT1, VOUT2" | "Header 3"            | "" |
| "1"   | "0.1uF"         | "CAP0805"                       | "0805"      | "C1"                | "Capacitor"           | "" |
| "1"   | "100uF"         | "CAP_POL3528"                   | "EIA3528"   | "C3"                | "Capacitor Polarized" | "" |
| "1"   | "10nF"          | "CERAMIC-10NF-50V-5%-X7R(0805)" | "C0805"     | "C7"                | "302010175"           | "" |
| "3"   | "22uF"          | "CAP_POL1206"                   | "EIA3216"   | "C2, C4, C6"        | "Capacitor Polarized" | "" |
| "3"   | "75R"           | "RESISTOR0805-RES"              | "0805"      | "R1, R2, R3"        | "Resistor"            | "" |
| "1"   | "IA171"         | "IA171"                         | "SOT23-6"   | "U$1"               | ""                    | "" |
| "1"   | "LP2985-33DBVR" | "PMIC-LP2985-33DBVR(SOT23-5)"   | "SOT-23-5"  | "VREG"              | "310030033"           | "" |

