# transition-scenarios

## Input Folder
The input folder is to generate various input files for transition scenario
simulations. Currently it has files that generate PWR input files with 
different capacities. The assumptions for the parameters are as follows:

	Cycle 			= 18 months (timesteps) for all
	Refueling 		= 2 months (timesteps) for all
	assembly mass 	= 523.4 UO2 / assembly for all (PWR, nucleartourist.com)
	#of assemblies 	= 193 for 1000MWe, linearly adjusted for other capacities



### write_reactors.py
Python script for input file generation.

Uses csv file to generate input files from the template.

Creates (or appends to) a file called written_input_file.xml as a result.


To run:

	python write_reactors.py [csv_file] [template_file]


### france.csv
Lists all the operating reactors in France by 

[name],[num_assemblies_core],[num_assemblies_batch]

For cyclus input file.


### template.xml
Template for the cyclus input file in xml.

This will work with jinja2 and create reator agent

Input files for cyclus, when write_reactors.py is run.


### written_input_file.xml
This is an exmpale input file generated by write_reactors.py.

Make sure to delete this prior to running write_reactors.py.

