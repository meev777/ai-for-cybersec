# TP 02 — Web Log Analysis for Cybersecurity

Coursework project for **AI for Cybersecurity**. This project analyses simulated
Apache/Nginx-style web-server access logs to detect a directory-enumeration scan.

## Included files

- `Lab02_Log_Analysis.ipynb` — complete, reproducible analysis.
- `Lab02_Report.pdf` — project report.
- `Lab 02 IA fo CyS 3SC.pdf` — assignment brief.
- `data/` — simulated day-one/day-two access logs, ground-truth labels, and
  exported results.

## Method

The notebook parses the logs, explores traffic and error patterns, visualizes
the anomaly, and evaluates a simple explainable rule: alert when an IP produces
more than 20 HTTP 404 responses in a one-minute window. Day one includes an
injected directory-enumeration scan; day two is an unseen normal-only test day.

## Run

Open `Lab02_Log_Analysis.ipynb` with a Python 3.10+ Jupyter environment and run
it from top to bottom. The included dataset is simulated and the random seeds
are fixed, so results are reproducible without internet access.
