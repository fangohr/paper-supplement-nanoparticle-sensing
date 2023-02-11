# Frequency-based nanoparticle sensing over large field ranges using the ferromagnetic resonances of a magnetic nanodisc: supplementary material

[![MIT license](https://img.shields.io/badge/license-MIT-blue.svg?style=flat-square)](https://raw.githubusercontent.com/fangohr/paper-supplement-nanoparticle-sensing/master/LICENSE)
[![Binder](http://mybinder.org/badge.svg)](http://mybinder.org/repo/fangohr/paper-supplement-nanoparticle-sensing)
[![rerun-notebooks](https://github.com/fangohr/paper-supplement-nanoparticle-sensing/actions/workflows/rerun-notebooks.yaml/badge.svg)](https://github.com/fangohr/paper-supplement-nanoparticle-sensing/actions/workflows/rerun-notebooks.yaml)
[![Corresponding publication](https://img.shields.io/badge/Publication-URL-orange.svg?style=flat-square)](https://iopscience.iop.org/article/10.1088/0957-4484/27/45/455502)

This repository accompanies the paper 
[https://iopscience.iop.org/article/10.1088/0957-4484/27/45/455502](Frequency-based nanoparticle sensing over large field ranges using the ferromagnetic resonances of a magnetic nanodisc).
It provides the data underlying the figures in the paper as well as Jupyter notebooks to reproduce those figures.
The latest version of this repository can be found at https://github.com/fangohr/paper-supplement-nanoparticle-sensing

----------

**Authors:**
Maximilian Albert, Marijan Beg, Dmitri Chernyshenko, Marc-Antonio Bisotti, Rebecca L. Carey, Hans Fangohr and Peter Metaxas.


## Contents

The directory `notebooks/` contains Jupyter notebooks for the relevant figures in the paper.
On Github you can view them directly in the browser:

- [Fig. 2: Dipole field visualisation](./notebooks/fig_2_dipole_field_visualisation.ipynb)
- [Fig. 4: Frequency dependence on external field strength](./notebooks/fig_4_frequency_dependence_on_external_field.ipynb)
- [Fig. 7: Frequency change vs. lateral particle position](./notebooks/fig_7_frequency_change_vs_lateral_particle_position.ipynb)
- [Fig. 8: Frequency change vs. particle-disc separation](./notebooks/fig_8_frequency_change_vs_particle_separation.ipynb)
- [Fig. 9(a): Frequency change vs. particle M_S](./notebooks/fig_9a_dependence_of_frequency_change_on_particle_Ms.ipynb)
- [Fig. 9(b): Frequency change vs. particle size](./notebooks/fig_9b_dependence_of_frequency_change_on_particle_size.ipynb)
- [Fig. 9(c): Frequency change for the fundamental mode for various external field strengths](./notebooks/fig_9c_comparison_of_frequency_change_for_various_external_field_strengths.ipynb)

The raw data is available in the file [data/eigenmode_info_data_frame.csv](./data/eigenmode_info_data_frame.csv), which is a CSV (= comma-separated values) file containing the simulation parameters and computed resonant frequencies for all performed simulations. All notebooks use this data to generate the figures.
The data format is explained in the notebook [Explanation of the data format](./notebooks/explanation_of_the_data_format.ipynb).


## Executing the notebooks

### Using a cloud Jupyter server via Binder (no installation required)

The easiest way to execute the notebooks without installing anything
is to launch a cloud Jupyter server using [Binder](http://mybinder.org/).
You can access it here:

http://mybinder.org/repo/fangohr/paper-supplement-nanoparticle-sensing

### Running the notebooks locally on your machine

In order to run the notebooks on your own computer, follow the steps below.

1. Clone this repository and change into the newly created directory:
   ```
   git clone https://github.com/fangohr/paper-supplement-nanoparticle-sensing.git
   cd paper-supplement-nanoparticle-sensing
   ```

2. Install all required dependencies. Tested for Python 3.9 to Python 3.11. First, create a virtual environment (or conda environment if you prefer):
   ```shell
   python -m venv venv-paper
   source venv-paper/bin/activate
   ```
   Then install the required libraries:
   ```shell
   pip install -r requirements.txt
   ```
   
3. Start a notebook server:
   ```shell
   jupyter notebook
   ```
   This will open a browser window with a dashboard showing the contents of this repository.

4. Navigate to the `notebooks/` folder and open any of the `.ipynb` files. You can reproduce 
   the associated figure by selecting the menu item `Cell -> Run All`.


## Changes

- [11 February 2023](https://github.com/fangohr/paper-supplement-nanoparticle-sensing/pull/2): 
  changed from conda-environment to requirements.txt, added
  CI, updated notebooks to execute with latest matplotlib.
