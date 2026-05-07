# corona-auto-georeferencing
This is a python project with the goal of establishing a reliable end to end workflow for taking distorted corona imagery and making it usable for the real world.

This project will be split up into folders containing different parts of the workflow, which correspond to different python enviroments and goals:
 - coordinate_matching: Goal is to vaguely match corona and NAIP imagery in order to utilize LightGlue to match points of images. Creates CSV for agisoft_automation
 - agisoft_automation: Takes in a CSV with points and should properly georeference the corona image utilizing Agisofts API
> The reason for this workflow is for two reasons, first at the time of writing I have only gotten both projects to work with different python versions: lightglue works for the latest version of python, while Agisofts API is up to version 3.11.
> 
> Second, These two aspects are entirely independent of each other, and I felt that it would improve readability.
