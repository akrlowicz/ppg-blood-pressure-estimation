# ppg-blood-pressure-estimation

This notebook attempts blood pressure estimation from PPG signal. On the basis of https://arxiv.org/pdf/1705.04524v3.pdf article here LSTMs are used on extracted features from signal.


# Dataset

Dataset is private, consisting of PPG signal and info files with blood pressure for every signal.

# Problem approach

Bidirectional LSTMs were used with residual connections to predict blood pressure (systolic and diastolic). Instead of feeding signal to LSTMs, feature based approach was used. Features were extracted for every beat in signal based on location of systolic, diastolic and dicrotic peaks. To find out more about features and such approach check article linked above.

# Results so far

RMSE was used as metric, MAE as loss function. Since RMSE was converted to [mmHg] unit in article, here I use same unit.

Train Score RMSE [mmHg]: 
 SBP 15.65 
 DBP 10.33
Test Score RMSE [mmHg]: 
 SBP 16.58 
 DBP 12.05

//TODO

  
# Further actions

//TODO

# Used libraries

- numpy, scipy
- pandas
- matplotlib
- sk-learn, keras

# References 
[1] Peng Su, Xiao-Rong Ding, Yuan-Ting Zhang, Fellow, IEEE, Jing Liu, Fen Miao, Ni Zhao, Long-term Blood Pressure Prediction with Deep Recurrent Neural
Networks, 2018, https://arxiv.org/pdf/1705.04524v3.pdf
