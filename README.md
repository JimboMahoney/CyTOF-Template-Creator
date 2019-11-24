# CyTOF-Panel-Creator
A web-based (Shiny) [interface](https://jimbomahoney.shinyapps.io/shiny/) to create CyTOF .tem files.

This allows (hopefully) easy creation of .tem files, which can then be loaded onto a CyTOF system for acquisition.

The motivation for this was:

- It seems unnecessary to download and install (CyTOF) software on an offline system to create an acquisition template.
- Creating a template at the machine (based on an e-mail or Excel file from a user) is risky unless the user is present to verify.
- There is no error-checking in the CyTOF software (e.g. it's easy to miss essential channels, such as EQ beads).
- Just for fun! It's the first time I've built and uploaded a Shiny app.

Currently, it performs the following:

Checks to ensure that:

- All essential normalisation channels are present.
- Illegal characters are not present in the Target names. (This is a limitation imposed by CyTOF software).
- Cell ID (Ir / Rh) is present.

Provides the following functionality:

- Default template containing common contaminants, barcodes and Cell ID (Live/Dead, Ir).
- Upload template from Excel file (file must have headers for columns and mass/element in first column; target/markers in second column).
- Easy Add/Remove of Barcodes, Bead (EQ), Contaminants and Blank (M +/- 1) channels.
- Lookup of isotope by mass or name.
- Sorting of Panel by mass or name.
- Save as .tem file ready for use on CyTOF.

Tested on CyTOF software version 6.7.1014, using default Event mode parameters.

<br>

[![Foo](https://raw.githubusercontent.com/JimboMahoney/CyTOF-Panel-Creator/master/2019_11_22_14_12_17_CyTOF_Template_Creator.png)](https://jimbomahoney.shinyapps.io/shiny/)


