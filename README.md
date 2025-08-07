**OPTIC-ER: A Reinforcement Learning Framework for Real-Time Emergency Response and Equitable Resource Allocation in Underserved African Communities**  
*Mary Tonwe*  
[*Link to arXiv preprint*](#)

![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)

This repository contains the official source code, datasets, and analysis for the OPTIC-ER research project, as detailed in the paper:

---

## About the Project

**OPTIC-ER** is an AI-powered governance platform designed to solve the challenge of **inefficient and inequitable emergency service delivery** in resource constrained environments. Built under the **TALS framework** (Thin computing, Adaptability, Low-cost, Scalability), it transforms reactive dispatch into proactive, data-driven public policy.

- **Core engine**: Attention-based Actor-Critic (A2C) agent
- **Performance**: 100% optimality rate in high-fidelity simulations of Rivers State, Nigeria

Beyond tactical dispatch, the system's Strategic Policy Engine provides actionable recommendations for **infrastructure investment** to eliminate service gaps and promote equity.


---

## Repository Structure

- /data → Curated geospatial datasets 
- /notebooks → Jupyter notebooks for training, evaluation, and analysis
- /reports → Final CSV outputs (dispatch logs, policy tables)
- LICENSE → Apache 2.0 License
- .gitignore → Files/folders ignored by Git
- requirements.txt → Python dependencies

---

## How to Reproduce Results

### 1. Prerequisites
- Python 3.9+ environment (e.g., Anaconda or Google Colab)
- Download the **WorldPop 2020 raster** for Nigeria:  
  `nga_ppp_2020_UNadj_constrained.tif`  
  ➤ Place it in the `/data` directory after cloning.

### 2. Installation

```bash
git clone https://github.com/marytonwe/OPTIC-ER.git
cd OPTIC-ER
pip install -r requirements.txt
```

### 3. Execution Order
- Notebook 1: notebooks/1_Data_Curation_and_Analysis.ipynb
  Data sourcing, cleaning, clustering, and mapping
  Generates foundational visuals for the paper

- Notebook 2: notebooks/2_Training_and_Evaluation.ipynb
  Loads preprocessed data
  Trains the RL agent and runs final validations
  Generates dispatch logs, policy maps, and performance tables

Note: The Travel Time Atlas generation is computationally intensive on the first run.

## Citation
If you use this work in academic or applied research, please cite:

@article{Tonwe2025OPTICER,
  title     = {OPTIC-ER: A Reinforcement Learning Framework for Real-Time Emergency Response 
               and Equitable Resource Allocation in Underserved African Communities},
  author    = {Tonwe, Mary},
  journal   = {arXiv preprint arXiv:XXXXX},
  year      = {2025}
}

## Acknowledgements
This work was made possible by numerous open-source libraries and public datasets. SALT