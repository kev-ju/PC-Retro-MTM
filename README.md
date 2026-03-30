# PC-Retro-MTM
Modern KiCad version of the IBM 5150 system board clone originally created by MTM Scientific, Inc.

Buy the original board (not from these files, not affiliated) [here](http://www.mtmscientific.com/pc-retro.html)

VCF [discussion](https://forum.vcfed.org/index.php?threads/pc-retro-design-files-ibm-5150-clone.1247940/)

## Notes
mmruzek @ VCF was very kind to open-source the design files of his IBM 5150 system board clone. The project was from 2012 or so, and not immediately usable in later KiCad versions. I converted it to KiCad 9 and did enough clean-up and repair to get forward and backward annotation working without issue, along with some small edits listed below. I have not fabricated these files. Use at your own risk.

## Changes
- Fixed skewed edge cuts outline
- Silkscreen formatting to more closely match the style of the original IBM board, along with some assembly and operation hints
- Re-annotated the capacitors so that they have unique references
- Capacitor footprints to help assembly and improve component flexibility/availability
- Removed dangling traces and vias
- Added missing decoupling capacitor around RAM
- Changed keyboard power decoupling capacitor value
- Added keyboard clock line capacitor
- Added jumper for RESERVED ISA bus connection
- Updated 3D models
  

## BOM
|Reference|Value|Qty|Link|
|--------------------|------------|----|------------------------------------------------------------------|
|C2, C3, C6, C12, C13, C14, C17, C23, C25, C38, C40, C42, C44|10u|13||
|C4, C10, C16, C18, C19, C20, C21, C22, C24, C26, C27, C28, C29, C30, C31, C32, C33, C34, C35, C36, C37, C39, C41, C43, C45|.047u|25||
|C5, C9|.01u|2||
|C7, C11, C15|47p|3||
|C8|.047u|1||
|D1|TYPE FC|1||
|J1, J2, J3, J4, J5|I/O_CONNECTOR|5||
|J6|CASSETTE|1||
|J7|KBD|1||
|J8|+RUN|1||
|JP1|Jumper_2_Open|1||
|K1|DIP_RELAY|1||
|P1, P2|POWER_CON|2||
|P3|CONN_4|1||
|P4|4_PIN_BERG_2X2_STRIP|1||
|R1, R3, R4, R5|18K|4||
|R2|1MEG|1||
|R6|150|1||
|R7|1200|1||
|R8|4.7K|1||
|R9|3.9K|1||
|R10|33|1||
|R11|180|1||
|R12|220|1||
|R13, R14, R15, R16, R17, R18, R19, R20, R21|27|9||
|R22, R25|510|2||
|R23|30 OHM|1||
|RN1, RN3|4.7k|2||
|RN2|8.2K|1||
|RN4|30 OHM|1||
|SW1, SW2|DIP_SW8|2||
|TD1|125n|1||
|TD2|7ns|1||
|U1|MC1741|1||
|U2|8259A|1||
|U3|8088|1||
|U4|8087 SOCKET|1||
|U5|74LS30|1||
|U6|8288|1||
|U7, U9, U10, U18|74LS373|4||
|U8, U12, U13, U14|74LS245|4||
|U11|8284A|1||
|U15, U16, U17, U23|74LS244|4||
|U19|LS670|1||
|U24|74LS322|1||
|U26, U98|74LS175|2||
|U27, U50|74LS02|2||
|U28, U29, U30, U31, U32, U33|8K_X_8ROS|6||
|U34|8253-5|1||
|U35|8237A|1||
|U36|8255A-5|1||
|U37, U38, U39, U40, U41, U42, U43, U44, U45, U53, U54, U55, U56, U57, U58, U59, U60, U61, U69, U70, U71, U72, U73, U74, U75, U76, U77, U85, U86, U87, U88, U89, U90, U91, U92, U93|RAM_64K_X_1|36||
|U46, U47, U48, U65, U66|74LS138|5||
|U49, U97|74LS08|2||
|U51, U83, U99|74LS04|3||
|U52, U81|74LS00|2||
|U62, U79|74LS158|2||
|U63|74LS38|1||
|U64|74LS20|1||
|U67, U82, U96|74LS74|3||
|U80|74LS125|1||
|U84|74LS10|1||
|U94|74LS280|1||
|U95|75477|1||
|U101|74LS32|1||
|VC1|5-30|1||
|Y1|14.31818|1||
