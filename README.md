# Documentor
Document DP databases
Read notes at end of Readme for browser issues.

Files
-----
Documentor.zip files
contains

DP26Y.exe	Standard DP program files
DP.SYS	
STE-MGR.COM	This creates a .{L} file from an .STR

STE-BASE.STR	This is a variation from the STE-BASE that is distributed with DP. Its purpose is to 
document a DP program from a .{L} file created by the STE-MGR.com  There are some panel changes 
to the original release, plus a report to export the definition to an XML file, (it outputs it as STE.XML)

STE-Def.xsl	This is the stylesheet to transform the STE.xml to a readable form using a web browser 
such as Firefox or Chrome. 

STE-js	This is the Javascript to enable interactivity in the transformed XML

wz_tooltip.js to use tooltip when displaying all field  tooltips

Use:
---
-              Unzip the Documentor.zip file into a folder, I use a different folder for each documenting project
-              
-              Copy the .STR file you wish to document into the same folder

-              If you are using Win  64-bit then place it in a file accessible to VDOS, and configure VDOS to put you to DOS command prompt (rather than to run the DPTest program)

-              Open a command window (VDOS or native as the case may be)

-              Run the STE-MGR.com program and select the STR file you wish to document.

-              This will create an .{L} file of the same base name as the STR file you are documenting

-              Start DP, and select the STR-BASE  DP program.

-              Using Shift-F9 Import  choose 8- Import Transaction Log and supply it the filename of the .{L} file previously created

-              Go to the STE-BASE.HDR panel, and then access the Reports menu (Shift-F7) and run the report “XML Database Descriptor “
               This will create a file STE.xml 

-              Exit DP, and exit VDOS

-              Open the STE.xml from the same folder as the STE.js and wz_tooltip.js 

Note:
This was written many years ago and since then both Firefox and Chrome have added security features so that local files can't open other 
files. You can allow both to do this with some changes, but since it has been identified as a security risk I would only do this while you
are open the documentor XML file.

In the case of Chrome add a start up switch to the Chrome Command Line. --allow-file-access-from-files
as in  "C:\Program Files (x86)\Google\Chrome\Application\chrome.exe" --allow-file-access-from-files

For Firefox change the config option privacy.file_unique_origin to false
open the URL about:config accepting all the warnings
search for privacy.file_unique_origin
Double click it to change it from true to false

Older version of Internet Explorer will also work

There is a sample file EXAMPLE.XML to see the results of an old DP application I wrote.

