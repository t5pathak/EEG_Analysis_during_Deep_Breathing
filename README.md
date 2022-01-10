# Predicting Breathing Patterns using EEG Data - a Neural Network based Deep Breathing Classification Model

## Introduction 
Normal ventilation is largely an autonomic process in humans, with brain signals from accessory muscles filtered out during resting state (RS) analysis. A deep breathing (DB) exercise requires control of respiratory patterns of the inspiratory expansion and expiratory contraction. The present study compares the EEG signals during RS and DB, with a specific focus on analyzing alpha, beta, and theta frequency band rhythms of the motor regions of the brain. The study also presents a neural network-based classification model to predict breathing patterns. 
 
## Materials 
The dataset contains 32-channel scalp EEG data of 29 healthy male subjects (age:  mean = 24.25 yrs; SD = 3.96 yrs), each first performing shallow breathing (RS) for 15 seconds followed by 15 seconds of DB. The 32-channel scalp EEG dataset was pre-processed, and 15-second windows of RS and DB  of all subjects were concatenated to create a (29x15) datasets. Post standard pre-processing, the artifacts due to excessive head movement were rejected by visual inspection. 
 
## Methods 
The time-series data was transformed into the spectral domain, and the power spectrum was extracted to examine the change in brain activity when subjects changed breathing patterns from shallow (RS) to DB. We calculated the average percentage change in brain activity across all electrodes for the different frequency bands. After observing a uniform decrease in power amplitude, a k-means based multiple cluster classification model was used to predict the breathing pattern using EEG data from 9 motor electrodes. The model clustered both the RS and DB EEG time series into ‘k’ clusters each and utilized cluster centroid data to perform classification. The classification accuracies were insignificant due to the highly varied nature of the resting data. The highly disparate values of peak and average inter-subject resting-state coherence confirmed the variability among resting-state data. To overcome clustering inefficiencies, we implemented a neural network-based classification model to predict breathing patterns. 
 
## Results 
When compared with resting-state data, EEG signals during deep breathing shows a uniform decrease in brain activity in the theta (25%) and alpha (33.5%) frequency bands. From the multiple cluster-based k-means, we observed an increase in classification accuracy with an increase in the number of clusters. The classification accuracy peaked at 65.28% with k=4 (four clusters each). Using a neural network-based pipeline, we achieve a 90.97% classification accuracy. 
 
## Conclusions 
A deep breathing exercise is an altered respiratory effort that engages cardiac and cortical areas, especially the motor regions of the brain. The data from this study shows that deep breathing results in a consistent reduction in average brain activity. While the reduction in power was observed among all frequency bands, it was most prominent among the alpha frequency band. The neural network-based pipeline resulted in high classification accuracy, which indicates a high cross-subject EEG data similarity during deep breathing. Moreover, this real-time classification model with the ability to predict the breathing pattern has potential applications in assessing the subject-specific effectiveness of deep breathing-based techniques as followed in practices like yoga and in anxiety assessment. 
