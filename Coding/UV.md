# New project

* In terminal go to the folder in which the new project should be in (e.g. ~code/projects/)

* Make a folder with the wanted `projectname`, `mkdir projectname`

* go to the project folder `cd projectname`

* type `uv init projectname`

* this creates the following files in the `projectfolder`
  
  * main.py
  
  * pyprojet.toml
  
  * README.md

* Open VsCode by typing `code` or Cursor by typing `cursor` in Terminal from the projectfolder  

# Add Python packages to the uv virtual environmen

* Type `uv add numpy`

# Add Marimo

* Type `uv add "marimo[recommended]"

# Start Marimo

* `uv run marimo edit file.py`

* `uv run marimo run file.py`




