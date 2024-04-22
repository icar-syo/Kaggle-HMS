#**HMS - Harmful Brain Activity Classification**<br>
##Project Background:  
The goal of this competition is to predict and classify epileptic seizures and other types of harmful brain activities using EEG and spectrogram data.<br>

###Project Approach:
1.Data Preprocessing:  
Through data exploratory data analysis (EDA), it was discovered that there were duplicate similar data in the dataset,  
which were removed. Missing values were also found in both EEG and spectrogram data, and those missing values were removed.  

2.Feature Engineering:  
Feature construction mainly involved concatenating spectrogram data of different lengths obtained from 10-minute spectrograms  
and EEG using various methods to generate new training data. Additionally, EEG wave data was obtained by subtracting pairs of original EEG data.

3.Model Building:  
The models used include efficientNet_v2, efficientNet_b4, and EegNet,  
trained with different data. A total of 8 models were trained for ensemble.

4.Model Training:  
The training adopted a 10-fold cross-validation method. Data augmentation involved adding masks to the time/frequency dimensions  
of the spectrogram data. Training followed a two-stage training method, where data was split into two parts based on different data information.  
In the first stage, part of the data was trained, and in the second stage, the pre-trained models from the first stage were further trained  
on the remaining training data. Finally, the results of the 8 models trained with different models and data were integrated to obtain the optimal solution.
