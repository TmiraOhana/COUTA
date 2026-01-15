# COUTA – Time Series Anomaly Detection

Implementation of **COUTA (Calibrated One-Class Classification for Unsupervised Time Series Anomaly Detection)**  
based on Xu et al., IEEE Transactions on Knowledge and Data Engineering (2024).

---

## Requirements

Python 3.9+

Install dependencies:

```bash
pip install -r requirements.txt
```

---

## Datasets

Due to file size limitations, **datasets are NOT included in this repository**.

Please download the original datasets from the following sources:

- **ASD** – https://github.com/zhhlee/InterFusion  
- **SMD** – https://github.com/NetManAIOps/OmniAnomaly  
- **SWaT** – https://itrust.sutd.edu.sg/itrust-labs_datasets  
- **WaQ** – https://www.spotseven.de/gecco/gecco-challenge  
- **DSADS** – https://github.com/zhangyuxin621/AMSL  
- **Epilepsy** – https://github.com/boschresearch/NeuTraL-AD  

---

## Dataset Directory Structure

After downloading and preprocessing, place the datasets in the following structure:

```
project_root/

    data/                 # (optional) original raw datasets
        ASD/
        SMD/
        ...

    data_processed/       # REQUIRED – processed datasets used by the code
        ASD/
            machine-1-1/
            machine-1-6/
            machine-1-7/
            machine-2-1/
            machine-2-2/
            machine-2-7/
            machine-2-8/
            machine-3-3/
            machine-3-4/
            machine-3-6/
            machine-3-8/
            machine-3-11/
            omi-1/
            omi-2/
            omi-3/
```

Each subfolder contains the processed time-series files for one machine or system instance.

**Note:**  
The project reads datasets from the `data_processed/` directory when running experiments.

---

## Run

Example: run COUTA on the ASD dataset using CPU:

```bash
python main.py --algo COUTA --data ASD --device cpu
```

---

## Citation

If you use this project, please cite:

```bibtex
@article{xu2024calibrated,
  title={Calibrated one-class classification for unsupervised time series anomaly detection},
  author={Xu et al.},
  journal={IEEE Transactions on Knowledge and Data Engineering},
  year={2024}
}
```

---

## Notes

- The `data/` and `data_processed/` directories should be excluded from GitHub using `.gitignore`.
- Only source code and configuration files are tracked in this repository.
