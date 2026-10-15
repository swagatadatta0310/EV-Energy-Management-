# Physics-Informed Machine Learning for Electric Vehicle Energy Consumption Estimation

## Overview

This project presents a Physics-Informed Machine Learning (PIML) framework for estimating electric vehicle (EV) energy consumption by integrating vehicle physics, electrical subsystem modelling, and machine learning-based correction.

The proposed framework combines the interpretability of physics-based modelling with the predictive capabilities of machine learning. It aims to improve energy estimation accuracy while maintaining computational efficiency for potential real-time EV applications.

## Objectives

- Develop a physics-informed framework for EV energy consumption estimation.
- Model mechanical energy requirements under different driving conditions.
- Incorporate battery characteristics, power electronics, drivetrain efficiency, and electrical losses.
- Investigate machine learning models such as Random Forest and XGBoost for data-driven correction.
- Integrate mechanical, electrical, and auxiliary energy contributions.
- Evaluate prediction accuracy, error distribution, model agreement, and computational performance.

## Proposed Methodology

The framework consists of three main subsystems.

### 1. Mechanical Subsystem

This subsystem estimates the mechanical energy required to move the vehicle. It considers:

- Rolling resistance
- Aerodynamic drag
- Road gradient and slope
- Vehicle operating conditions

These factors influence the energy required under different driving conditions.

### 2. Electrical Subsystem

The electrical subsystem represents the energy conversion process and associated losses. It includes:

- Battery pack voltage and capacity
- Electric motor and inverter
- Drivetrain efficiency
- Electrical loss estimation

This subsystem estimates the electrical energy associated with vehicle operation.

### 3. Auxiliary and Machine Learning Subsystem

This subsystem considers energy consumption from auxiliary equipment, including HVAC systems and onboard electronics.

Machine learning models, such as Random Forest and XGBoost, are considered for data-driven correction. The resulting correction is integrated with the physics-based energy estimates through an energy fusion layer.

The central concept is to **retain the physical interpretation of EV energy consumption while using machine learning to account for additional nonlinear behaviour and residual errors**.

## Input Parameters

Depending on data availability and implementation, the framework may consider:

- Vehicle speed
- Acceleration
- Vehicle mass
- Road slope
- Motor torque
- Battery voltage and capacity
- Drivetrain efficiency
- HVAC and auxiliary loads

## Model Evaluation

The framework supports evaluation using the following metrics and analysis techniques:

| Evaluation method | Purpose |
|---|---|
| RMSE | Measures prediction error, with greater sensitivity to large errors |
| MAE | Measures average absolute prediction error |
| MAPE | Expresses prediction error as a percentage |
| R² | Evaluates goodness of fit |
| Bland–Altman plot | Examines agreement and systematic bias between predictions and reference values |
| Box plot | Compares error distributions, variability, and potential outliers |
| SHAP analysis | Identifies feature contributions to model predictions |
| Sensitivity analysis | Examines the influence of input variations on estimated energy consumption |
| Computational analysis | Evaluates inference time, model size, and memory requirements |

The analyses reported as completed should correspond to the actual implementation and results available in the repository.

## Technology Stack

- Python
- Google Colab / Jupyter Notebook
- NumPy
- Pandas
- Matplotlib
- Seaborn
- Scikit-learn
- XGBoost, where implemented
- Graphviz for flowchart generation

## Repository Structure

```text
EV-Energy-Consumption-PIML/
├── README.md
├── notebooks/
├── figures/
├── results/
├── requirements.txt
└── LICENSE
```

The structure above is illustrative and can be adjusted to match the actual repository contents.

## How to Run

1. Open the project repository on GitHub.
2. Open the available Jupyter Notebook or launch it in Google Colab.
3. Install the required Python libraries.
4. Load the dataset required by the notebook.
5. Execute the notebook cells in sequence.
6. Review the generated predictions, evaluation metrics, and visualizations.

Refer to the notebook for implementation-specific instructions and dataset requirements.

## Research Significance

This project explores the integration of physical knowledge and data-driven learning for EV energy estimation. The approach aims to balance physical interpretability, prediction accuracy, and computational efficiency.

Potential research applications include:

- EV energy consumption estimation
- Driving-range estimation
- Battery-aware energy management
- EV performance analysis
- Intelligent transportation systems
- Integration with EV charging and microgrid energy management

These applications require validation appropriate to the intended operating conditions.

## Limitations

- Model performance depends on data quality and the availability of appropriate vehicle parameters.
- Results based on synthetic data should not be interpreted as experimental vehicle validation.
- Generalization across vehicle types and driving cycles requires further evaluation.
- Application-level relevance to engineering standards does not establish formal certification or compliance.
- Real-world deployment requires suitable experimental validation.

## Future Work

- Validate the framework using measured EV driving-cycle data.
- Extend the model to battery State-of-Charge and driving-range estimation.
- Investigate uncertainty quantification and robustness under varying road and weather conditions.
- Optimize the model for real-time implementation.
- Integrate the framework with EV charging, battery management systems, and microgrid energy management.

## Author

**Swagata Datta**  
Electrical Engineering  
Research Interests: Electric Vehicles, Physics-Informed Machine Learning, EV Energy Estimation, and Power Systems.

## Disclaimer

This repository is intended for research and educational purposes. Performance depends on the dataset, implementation, and evaluation methodology. The framework is not a certified automotive safety or battery-management system.

## Citation

If you use this repository in academic research, please cite the associated research paper when its publication details become available.
