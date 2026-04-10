# KCA_DSTGCN
Y. Hu, L. Chen, F. Zhou, J. Zhao and W. Wang, "Modeling of Gas Turbines via a Knowledge-Embedded Condition-Aware Dynamic Spatiotemporal Graph Convolutional Network," in IEEE Transactions on Industry Applications, doi: 10.1109/TIA.2026.3678882. 

## Project Introduction

The code in this repository is publicly available. 



## File Structure

```text
├── model/                  # Model architecture
│   ├── layers.py           # Network layers and modules
│   └── models.py           # Main model definitions (KCA-DSTGCN)
│
├── data/                   # Dataset folder or data samples
│
├── script/                 # Training and utility scripts
│   ├── dataloader.py       # Data loading and preprocessing
│   ├── earlystopping.py    # Early stopping for training
│   ├── opt.py              # Optimizer
│   └── utility.py          # Helper functions and evaluation metrics
│
├── requirements.txt        # Python dependencies
└── README.md               # Project description and usage instructions

```
## 📊 Metrics

| Target | R² | MAPE |
| :----: | :----: | :----: |
| T2 | 0.9885 | 0.1393% |
| T4 | 0.9805 | 0.2179% |
| P4 | 0.9877 | 0.4296% |
| WO | 0.9871 | 0.4655% |
| **Average** | **0.9860** | **0.3131%** |


## Environmental Requirements

-  Python==3.10.0
- matplotlib==3.10.7
- numpy==2.1.2
- pandas==2.3.3
- torch==2.8.0
- scikit-learn==1.7.2
- scipy==1.15.3
- tqdm==4.67.1

```bash
pip install -r requirements.txt
```
## Run the script for testing only (loads the pre-trained model):

```bash
python main_gt.py
```
## Retrain the model:
If you want to retrain the model from scratch, uncomment the following line in main_gt.py:
```bash
# train(args, model, loss, optimizer, scheduler, es, train_iter, val_iter)
```
## Use Your Own Dataset
To use your own data, replace the dataset paths in `main_gt.py` and `dataloader.py` with the paths to your dataset.

## Contact Information

If there are any questions about the codes and datasets, please don't hesitate to contact us. Thanks!

