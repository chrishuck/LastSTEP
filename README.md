# LastSTEP

A FreeCAD macro to batch export multiple bodies to individual STEP files.

[Release Notes](https://github.com/chrishuck/LastSTEP/blob/main/Release_Notes.md)

## Description:

This is a macro to batch export STEP files of bodies from any FreeCAD file.
Individual STEP files are created, in a user-selected folder, for each body 
with the filename based on a user-selected naming scheme:

By Body Name: Matches the Label property of the body.
(i.e. If the body is named "MyBody", the exported STEP file will be "MyBody.step")

Sequential Numbers: (i.e. "1.step", "2.step", etc...)

I decided to call it LastSTEP because it would likely be the the last step before publishing CAD
files to an online model sharing service.

IMPORTANT: Body names CANNOT contain a '/' because it is interpreted as part of the file path.
Consider a different character in your body names (This is the 'Label' property of the object) 

If no bodies are selected when the macro is run, an error dialog will appear.

## Installation:

Place the LastSTEP.FCMacro in your chosen FreeCAD macros folder. To use the ResetPlacement feature, the kicadStepUp workbench must also be installed.

## Usage

1. Pre-select a body, or bodies, you would like to export.
2. Run the macro.
3. A dialog box will appear asking you to select the folder to export the files into. Make a selection.
4. A dialog box will appear asking you to select the file naming scheme to use. 

    a. If ResetPlacement of the body(s) is desired, click the checkbox prior to choosing a file naming scheme.

    b. Choose a file naming scheme.

5. The STEP files will be exported to the chosen folder with file names based on the chosen naming scheme. If ResetPlacement was chosen, the body origin will be set to the origin of the parent file in which it's contained.

## Credit

This macro is based on code from a great blog post and video from MangoJelly Solutions about batch
exporting FreeCAD bodies into individual STEP files. The code in the blog post outputs the filenames as 
sequential numbers. I wanted the macro to use the name of the body as the filename. So, I tweaked
the code in the blog post to add that functionality, but make the naming scheme user-selectable.
I also added an error dialog if the user forgot to select any bodies prior to running the macro.

Blog post: [Export Multiple Selected to Multiple STEP Files in One Go - FreeCAD Macro
](https://mangojellysolutions.blogspot.com/2023/09/export-multiple-selected-to-multiple.html)

YouTube video: [FreeCAD: Export multiple Selected Objects / Parts to Individual Files in One Go
](https://www.youtube.com/watch?v=IapVaYQWN2M)
