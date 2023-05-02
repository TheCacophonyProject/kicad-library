# kicad-library
Cacophony kicad library of 3D models, footprints, and symbols.

## Adding Libraries to Project
- Clone/download git repo.
- Add new environment variable:
    - `Preferences` -> `Configure Paths...`
    - Add new variable with Name=`CAC_KICAD_LIBRARY` and Path=`<path to git repo>`
- Add Symbol library:
    - `Preferences` -> `Manage Symbol Libraries...`
    - Add to Global or Project depending on what you want.
    - Add new library with nickname=`cacophony-library` Path=`${CAC_KICAD_LIBRARY}/cacophony-library.kicad_sym`

- Add Footprint library:
    - `Preferences` -> `Manage Footprint Libraries...`
    - Add to Global or Project depending on what you want.
    - Add new library with nickname=`cacophony-library` Path=`${CAC_KICAD_LIBRARY}/cacophony-library.pretty`

## Adding new parts with eadyeda2kicad
- Install easyeda2kicad https://github.com/uPesy/easyeda2kicad.py
- `cd <path to kicad-library>`
- `easyeda2kicad --full --output ./cacophony-library --lcsc_id <id>`
- To make the footprint link to the 3D model you will need to add `${CAC_KICAD_LIBRARY}` to the start of the 3D model path in the footprint.

## Adding a module to your project
These kicad modules are parts that I have used multiple times in different projects. They contain the schematics and the layout of the footprints.

- With your kicad project open, open the module in a different kicad instance.
- 