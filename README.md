# franklabnwb

Example notebook and related code to create NWB files from trodes .rec and associated files assuming franklab
compatible naming system

## Instructions for initial setup and testing: 

### Prerequisites

- [Download](https://bitbucket.org/mkarlsso/trodes/downloads/) and install Trodes export code, and add installed directory to path.

    - NOTE: v1.9.* seems to have an issue in mda file export (tested on Linux as of 10/4/2020). Install v1.8.2 instead.

    - If you accepted the default location suggested by the graphical installer, you can add this line to your `~/.bashrc`:
        
        ```
        PATH="${HOME}/SpikeGadgets:$PATH"
        ```
        
        Change accordingly if you chose a different location.



### Setting up a python environment

1. Clone this repository to your code source directory:
    
    ```
    cd your_source_directory
    git clone https://github.com/LorenFrankLab/franklabnwb.git
    git clone https://github.com/LorenFrankLab/rec_to_nwb.git
    ```

2. Create the conda environment required for the conversion

    ```
    cd rec_to_nwb/rec_to_nwb
    conda env create -f environment.yml
    ```

3. Start the notebook server from a directory below the franklabnwb directory:

    ```
    jupyter notebook
    ```

4. In the notebook, navigate to the `franklabnwb/notebooks` directory and open
    `franklab_nwb_generation.ipynb`.

5. Edit the variables in that notebook as required for your data and run all cells. See below for more
information on the animal metadata file.


## Animal metadata file:

`rec_to_nwb` requires a metadata file for each day of recording. Details on the content of that file can
be found in the
[documentation](https://novelaneuro.github.io/rec_to_nwb-docs/README.html#how-to-use-it).

Alternatively, you can start with the [franklabnwb/yaml/beans20190718_metadata.yml](yaml/beans20190718_metadata.yml) file as an example.
