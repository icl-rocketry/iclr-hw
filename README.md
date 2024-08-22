# ICLR KiCad Hardware Libraries
This repository contains custom symbol, footprint and 3d model libraries for components that are not included in the default KiCad library.

## Using this library
The first step to using this library is to clone this repository using your git client of choice. Our recommendation is to make an ICLR somewhere on your computer where it is not backed up to onedrive - this is because some tools used in designing do not work when there is a whitespace in the path name!

### Environment variable
For this library to properly associate footprints to their 3D models, the location the library is cloned in must be added as an environment variables called ```ICLR_HW```. This can be done in ```KiCad -> Preferences -> Configure Paths...```, and once done it should look similar to the following:

![envvar example](docs/example_env_var.png)

### Symbol library
A KiCad symbol libraries is stored in a single file with the extension ```.kicad_sym```. This library can be added as a global KiCad library in ```KiCad -> Preferences -> Manage Symbol Libraries```. From here, add a library and select it by navigating to the cloned iclr-hw folder, then to ```syms``` and select ```iclr.kicad_sym```. If the environment variable step has been followed, this should then be the same as the following:

![envvar example](docs/example_sym_lib.png)

To import downloaded symbols into this library: 
- Go to the ```Kicad Symbol Editor```, scroll to the iclr library
- Scroll to the iclr library
- Right click the iclr library
- Click ```Import Symbol```
- Select the new symbol's ```.kicad_sym``` file
- Save the library

### Footprint library
A KiCad footprint library is stored in a single folder. This library can be added as a global KiCad library in ```KiCad -> Preferences -> Manage Footprint Libraries```. From here, add a library and select it by navigating to the cloned iclr-hw folder, then to ```fp``` then into ```iclr.pretty``` and click open. Like before, if the environment variable step has been followed, this should be the same as the following:

![envvar example](docs/example_fp_lib.png)

To import downloaded footprints into this library: 
- Copy the downloaded footprint's ```.kicad_mod``` file
- Navigate to ```iclr-hw/fp/iclr.pretty/```
- Paste the ```.kicad_mod``` file

### 3D model library
Each KiCad footprint has a 3D model associated with it, which can be assigned in the footprint properties. If a footprint also includes a 3D model, it can be associated to the footprint with the following steps:

- Copy the downloaded 3D model
- Paste it in ```iclr-hw/3d/```
- Open the ```KiCad Footprint Editor```
- Open the footprint the 3d model should be associated to
- Go to footprint properties (shortcut E)
- Click the ```3D Models``` tab
- Select the 3D model pasted previously
- Align the 3D model with the footprint if necessary
- Save the footprint.
