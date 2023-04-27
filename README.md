# EPiC-submission
---

Our team has four members. Shubham, Shranayak, Rushi and Arpit. In our approach, we first sampled all data to 200 Hz. We then extracted eight features from physiology data with the neurokit library. Then we employed a two-second delay window to adjust physiology and corresponding annotations data. Finally, we trained our data using a decision tree regression model and predicted results. 


The result directory in the repository has test results (predicted arousal and valence). Unfortunately, we could not make predictions for two files as neurokit gave NaN features for respiration rate for them. 


There are separate code files associated with each step. The file clean_physio_data.ipynb applies the neurokit library and gives features of data. We used eight features: 
heart rate from ECG data, BVP clean data, skin conductance response from GSR data, respiration rate from RSP data, cleaned skin temperature data, and the amplitudes from three muscles data. The file merge_data.ipynb samples data at 200 Hz and then merges it. The file train_model.ipynb fits the data to regression mode. The file predict_newdata.ipynb used the model to predict new data. 


Two files where we could not predict valence and arousal owing to an error generated due to neurokit:

1)  \scenario_3\fold_3\test\physiology\sub_43_vid_21
2)  \scenario_2\fold_1\test\physiology\sub_1_vid_10
