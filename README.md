# pytiba
pytiba is an extension for [pyRevit](http://eirannejad.github.io/pyRevit/)

![pyTiBa](https://github.com/tillbaum/pytiba/blob/master/pytiba%20documentation/pdf_export/pyTiBa%20Tab.png)

## Features
### pdf_export tool
The pdf_export tool exports: 
 +   multiple Revit Sheets to pdf at the same time,  
 +   with filenames specified by sheet  parameters for each sheet, i.e. 
    „SheetNumber_Revision_SheetName_date_time“  
    (ex: “A01_b_Floorplan L00_17.06.18_11:34.pdf“ ).
 +   with papersize format automatically matching the sheetsize format
 +   Sheetview selection is made either by selecting Sheets in Project Browser before the script is run or by Sheet-Selection-Dialog. 
 
#### Sheet Selection Dialog 

<table>
<tr>
<td>
<img src="https://github.com/tillbaum/pytiba/blob/master/pytiba%20documentation/pdf_export/SheetSelectionDialog.png" alt="alt text" width="390" height="390">
</td>
<td>
<img src="https://github.com/tillbaum/pytiba/blob/master/pytiba%20documentation/pdf_export/SheetSelecDia_options.png" alt="alt text" width="390" height="390">
</td>
</tr>
</table>

#### Recommended pdfprinter
The pdfprinter must be configured. 

**Automatic Filenaming** works best with free **PDFCreator printer** (pdfforge.org). **Filenaming** and the correct **filepath output** can be specified. 

Other printers that have been tested towork: 
Adobe PDF, bullzip PDF Printer. (Filepath output can not be set in the dialog, directory has to be set in the printer options)

<img src="https://github.com/tillbaum/pytiba/blob/master/pytiba%20documentation/pdf_export/PDFCreator%20ProfileSettings.png" alt="alt text" width="720" height="480">

(PDFCreator Version 3.2.1, there is a newer version available)
It also works with older version, see http://wrw.is/using-free-pdf-printer-rtv-xporter-pro-automatic-batch-pdf-naming-revit/

Adobe PDF printer:

<img src="https://github.com/tillbaum/pytiba/blob/master/pytiba%20documentation/pdf_export/AdobePDF%20printer_filename_working_Creation_dlg.png" alt="alt text" > <!--- width="720" height="480" -->

#### Papersize-format matching Sheetformat Size
To get this function to work properly you have to add Print Forms with the right papersizeformat, to your 
Print Management on Windows. 

<img src="https://github.com/tillbaum/pytiba/blob/master/pytiba%20documentation/pdf_export/PrintManagementForms.png" alt="alt text" width="663" height="210">
Windows Print Management Dialog


<img src="https://github.com/tillbaum/pytiba/blob/master/pytiba%20documentation/pdf_export/Add%20Print%20Forms.png" alt="alt text" width="328" height="374" > 
Print Form Dialog


If you add forms they will be available globaly to most installed pdf printers.
(You can open this dialog by typing "Print Management" in your SearchBox in the WIN10 taskbar, 
from old Win7Style Conrol Panel its ControlPanel>AdministrativeTools>PrintManagement)

The new forms must be named **"width[cm]xheight[cm]"**, "118.9x84.1" (A0 format), "42.0x29.7" (A3 format). only one position after the decimal point is allowed. Or "90x65", "125x85", without any decimal point, in a raster of 5.

** work in progress **

#### FAQ / Errors 
+ PDFCreator switches Page Orientation/ Automatic page orientation doesn't seem to work. --> Set Page Orientation Setting manually from  Automatic to Landscape. 
In Revit !temp PrintSetting set Page Orientation to Portrai, its the default setting to assure matchPaperSizeFunc finds the right Print Form.

**(work in progress)**


# Credits
Credits and a thank you go to the following: 
+ Ehsan Iran-Najad for providing [PyRevit](https://github.com/eirannejad/pyRevit), the amazing IronPython Script Library / Environment for Revit.
+ Gui Talariko, creator of [RevitPythonWrapper](https://revitpythonwrapper.readthedocs.io/en/latest/)
+ Daren Thomas, creator of [RevitPythonShell](https://github.com/architecture-building-systems/revitpythonshell)
+ Jeremy Tammik, creator of [RevitLookup](https://github.com/jeremytammik/RevitLookup)
+ Icon8 for nice Icons

# License
This package is licensed under GNU GENERAL PUBLIC LICENSE, Version 3, 29 June 2007.




