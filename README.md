# COUTA – Time Series Anomaly Detection

Implementation of **COUTA (Calibrated One-Class Classification for Unsupervised Time Series Anomaly Detection)**  
based on Xu et al., IEEE TKDE 2024.

---

## Requirements

Python 3.9+

```bash
pip install -r requirements.txt
```

---

## Datasets

Download the datasets from:

- **ASD** – https://github.com/zhhlee/InterFusion  
- **SMD** – https://github.com/NetManAIOps/OmniAnomaly  
- **SWaT** – https://itrust.sutd.edu.sg/itrust-labs_datasets  
- **WaQ** – https://www.spotseven.de/gecco/gecco-challenge  
- **DSADS** – https://github.com/zhangyuxin621/AMSL  
- **Epilepsy** – https://github.com/boschresearch/NeuTraL-AD  

Place the processed datasets under:

```text
data/
```

Example:

```text
data/ASD/
data/SMD/
```

> **Note:**  
> The **ASD dataset is already preprocessed and included in this repository**,  
> so it can be used directly without additional preparation.

---

## Run

```bash
python main.py --algo COUTA --data ASD --device cpu
```

---

## Citation

```bibtex
@article{xu2024calibrated,
  title={Calibrated one-class classification for unsupervised time series anomaly detection},
  author={Xu et al.},
  journal={IEEE Transactions on Knowledge and Data Engineering},
  year={2024}
}
```
