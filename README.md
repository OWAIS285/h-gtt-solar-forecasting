# H-GTT: Hybrid Graph Attention Transformer for Solar Energy Forecasting

[![Paper Results](https://img.shields.io/badge/MAE-105.90%20GWh-brightgreen.svg)](https://github.com/OWAIS285/h-gtt-solar-forecasting) [![R²](https://img.shields.io/badge/R²-0.8888-blue.svg)](https://github.com/OWAIS285/h-gtt-solar-forecasting)

**Official code for "A Deep Learning-Based Hybrid Approach for Solar Energy Prediction Using GAT and Transformers"** - MAE **105.90 GWh**, R² **0.90** on Pavagada Solar Plant (11 years data).

**H-GTT** combines **Graph Attention Networks (GAT)** + **TransformerConv** for next-day solar forecasting. Beats TCN (203.50), Transformer (152.58), XGBoost, LSTM on all metrics.

## 🎯 **Key Results (Table 3)**
| Model | MAE (GWh) | RMSE (GWh) | R² |
|-------|-----------|------------|----|
| **H-GTT** | **105.90** | **133.14** | **0.90** |
| Transformer | 152.58 | 177.79 | 0.8017 |
| TCN | 203.50 | 210.19 | 0.7228 |
| XGBoost | 211.99 | 261.57 | 0.5739 |

## 🚀 **Quick Start**

```bash
# 1. Clone
git clone https://github.com/OWAIS285/h-gtt-solar-forecasting.git
cd h-gtt-solar-forecasting

# 2. Environment
pip install -r requirements.txt

# 3. Get data (Pavagada Solar Plant)
# Download solar_data.csv (temp, humidity, windspeed, cloudcover, solarradiation, solarenergy(GWh))
# Place in ./data/ folder

# 4. Run (prints Table 3 results)
python h_gtt_45day_lookback.py
