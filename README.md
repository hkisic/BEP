# BEP
# AdExIF_Model_LFP.ipynb

This Jupyter Notebook implements and analyzes a spiking neural network model based on the Adaptive Exponential Integrate-and-Fire (AdExIF) neuron. It simulates different network connectivity profiles and computes local field potentials (LFPs) using the Brian2 simulator. The notebook is designed for computational neuroscience research, particularly for exploring how developmental changes in neural connectivity affect network dynamics and extracellular signals.

## Features

- Simulation of neural networks (excitatory and inhibitory populations) using the AdExIF model.
- Multiple connectivity profiles: Control, Linear Mutant, and Parabolic Mutant.
- Calculation and storage of LFPs from virtual electrode arrays.
- Parameter sweeps for developmental and mutant scenarios.
- Organized saving of simulation results and connectivity data.
- Visualization tools for analyzing connectivity and network behavior.

## Table of Contents

1. [Neuron Network Model](#neuron-network-model)
    - Model construction and parameters
    - Connectivity profiles
    - Simulation and data storage
2. [Visualizing Model Behavior](#visualizing-model-behavior)
    - Plotting connectivity
    - Analyzing outcomes

## Prerequisites

- Python 3.7+
- Jupyter Notebook
- The following Python packages:
    - brian2
    - numpy
    - scipy
    - matplotlib
    - pandas
    - ipywidgets
    - pickle

Install required packages using pip:

```bash
pip install brian2 numpy scipy matplotlib pandas ipywidgets
```

## Usage

1. **Clone the repository and navigate to the folder:**
   ```bash
   git clone https://github.com/hkisic/BEP.git
   cd BEP
   ```

2. **Open the notebook:**
   ```bash
   jupyter notebook AdExIF_Model_LFP.ipynb
   ```

3. **Run the notebook cells sequentially:**
   - The notebook will simulate the network under different connectivity profiles.
   - Results (LFPs, voltage traces, connectivity data) are saved to the filesystem in organized directories.
   - Custom helper functions are provided for loading and analyzing saved data.

## File Structure

- `AdExIF_Model_LFP.ipynb`: Main notebook for model definition, simulation, analysis, and visualization.
- `final_result_batch_*`: Directories (created during execution) containing experiment results and logs.
- Helper scripts and code for data saving and loading are included within the notebook.

## Main Functions

- `run_model(connectivity_profile, N, **params)`: Core simulation function. Runs the network with given parameters and connectivity.
- `save_simulation_data(...)`: Helper for saving simulation results in a consistent format.
- `load_simulation_data(filepath)`: Re-loads results for analysis and plotting.

## Customization

- Adjust neuron numbers, connectivity parameters, noise, and simulation duration within the notebook to explore different scenarios.
- New connectivity profiles can be added by modifying the `run_model` function.

## Output Data

- Local field potentials (LFP) for each virtual electrode.
- Voltage traces and synaptic currents for all neurons.
- Connectivity matrices and synapse statistics.
- Experiment parameter logs for reproducibility.

## Visualization

- Built-in plotting code for:
    - Network connectivity graphs
    - LFP time series
    - Neuron voltage traces
    - Synapse count distributions

## Notes

- Simulations of this scale may require substantial memory and CPU time.
- Results are automatically organized by experiment and timestamp for reproducibility.

## References

- Brian2 Simulator: https://brian2.readthedocs.io
- AdExIF Model: Brette & Gerstner, 2005, J. Neurophysiology


