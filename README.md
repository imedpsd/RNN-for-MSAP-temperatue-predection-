# Rotor Temperature Prediction in Permanent Magnet Synchronous Machines (PMSMs)

## Overview
This project focuses on predicting rotor temperature in Permanent Magnet Synchronous Machines (PMSMs) using Artificial Neural Networks (ANN) and, more prominently, Recurrent Neural Networks (RNN). The study aims to enhance temperature estimation accuracy, facilitating proactive maintenance and mitigating potential risks associated with temperature-related faults in PMSMs.

## Dataset
The dataset consists of multiple measurement sessions collected from a PMSM deployed on a test bench. It includes various sensor data such as currents, voltages, motor speed, and torque, sampled at 2 Hz. The dataset is structured to allow for the differentiation of measurement sessions through a unique profile ID.

## Methodology
1. **Data Preprocessing**: The data is partitioned into features and target variables, followed by standardization using `StandardScaler`.
2. **Model Construction**:
   - Four distinct Neural Networks (NNs) are constructed and compiled with unique architectures.
   - A bagging approach is applied to enhance model diversity.
   - A combiner network merges the outputs of the individual networks.
3. **Recurrent Neural Network (RNN)**: The RNN architecture is specifically designed to address the limitations of traditional NNs by effectively handling the sequential nature of the dataset. This allows the model to capture temporal dependencies and dynamic patterns, significantly improving temperature estimation accuracy.

## Experimental Results
The performance of the models is evaluated through loss and accuracy metrics during the training process. The results indicate that the combined approach of NNs and RNNs significantly enhances temperature estimation accuracy, with the RNN effectively mitigating the issue of spikes in temperature predictions.

### Drawback of Normal NN
**[Drawback of Normal NN](RNN-for-MSAP-temperatue-predection-/Images/NN.png)**

### How RNN Fixed the Spikes Problem
**[How RNN Fixed the Spikes Problem](RNN-for-MSAP-temperatue-predection-/Images/RNN.png)**

## Conclusion
The integration of NNs and RNNs has led to significant advancements in accurately predicting and monitoring the temperature of PMSMs. This project highlights the potential of RNNs in improving the performance and reliability of electrical machines in various industrial applications, showcasing their ability to handle complex, time-dependent data effectively.
