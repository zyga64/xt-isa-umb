### Simple UMB memory expansion for IBM PC (XT) and clones.

With this card, you can add 128 kB of continuous UMB memory in the D0000 - EFFFF area, or only 64 kB in the D0000 - DFFFF or E0000 - EFFFF areas. 

* Original schematic diagram was drawn by Ruud Baltissen (VCF forum thread): https://forum.vcfed.org/index.php?threads/loading-dos-high-on-a-xt.32320/
* The idea for the printed circuit board layout borrowed from Adrian Black: https://github.com/misterblack1/isa-ram-expansion
* 8 bit ISA footprint from Sergey Kiselev: https://github.com/skiselev/my_kicad_library

Diagram/PCB drawn by me in KiCad 9.0, the only minor change from Ruud's schematic is the addition of a 74LS245 buffer for the data bus (as done by Adrian and in the Lo-tech 1MB RAM Board https://www.lo-tech.co.uk/wiki/Lo-tech_1MB_RAM_Board).
![picture of working prototype](images/prototype.jpg)

![3d view of PCB](images/3d_view.png)

## Bill Of Materials

Reference      | Quantity    | Value                    
---------------|-------------|--------------------------
U1             | 1           | 74HCT138                  
U2             | 1           | 74HCT08                   
U3             | 1           | AS6C1008 (or another compatible 128k x 8bit SRAM)
U4             | 1           | 74HCT245                  
C6             | 1           | 47uF /16V                 
C1, C2, C3, C4 | 4           | 100nF                     
JP1, JP2       | 2           | 1x02 male through-hole pin-header 2.54mm
R1, R2         | 2           | 15k / 0.125W   (pull-up resistors - 10k will also be fine)

