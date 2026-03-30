# PC-Retro-MTM
Modern KiCad version of the IBM 5150 system board originally created by MTM Scientific, Inc.

Buy the original board (not from these files, not affiliated) [here](http://www.mtmscientific.com/pc-retro.html)

VCF [discussion](https://forum.vcfed.org/index.php?threads/pc-retro-design-files-ibm-5150-clone.1247940/)

## Notes
mmruzek @ VCF was very kind to open-source the design files of his IBM 5150 system board clone. The project was from 2012 or so, and not immediately usable in later KiCad versions. I converted it to KiCad 9 and did enough clean-up and repair to get forward and backward annotation working without issue, along with some small edits listed below. I have not fabricated these files. Use at your own risk.

## Changes
- Fixed skewed edge cuts outline
- Silkscreen formatting to more closely match the style of the original IBM board, along with some assembly and operation hints
- Capacitor footprints to help assembly and improve component flexibility/availability
- Removed dangling traces and vias
- Added missing decoupling capacitor around RAM
- Changed keyboard power decoupling capacitor value
- Added keyboard clock line capacitor
- Added jumper for RESERVED ISA bus connection
  

## BOM
