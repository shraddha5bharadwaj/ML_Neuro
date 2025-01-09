# ML_Neuro

# Decoding Motor Behavior: Enhancing Trajectory and Velocity Predictions Through Neural Dynamics and Informed Kalman Filtering

## Project Overview
This project investigates the neural dynamics underlying motor tasks, focusing on decoding movement phases and predicting motor trajectories and velocities. The study utilizes neural activity data from the primary motor cortex (M1) and dorsal premotor cortex (PMd) to understand how the brain coordinates complex movements.

## Key Objectives
1. **Decoding Movement Phases:** Analyze neural activity to distinguish between movement planning and execution phases.
2. **Predicting Motor Trajectories:** Utilize a Kalman filter to predict hand and cursor trajectories from neural data.
3. **Velocity Prediction:** Employ a neural operator to predict velocity, learning the velocity function space from both neural spikes and behavioral data.

## Methodology
### 1. Data Collection
- Neural activity data collected from electrode arrays implanted in PMd and M1.
- Behavioral metrics such as hand position, velocity, and trial metadata recorded.

### 2. Data Preprocessing
- Spike times binned at 1 ms intervals.
- Gaussian smoothing applied to reduce noise.
- Data aligned to key trial events for phase-specific analysis.

### 3. Computational Models
- **Kalman Filter:** The mathematical model was tweaked to train the filter using available behavioral data (coordinate data). This training informed the filter, enhancing its ability to predict trajectories accurately.
- **Neural Operator (DeepONet):** Used to predict velocity by learning the velocity function space from both neural spike data and behavioral data.
- **LSTM Networks:** Implemented to capture temporal dependencies in neural activity, effectively distinguishing between planning and execution phases.

## Results
- The **Kalman Filter** demonstrated improved trajectory predictions when trained with behavioral data, confirming our hypothesis.
- **LSTM Networks** provided robust classification of movement phases, leveraging temporal dynamics in the data.
- The **Neural Operator** successfully predicted velocity, indicating a strong functional relationship between neural activity and motor output.

## Key Findings
- **Informed Kalman Filtering** significantly enhances trajectory prediction accuracy.
- **Temporal Dynamics** are crucial for decoding movement phases and predicting motor behavior.
- **Neural Operators** effectively capture complex relationships between neural activity and motor behavior.

## Conclusion
This project successfully demonstrates the integration of advanced computational methods to decode motor behavior from neural data. The findings emphasize the importance of informed filtering, temporal dynamics, and feature engineering in advancing brain-computer interface technologies.

## Future Directions
- Further refine noise estimations for the Kalman Filter to enhance prediction accuracy in complex scenarios.
- Integrate attention mechanisms into LSTM models to improve interpretability and accuracy.
- Expand the dataset to include more diverse neural and motor conditions for broader generalization of methodologies.

## Project Contributors
- Aarushi Dhanuka
- Riya Patel
- Shraddha Bharadwaj

## References
1. Felix, P. (2022). DANDI Archive. Retrieved from [Dandiarchive.org](https://dandiarchive.org/dandiset/000128)
2. Schimel, M., Kao, T.-C., & Hennequin, G. (2023). When and why does motor preparation arise in recurrent neural network models of motor control? *ELife*. [DOI](https://doi.org/10.7554/eLife.89131)
3. Churchland, M. M., Cunningham, J. P., Kaufman, M. T., et al. (2010). Cortical preparatory activity: Representation of movement or first cog in a dynamical machine? *Neuron*. [DOI](https://doi.org/10.1016/j.neuron.2010.09.015)
4. Churchland, M. M., Cunningham, J. P., Kaufman, M. T., et al. (2012). Neural population dynamics during reaching. *Nature*. [DOI](https://doi.org/10.1038/nature11129)

