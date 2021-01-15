# Neural Data Transformers

This is the code for the paper "". We provide the code as reference, but we are unable to help debug specific issues e.g. in using the model, at this time.

## Setup
We recommend you set up your code environment with `conda/miniconda`.
The dependencies necessary for this project can then be installed with:
    `conda env create -f environment.yml`
This project was developed with Python 3.6.

## Data
The autonomous chaotic RNN dataset can be generated by running `./data/gen_synth_data_no_inputs.sh`. The maze dataset and lorenz dataset are unavailable at this time.

## Training + Evaluation
Experimental configurations are set in `./configs/`. To train a single model with a configuration `./configs/<variant_name>.yaml`, run `./scripts/train.sh <variant_name>`.

The provided sample configurations in `./configs/arxiv/` were used in the HP sweeps for the main results in the paper, with the sweep parameters in `./configs/*json`. Note that sweeping is done with the `ray[tune]` package. To run a sweep, run `python ray_random.py -e <variant_name>` (the same config system is used).

R2 is reported automatically for synthetic datasets. Maze analyses + configurations are unfortunately unavailable at this time.

## Analysis
Reference scripts that were used to produce most figures are available in `scripts`. They were created and iterated on as VSCode ntoebooks. They may require external information, run directories, even codebases etc. Scripts are provided to give a sense of analysis procedure, not to use as an out-of-the-box reproducibility notebook.

## Citation
