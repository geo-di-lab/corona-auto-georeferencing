# corona-auto-georeferencing
This is a python project with the goal of establishing a reliable end to end workflow for taking distorted corona imagery and making it usable for the real world.

This project will be split up into folders containing different parts of the workflow, which correspond to different python enviroments and goals:
 - coordinate_matching: Goal is to vaguely match corona and NAIP imagery in order to utilize LightGlue to match points of images. Creates CSV for agisoft_automation
 - agisoft_automation: Takes in a CSV with points and should properly georeference the corona image utilizing Agisofts API
> The reason for this workflow is for two reasons, first at the time of writing I have only gotten both projects to work with different python versions: lightglue works for the latest version of python, while Agisofts API is up to version 3.11.
> 
> Second, These two aspects are entirely independent of each other, and I felt that it would improve readability.

## Setup
Due to the conflicting python versions, a tool known as `uv` is utilized to manage both virtual environments effciently
In order to utilize uv, I recommend installing uv globally with the standalone installer, found at the following link https://docs.astral.sh/uv/getting-started/installation/.
once uv is installed, open your terminal and cd to project directory and run 'uv sync'. This will handle installing a .venv with the correct version of python
and the correct packages and dependencies. From there you can either use 'uv run XXXXX.py' to run python scripts, or you can add the python installation 
to to your IDE as a local interpreter to use it within the IDE seamlessly.
>Note: If agisoft automation fails to download the agisoft api, you can use the the manual installation of the agisoft api.
> The link to the api can be found here: https://www.agisoft.com/downloads/installer/. 
> Go to the python 3 module section, download the .whl, and then move it to agisoft_automation folder and then use uv add path/to/whl/
