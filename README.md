# deepchem-for-dummies
My experiences as a chemist for installing and using deepchem


As a medicinal chemist interested in deep learning and trying to understand new tools to increase productivity I was very interested when I saw the [blogpost by Derek Lowe](https://blogs.sciencemag.org/pipeline/archives/2019/05/14/an-intro-to-deep-learning) on his in the pipeline blog  about [Deepchem](https://deepchem.io/). Since I am not a programmer I was a bit overwhelmed when I tried to use the tool and was originally unable to get any of the tutorials to work. After a little bit of experience I have been at least able to get the tutorials to work. 

Here I plan on documenting first the installation of Deepchem and the required dependencies then as I get more familiar with the software I plan on documenting a how to use deepchem for dummies.

## Installation

  * Install a working version of Linux
    * I used [Linux Mint](https://linuxmint.com/) installed on Hyper-V on a Windows 10 computer at work. It would work even better on a native Linux box. Since Mint is a fork of Ubuntu/Debain I will use those commands
  * Install [Miniconda](https://docs.conda.io/en/latest/miniconda.html) - I used miniconda so I could control which packages/dependencies I install
    * download the installer, then navigate to the ~/Downloads folder in the terminal
    * bash Miniconda3-latest-Linux-x86_64.sh
  * Install git and download the deepchem repository - I built from the repository for 2 reasons. 1) it worked 2) so I would have the notebooks
    * from your home directory in terminal
    * $ sudo apt install git
    * $ git clone https://github.com/deepchem/deepchem.git
  * Install [Deepchem](https://github.com/deepchem/deepchem) in a conda environment called deepchem
    * $ cd deepchem
    * $ bash scripts/install_deepchem_conda.sh deepchem
    * $ conda activate deepchem
    * $ python setup.py install
  * Install the required dependencies and Jupyter notebook - I used conda then updated/upgrades with pip. Make sure you are within your deepchem environment
    * $ conda install numpy, pandas, joblib, scikit-learn, tensorflow, matplotlib
    * $ conda install -c conda-forge rdkit
    * $ pip install --upgrade tensorflow
    * $ conda install jupyter
  * You should now have all of the required libraries to use deepchem - open the jupyter notebook and navigate to the deepchem notebooks
    * $ jupyter notebook
    
