*Zero‑Day Attack (Defensive Research)*– README

Short version: This repo is for defensive security research on detecting previously unseen (zero‑day–like) behaviors using synthetic data, benign telemetry, and public CVE write‑ups for context. No exploit code. No weaponization.

⚠️ Legal & Ethical Use

This project is provided solely for education and defense: threat modeling, anomaly detection, blue‑team analytics, and research. Do not use it to attack systems you do not own or have explicit permission to test. By using this repository, you agree to follow your local laws and the Responsible Disclosure policy below.

🎯 What this project is / isn’t

Is: A reproducible framework to simulate zero‑day–like behaviors (novel sequences, rare process trees, suspicious network patterns) and evaluate detection strategies that generalize to the unseen.

Isn’t: A collection of exploits or step‑by‑step attack guides. We only reference public CVEs at a high level to mirror tactics/techniques in benign synthetic data.

✨ Features

Synthetic Zero‑Day Simulator: Generate time‑series and event logs (process, file, network) that mimic unknown attack patterns without using real malware.

Detection Methods:

Unsupervised: Isolation Forest, One‑Class SVM, HBOS, LOF

Self‑supervised: Autoencoders (dense/LSTM/GRU), contrastive sequence models

Graph‑based: Process‑tree / host‑graph anomaly scoring

Evaluation Harness: ROC‑AUC/PR‑AUC, alert volume, mean time‑to‑detect (MTTD), and leave‑family‑out testing to simulate zero‑day conditions.

Reproducible Pipelines: Config‑driven data generation, training, and scoring via configs/*.yaml.

Visualization: Notebooks + lightweight dashboard to inspect anomalies and attack timelines.
