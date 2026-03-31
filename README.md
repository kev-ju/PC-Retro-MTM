 ![PC-Retro-MTM](/64_256KB_SYSTEM_BOARD.png)

# PC-Retro-MTM
Modern KiCad version of the IBM 5150 system board clone originally created by MTM Scientific, Inc.

Buy the original board (not from these files, not affiliated) [here](http://www.mtmscientific.com/pc-retro.html)

VCF [discussion](https://forum.vcfed.org/index.php?threads/pc-retro-design-files-ibm-5150-clone.1247940/)

## Notes
mmruzek @ VCF was very kind to open-source the design files of his IBM 5150 system board clone. The project used a version of KiCad from 2012 or so, and was not immediately usable in later KiCad versions. I converted it to KiCad 9 and did enough clean-up and repair to get forward and backward annotation working without issue, along with some small edits listed below. I have not fabricated these files. Use at your own risk.

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
I added a BOM into the KiCad schematic featuring only US-based retailers where possible. I have not verified these parts, use at your own risk. It may be cheaper to buy the TTL parts direct from [ti.com](https://ti.com). Do not buy the TTL parts from China, most will be relabeled HC. 

If TD1 had its original DIP-14 footprint restored, the [DS1000-125](https://www.questcomp.com/part/4/ds1000-125/177327912) could be used.

PROMS that work with the 5150 are not common. An adapter can be used as described at [MZD](https://www.minuszerodegrees.net/5150/motherboard/IBM%205150%20motherboard%20-%20Substituting%20the%20U33%20BIOS%20ROM.htm), or U28 could possibly be changed to a 27C512 or equivalent by using A13-A15 from the ISA slots and connecting ROM_ADDR_SEL to CE and XMEMR to OE.


| # | Reference | Value | Qty | Link | Note |
|---|-----------|-------|-----|---|---|
| 1 | C2, C3, C6, C12, C13, C14, C17, C23, C25, C38, C40, C42, C44 | 10u | 13 | https://www.digikey.com/en/products/detail/kyocera-avx/TAP106K025SRS/11202552 | |
| 2 | C4, C10, C16, C18, C19, C20, C21, C22, C24, C26, C27, C28, C29, C30, C31, C32, C33, C34, C35, C36, C37, C39, C41, C43, C45 | .047u | 25 | https://www.digikey.com/en/products/detail/vishay-beyschlag-draloric-bc-components/K104K10X7RF5UH5/2356754 | No reason not to use 100n here |
| 3 | C5, C9 | .01u | 2 | https://www.digikey.com/en/products/detail/vishay-beyschlag-draloric-bc-components/MKT1813310405/5378151 | |
| 4 | C7, C11, C15 | 47p | 3 | https://www.digikey.com/en/products/detail/vishay-beyschlag-draloric-bc-components/K470J15C0GF5TH5/286492 | |
| 5 | C8 | .047u | 1 | https://www.digikey.com/en/products/detail/cornell-dubilier-knowles/150473K250BB/2538235 | |
| 6 | D1 | TYPE FC | 1 | https://www.digikey.com/en/products/detail/onsemi/1N4148/458603 | |
| 7 | J1, J2, J3, J4, J5 | I/O_CONNECTOR | 5 | https://www.digikey.com/en/products/detail/edac-inc/395-062-520-350/210777 | |
| 8 | J6 | CASSETTE | 1 | https://www.digikey.com/en/products/detail/kycon-inc/KCDX-5S-N/10246509 | |
| 9 | J7 | KBD | 1 | https://www.digikey.com/en/products/detail/kycon-inc/KCDX-5S-N/10246509 | |
| 12 | K1 | DIP_RELAY | 1 | https://www.digikey.com/en/products/detail/omron-electronics-inc-emc-div/G5V-2-DC5/87819 | |
| 13 | P1, P2 | POWER_CON | 2 | https://www.digikey.com/en/products/detail/molex/0366420001/4143772 | It's black instead of white, but it's the right shape. |
| 14 | P3 | 1x4 | 1 | https://www.digikey.com/en/products/detail/adam-tech/PH1RB-04-UA/9830473 | |
| 15 | P4 | 2x2 | 1 | https://www.digikey.com/en/products/detail/adam-tech/PH2-04-UA/9830324 | |
| 16 | R1, R3, R4, R5 | 18K | 4 | https://www.digikey.com/en/products/detail/yageo/MFR-25FTE52-18K/9139828 | |
| 17 | R2 | 1MEG | 1 | https://www.digikey.com/en/products/detail/yageo/MFR-25FTE52-1M/9139874 | |
| 18 | R6 | 150 | 1 | https://www.digikey.com/en/products/detail/yageo/MFR-25FBF52-150R/12831 | |
| 19 | R7 | 1200 | 1 | https://www.digikey.com/en/products/detail/yageo/MFR-25FBF52-1K2/9138061 | |
| 20 | R8 | 4.7K | 1 | https://www.digikey.com/en/products/detail/yageo/MFR-25FTF52-4K7/9140940 | |
| 21 | R9 | 3.9K | 1 | https://www.digikey.com/en/products/detail/yageo/MFR-25FTE52-3K9/9140156 | |
| 22 | R10 | 33 1/2W | 1 | https://www.digikey.com/en/products/detail/yageo/MFR50SFTE52-33R/9151419 | 1/2 watt |
| 23 | R11 | 180 | 1 | https://www.digikey.com/en/products/detail/yageo/MFR-25FTE52-180R/9139823 | |
| 24 | R12 | 220 | 1 | https://www.digikey.com/en/products/detail/yageo/MFR-25FRF52-220R/9138942 | |
| 25 | R13, R14, R15, R16, R17, R18, R19, R20, R21 | 27 | 9 | https://www.digikey.com/en/products/detail/yageo/MFR-25FTE52-27R/9140004 | |
| 26 | R22, R25 | 510 | 2 | https://www.digikey.com/en/products/detail/yageo/MFR-25FBF52-510R/9138187 | |
| 27 | R23 | 30 OHM | 1 | https://www.digikey.com/en/products/detail/yageo/MFR-25FTE52-30R/9140087 | |
| 28 | RN1, RN3 | 4.7k | 2 | https://www.digikey.com/en/products/detail/bourns-inc/4116R-2-472LF/1088687 | |
| 29 | RN2 | 8.2K | 1 | https://www.digikey.com/en/products/detail/bourns-inc/4116R-2-472LF/1088687 | There is no reason to use 8.2k here, another 4.7k will work fine. |
| 30 | RN4 | 30 OHM | 1 | https://www.digikey.com/en/products/detail/bourns-inc/4116R-1-330LF/1088635 | 33 Ohm will work fine here |
| 31 | SW1, SW2 | DIP_SW8 | 2 | https://www.digikey.com/en/products/detail/te-connectivity-alcoswitch-switches/435640-5/42470 | |
| 32 | TD1 | 125n | 1 | https://www.questcomp.com/part/4/ds1000m-125/177328069 | https://www.questcomp.com/part/4/ds1000m-100/177328066 probably also works |
| 33 | TD2 | 7ns | 1 | https://www.digikey.com/en/products/detail/yageo/MFR-25FTE52-470R/9140223 | Use a 470 Ohm resistor here |
| 34 | U1 | MC1741 | 1 | https://www.digikey.com/en/products/detail/texas-instruments/LM741CN-NOPB/6322 | |
| 35 | U2 | 8259A | 1 | https://www.jameco.com/z/P8259A-Intel-Corporation-IC-8259-Programmable-Interrupt-Controller-DIP-28-pin_52775.html | |
| 36 | U3 | 8088 | 1 | https://www.jameco.com/z/P8088-2-Advanced-Micro-Devices-MPU-8088-CISC-8-Bit-HMOS-8MHz-40-Pin-CDIP_52169.html | |
| 37 | U4 | 8087 | 1 | https://www.questcomp.com/part/4/c8087/126791059 | |
| 38 | U5 | 74LS30 | 1 | https://www.digikey.com/en/products/detail/texas-instruments/SN74LS30N/377726 | |
| 39 | U6 | 8288 | 1 | https://www.questcomp.com/part/4/cp82c88/146639310 | |
| 40 | U7, U9, U10, U18 | 74LS373 | 4 | https://www.digikey.com/en/products/detail/texas-instruments/SN74LS373N/277306 | |
| 41 | U8, U12, U13, U14 | 74LS245 | 4 | https://www.digikey.com/en/products/detail/texas-instruments/SN74LS245N/277301 | |
| 42 | U11 | 8284A | 1 | https://www.questcomp.com/part/4/cp82c84a/146639293 | |
| 43 | U15, U16, U17, U23 | 74LS244 | 4 | https://www.digikey.com/en/products/detail/texas-instruments/SN74LS244N/277299 | |
| 44 | U19 | 74LS670 | 1 | https://www.digikey.com/en/products/detail/texas-instruments/SN74LS670N/1594880 | |
| 45 | U24 | 74LS322 | 1 | https://www.jameco.com/z/AM25LS22PC-Advanced-Micro-Devices-8-Bit-Serial-Parallel-Register-IC-with-Sign-Extend-DIP-20_2395479.html | *** Investigate replacing this |
| 46 | U26, U98 | 74LS175 | 2 | https://www.digikey.com/en/products/detail/texas-instruments/SN74LS175N/277294 | |
| 47 | U27, U50 | 74LS02 | 2 | https://www.digikey.com/en/products/detail/texas-instruments/SN74LS02N/277273 | |
| 48 | U28, U29, U30, U31, U32, U33 | 8K_X_8ROS | 6 | https://www.minuszerodegrees.net/5150/motherboard/IBM%205150%20motherboard%20-%20Substituting%20the%20U33%20BIOS%20ROM.htm | |
| 49 | U34 | 8253-5 | 1 | https://www.jameco.com/z/P8253-Intel-Corporation-Programmable-Interval-Timer-3-Independent-16-bit-Counters-2-6-MHz-DIP-24_52679.html | |
| 50 | U35 | 8237A | 1 | https://www.jameco.com/z/P8237A-5-NEC-Corporation-Multimode-DMA-Controller-4-Channel-5-MHz-DIP-40_2394975.html | |
| 51 | U36 | 8255A-5 | 1 | https://www.jameco.com/z/P8255A-5-Intel-Corporation-IC-8255A-5-Programmable-Peripheral-Interface-40-pin-DIP_52732.html | |
| 52 | U37, U38, U39, U40, U41, U42, U43, U44, U45, U53, U54, U55, U56, U57, U58, U59, U60, U61, U69, U70, U71, U72, U73, U74, U75, U76, U77, U85, U86, U87, U88, U89, U90, U91, U92 | RAM_64K_X_1 | 36 | https://www.jameco.com/z/KM4164B-12-Samsung-Electronics-IC-4164-120-NMOS-DRAM-64K-Bit-64K-x-1-120ns-w-Page-Mode_2290535.html | |
| 53 | U46, U47, U48, U66 | 74LS138 | 4 | https://www.digikey.com/en/products/detail/texas-instruments/SN74LS138N/277285 | |
| 54 | U49, U97 | 74S08 | 2 | https://www.digikey.com/en/products/detail/texas-instruments/SN74S08N/277371 | |
| 55 | U51, U83, U99 | 74LS04 | 3 | https://www.digikey.com/en/products/detail/texas-instruments/SN74LS04N/277275 | |
| 56 | U52 | 74LS00 | 1 | https://www.digikey.com/en/products/detail/texas-instruments/SN74LS00N/277272 | |
| 57 | U62, U79 | 74LS158 | 2 | https://www.digikey.com/en/products/detail/texas-instruments/SN74LS158N/1594759 | |
| 58 | U63 | 74LS38 | 1 | https://www.digikey.com/en/products/detail/texas-instruments/SN74LS38N/277310 | |
| 59 | U64 | 74LS20 | 1 | https://www.digikey.com/en/products/detail/texas-instruments/SN74LS20N/377790 | |
| 60 | U65 | 74S138 | 1 | https://www.digikey.com/en/products/detail/texas-instruments/SN74S138AN/277374 | |
| 61 | U67, U96 | 74LS74 | 2 | https://www.digikey.com/en/products/detail/texas-instruments/SN74LS74AN/277314 | |
| 62 | U80 | 74LS125 | 1 | https://www.digikey.com/en/products/detail/texas-instruments/SN74LS125AN/277284 | |
| 63 | U81 | 74S00 | 1 | https://www.digikey.com/en/products/detail/texas-instruments/SN74S00N/277369 | |
| 64 | U82 | 74S74 | 1 | https://www.digikey.com/en/products/detail/texas-instruments/SN74S74N/277380 | |
| 65 | U84 | 74S10 | 1 | https://www.mouser.com/ProductDetail/Texas-Instruments/SN74S10N?qs=dT9u2OTAaVW2XijXSK8i5w%3D%3D | |
| 66 | U94 | 74S280 | 1 | https://www.jameco.com/z/DM74S280N-National-Semiconductor-9-Bit-Parity-Generator-Checker-IC-DIP-14_48688.html | *** Investigate replacing this |
| 67 | U95 | 75477 | 1 | https://www.digikey.com/en/products/detail/texas-instruments/SN75477P/380178 | |
| 68 | U101 | 74LS32 | 1 | https://www.digikey.com/en/products/detail/texas-instruments/SN74LS32N/277304 | |
| 69 | VC1 | 5-30 | 1 | https://www.digikey.com/en/products/detail/ew-electronics/GKG30015/11689271 | Bend the leads a bit to fit across pins 1 and 2. |
| 70 | Y1 | 14.31818 | 1 | https://www.digikey.com/en/products/detail/cts-frequency-controls/MP143/67739 | |
