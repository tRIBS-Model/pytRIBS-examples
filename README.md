# pytRIBS Example Workflow

[![DOI](https://zenodo.org/badge/DOI/placeholder.svg)](https://doi.org/10.5281/zenodo.placeholder)

This repository provides official example workflows for **pytRIBS**, the Python input/output interface for the tRIBS distributed hydrological model. Its primary purpose is to allow users to:

1.  **Learn the pytRIBS workflow** by stepping through a complete, real-world example from raw data to simulation.
2.  **Reproduce results** associated with the official pytRIBS publication.
3.  **Access template scripts** that can be adapted for setting up new basins.

This repository is designed to be a companion to the [pytRIBS package](https://github.com/tRIBS-Model/pytRIBS) and the [tRIBS model source code](https://github.com/tRIBS-Model/tRIBS).

## Available Workflows

This repository currently contains the following tutorial workflows:

*   **`newman_demo/`**: A complete setup for the Newman Canyon domain. This Jupyter Notebook demonstrates:
    *   Preprocessing raw DEM and soil/vegetation rasters.
    *   Generating the tRIBS triangular irregular network (TIN).
    *   Processing meteorological forcing data (NLDAS).
    *   Writing the input files and executing the tRIBS model.
    *   Visualizing the results.

    *Note: To reduce repository size, the vegetation raster and DEM in this example has been resampled to 3m resolution.*

## Quickstart: Running the Example

Follow these steps to execute the workflow and verify your pytRIBS environment is configured correctly.

### Step 1: Prerequisites

Before you begin, ensure you have the following:

*   A working installation of **Python 3.9+**.
*   The **Docker** installed on your system.
*   The **pytRIBS** package installed.

### Step 2: Environment Setup

We recommend running this workflow in a dedicated virtual environment.

```bash
# Clone repositories
git clone https://github.com/tRIBS-Model/pytRIBS-examples.git
git clone https://github.com/tRIBS-Model/pytRIBS.git
cd pytRIBS-examples

# Create a virtual environment (optional but recommended)
python -m venv venv
source venv/bin/activate

# Install dependencies
cd pytRIBS
pip install -e .
```

### Step 3: Execute the Notebook

Navigate to the workflow directory and launch Jupyter.

```bash
# Launch Jupyter
jupyter notebook
```
Open the `pytRIBS_workflow_Newman.ipynb` notebook.

## Citation

If you use these workflows or the pytRIBS package in your research, please cite the following paper:

> Raming, L.W., Vivoni, E.R., Cederstrom, C.J., Hossain, M.A., Ko, A., and Becerra, J.A. (2025). pytRIBS: An open, modular, and reproducible python-based framework for distributed hydrologic modeling. Environmental Modelling & Software, 188, 106432, [https://doi.org/10.21105/joss.06747](https://doi.org/10.1016/j.envsoft.2025.106432)
