# Sensors-Data-about-Fuel-Consumption-in-Buses
This repository provides data collected by sensors about fuel consumption and contextual conditions of buses of public transportation 

- DATASET.csv
    Dataset with features:
        Index: Date-time
        VehicleID: Vehicle Identifier
        avg_slope (%): average slope of the path   
        mass (ton): of the vehicle including passengers     
        aircond_ptime (%): percentage of travel time with air conditioning on
        stop_ptime (%): percentage of the travel time with the vehicle stopped and with the engine on
        brake_usage (%): percentage of the travel time with the brake and with the engine on 
        accel (m/s**2): percentage of the travel time with thge accelerator pedal pressed
        
- Zip file TS_VEIC_MONTH_COLLECTION

    Contains multivariate time-series collection constructed from DATASET.csv
    Each time-series is named as: "V"<vehicle-index>-"M"<month-index>
    (e.g. "V1M1" is the multivariate time-series of VehicleID 1 in the Month of January)
    
- Zip file SYNTHETIC DATASET COLLECTION (generated from a given ground truth of causal dependencies among variables (X0-X4) assumed by a given DAG)

    Contains a collection of synthetic dataset:
    LLC: Lag-Linear-Combination dataset
    GCD: Gaussian Conditional Distribution dataset
    GCD_LLC_alpha: alpha = (0.2, 0.5, 0.8)
    
N.B. The monthly time-series is measured during a given month but contains generally only 5 days of the month
