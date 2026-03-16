# Argo Float Data Tutorials for Ocean Engineers

A beginner-friendly collection of Python/Jupyter notebooks for downloading and visualising
Argo profiling float data.  No prior Python experience is assumed.

---

## What is Argo?

[Argo](https://argo.ucsd.edu/) is a global array of ~4,000 autonomous profiling floats that
drift through the ocean, periodically diving to ~2,000 m and measuring **temperature**,
**salinity**, and **pressure** on the way back up.  Each float transmits its data via
satellite — making it freely available online.

Each float is identified by a unique **WMO number** (e.g. `6902746`).

---

## Notebooks in this repository

| Notebook | Topics covered |
|---|---|
| `00_getting_started.ipynb` | Install packages, fetch your first float, inspect the data |
| `01_single_float_contours.ipynb` | Temperature & salinity contour plots vs depth and time |
| `02_mixed_layer_depth.ipynb` | Calculate and plot Mixed Layer Depth (MLD) over time |
| `03_regional_floats.ipynb` | Fetch multiple floats from a geographic region, map positions |

---

## Setup instructions

### Option A — conda (recommended)

```bash
# 1. Install Miniconda if you don't have it:
#    https://docs.conda.io/en/latest/miniconda.html

# 2. Create the environment from the file in this repo
conda env create -f environment.yml

# 3. Activate it
conda activate argo-tutorials

# 4. Launch Jupyter
jupyter notebook
```

### Option B — pip (if you already have Python 3.9+)

```bash
# 1. (Optional but recommended) create a virtual environment
python -m venv argo-env
source argo-env/bin/activate        # Mac / Linux
argo-env\Scripts\activate           # Windows

# 2. Install dependencies
pip install -r requirements.txt

# 3. Launch Jupyter
jupyter notebook
```

Then open the `notebooks/` folder and start with `00_getting_started.ipynb`.

---

## Internet connection required

The notebooks download data live from the Argo ERDDAP server.  You need an active
internet connection when running cells that call `argopy`.

---

## Key packages used

| Package | Purpose |
|---|---|
| [`argopy`](https://argopy.readthedocs.io/) | Download Argo float data |
| `pandas` | Store and manipulate tabular data |
| `matplotlib` | Plots and figures |
| `numpy` | Numerical calculations |
| `xarray` | Intermediate data format returned by argopy |

---

## Finding your own float

1. Go to the [Argo float visualisation tool](https://fleetmonitoring.euro-argo.eu/)
2. Click on any float to find its **WMO number**
3. Replace the WMO number in any notebook with your chosen float

---

## Useful links

- [Argo homepage](https://argo.ucsd.edu/)
- [argopy documentation](https://argopy.readthedocs.io/)
- [Euro-Argo fleet monitor](https://fleetmonitoring.euro-argo.eu/)
- [Argo data user manual](https://doi.org/10.13155/29825)
