# TS-PMCD
Causal Structure-Based Forecasting for Multivariate Industrial Time Series under Covariate Drift
This repository contains the core implementation of TS-PMCD, a framework for forecasting multivariate time series under covariate drift while preserving causal structures.

📁Code Structure
main.py – entry point for training/evaluation

ts_pmcd_model.py – main model implementation

acdr.py – adaptive covariate drift recognition

causal_diff.py – causal diffusion process

graph_encoder.py, fusion_network.py, sflu.py, ifl.py – supporting modules

config.json – configuration file

data/ – folder for datasets

⚠️ Important Note on Causal Prior
TS-PMCD uses a pre-trained Causal-Transformer (Liang X, Hao K, Chen L, et al. Causal inference of multivariate time series in complex industrial systems[J]. Advanced Engineering Informatics, 2024, 59: 102320.) as the causal prior. Due to an ongoing patent application, the code for Causal-Transformer is not publicly available. You can replace it with any other causal discovery or representation learning algorithm that outputs causal graphs/features.

🚀 Quick Start
Clone the repo and install dependencies .
Place your time series data in data/ (format: (samples, timesteps, features)).
Adjust config.json (data paths, hyperparameters).

Run training:

bash
python main.py --mode train --config config.json
Run forecasting:

bash
python main.py --mode test --checkpoint <path> --config config.json

📚 Citation
If you use this code, please cite our paper:

text
@article{liang2024causal,
  title={Causal inference of multivariate time series in complex industrial systems},
  author={Liang, Xiao and Hao, Kuangrong and Chen, Lei and others},
  journal={Advanced Engineering Informatics},
  volume={59},
  pages={102320},
  year={2024}
}
and the TS-PMCD paper .

📧 Contact
For questions, open an issue or contact [1222029@mail.dhu.edu.cn].


