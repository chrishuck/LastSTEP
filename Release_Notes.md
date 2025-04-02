## v2025.03.31 RELEASE NOTES:

### NEW FEATURES:

_ResetPlacement Before Export:_

This version adds functionality to allow the user to perform a ResetPlacement function on each body during the batch export. This function comes from the kicadStepUp workbench, which much be installed for usage of this functionality. This function resets the origin of each body to the origin of the file in which it's contained. 

A checkbox has been added to the file naming scheme selection dialog box that allows the user to choose the ResetPlacement functionality prior to choosing a file naming scheme.

If the kicadStepUp workbench is not installed and the user chooses the ResetPlacement option, an error message will be displayed in the Python Report View for each body, but the body will be exported as before based on the chosen file naming scheme.

This feature was requested by Mastodon user: [@amd@gts.amd.im](https://gts.amd.im/@amd)
