OPTIC-ER: An Attention-based Reinforcement Learning Platform for Equitable Emergency Response
![alt text](https://img.shields.io/badge/License-Apache%202.0-blue.svg)
This repository contains the official source code, data, and analysis for the OPTIC-ER research project, as detailed in the paper:
OPTIC-ER: A Reinforcement Learning Framework for Real-Time Emergency Response and Equitable Resource Allocation in Underserved African Communities
Mary Tonwe
[*Link to arXiv pre-print]
About The Project
OPTIC-ER is a novel AI-powered governance platform designed to solve the critical challenge of inefficient and inequitable emergency service delivery in resource-constrained environments. The system moves beyond reactive dispatch to enable proactive, data-driven infrastructure planning.
The platform's core is an Attention-based Actor-Critic (A2C) agent, which achieved a 100% optimality rate in a high-fidelity simulation of Rivers State, Nigeria. Beyond tactical dispatch, the system's Strategic Policy Engine provides actionable recommendations for infrastructure investment to eliminate service gaps and promote equity.
This work was developed under the TALS framework:
Thin computing
Adaptability
Low-cost
Scalability
Repository Structure
/data: Contains the curated geospatial datasets required to run the simulation.
/notebooks: Contains the two core Jupyter notebooks for reproducing the study.
/reports: Contains all generated CSV reports, including the master dispatch log and the final policy intervention plan.
LICENSE: The Apache 2.0 License governing the use of this project.
.gitignore: Specifies which files and folders for Git to ignore.
requirements.txt: A list of all Python dependencies required to run the code.
How to Reproduce the Results
To reproduce the findings of this paper, please follow these steps.
1. Prerequisites
A Python environment (e.g., via Anaconda or Google Colab).
The WorldPop 2020 population raster for Nigeria (nga_ppp_2020_UNadj_constrained.tif). This must be placed in the /data directory after cloning.
2. Installation
Clone this repository:
code
Bash
git clone https://github.com/marytonwe/OPTIC-ER.git
cd OPTIC-ER
Install the required Python packages:
code
Bash
pip install -r requirements.txt
3. Execution Order
The project is divided into two main notebooks that should be run in sequence:
notebooks/1_Data_Curation_and_Analysis.ipynb
This notebook handles all the initial data sourcing, cleaning, and curation. It performs the preliminary data analysis and generates the foundational visuals for the paper.
notebooks/2_Training_and_Evaluation.ipynb
This notebook is the core of the project. It loads the curated data, builds the simulation environment, trains the Attention-based RL agent, and runs the final, definitive analysis suite. It will generate all the final results, tables, and policy maps.
Note: The pre-computation of the "Travel Time Atlas" within this notebook is computationally intensive and may take a significant amount of time on the first run.
Citation
If you use this work in your own research, please cite our paper:
code
Bibtex
@article{Tonwe2025OPTICER,
  title={OPTIC-ER: A Reinforcement Learning Framework for Real-Time Emergency Response and Equitable Resource Allocation in Underserved African Communities},
  author={Mary Tonwe},
  journal={*arXiv preprint arXiv:...},
  year={2025}
}
Acknowledgements
This work was made possible by numerous open-source libraries and public datasets.SALT