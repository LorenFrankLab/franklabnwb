# franklabnwb

Example notebook and related code to create NWB files from ,rec and associated files assuing franklab
compatible naming system

##Instructions for initial setup and testing: 

1. Clone this repository to your home directory:

	git clone https://github.com/LorenFrankLab/franklabnwb.git

2. Install trodes export code from https://bitbucket.org/mkarlsso/trodes/downloads/ and add installed
directory to path.

3. Strongly suggested: create and activate a new conda environment:

	conda create --name rec_to_nwb python=3.7
	conda activate rec_to_nwb

4. Install the required packages for the conversion

	conda install -c conda-forge -c novelakrk rec_to_nwb

5.  Install Jupyter notebook

	pip install jupyter notebook

6. Start the notebook server from a directory below the franklabnwb directory:

	jupyter notebook

7. In the notebook, navigate to the franklabnwb/notebooks directory and open 

	franklab_nwb_generation.ipynb

8. Edit the variables in that notebook as required for your data and run all cells. See below for more
information on the animal metadata file


##Animal metadata file:

rec_to_nwb requires a metadata file for each day of recording. Details on the content of that file can
be found at https://novelaneuro.github.io/rec_to_nwb-docs/README.html#how-to-use-it

Alternatively, you can start with the franklabnwb/yaml/beans20190718_metadata.yml file as an example


