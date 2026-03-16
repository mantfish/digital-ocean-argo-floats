# Argo Float Data Tutorial

---

## What is the Argo program?

[Argo](https://argo.ucsd.edu/) is a global array of ~4,000 autonomous profiling floats that
drift through the ocean, periodically diving to ~2,000 m and measuring **temperature**,
**salinity**, and **pressure** (and sometimes more) on the way back up.  Each float transmits its data via
satellite, the data then get's checked before being uploaded to a server, making it freely available online.
After a year, the old data is checked again and adjusted if necessary.

Each float is identified by a unique **WMO number** (e.g. `3902607`).

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

### Clone the repository
```bash
# Open a terminal and navigate to the directory where you want to clone the repository
# Then run
git clone https://github.com/euro-argo/argo-float-tutorials.git
cd argo-float-tutorials
```
If you don't have git installed, you can download the repository as a zip file .

### Option A: Pip (if you already have Python 3.9+)

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
### Option B: If you have conda installed

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

Then open the `notebooks/` folder and start with `00_getting_started.ipynb`.

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
