## ML Predictive Maintenance Dashboard

This project provides a predictive maintenance dashboard for monitoring industrial pump systems. It enables engineers to:

- Visualize real-time or uploaded sensor data  
- Forecast the next 50 values for key indicators (e.g., vibration, temperature)  
- Train custom machine learning models using uploaded datasets  
- Optionally integrate with OPC UA data sources from PLC/SCADA systems

### Tech Stack

- Python, Streamlit  
- scikit-learn (MultiOutputRegressor)  
- pandas, NumPy, matplotlib  
- OPC UA integration via `opc_logger.py` (optional)

### Project Structure

```
├── model/                        # Forecast models (.pkl files)
├── data/                         # Sensor data (.csv)
├── web_app/                      # Streamlit app
│   └── web_app.py
├── model/train_multi_forecast_model.py
├── opc_logger.py
├── LICENSE
└── README.md
```

### How to Use

1. [Visit the app link](https://ml-predictive-maintenance.streamlit.app/)
2. Upload your CSV (or check \"Use demo OPC UA data\")
3. Preview your data and plot it
4. (Optional) Click \"Train My Forecast Model\" to build your own model
5. View 50-step future predictions for any sensor tag
