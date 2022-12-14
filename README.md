# AI-X_Deep-Learning_anomaly-detection  
["https://www.youtube.com/watch?v=_TxCFetAPIY"](https://www.youtube.com/watch?v=_TxCFetAPIY)
## Title: Anomaly Detection
### Members: 
- 장신의, 경영학부, 2019045514, zzzcyy@naver.com
- 유여홍, 경영학부, 2019071785, L1511742072@gmail.com
- 강호묘, 경영학부, 2019079434, kanghomyo116@gmail.com
- 유금양, 경영학부, 2019066880, 1051265066@qq.com
### I. Proposal (Option A) 
- Motivation: Why are you doing this?   
Since the popularization of electronic information, a large number of sensor devices have been installed in various industrial equipment to monitor the operating status of the equipment. But for a long time, people lack effective means to utilize the large amount of data generated by these sensors. With the development of AI technology, people have new means to process and utilize large amounts of data.In this project, our team will try to use machine learning methods to detect anomalies in some data generated in industrial production.
- What do you want to see at the end?  
We first train the model using part of the data as the training set. Then use the trained model to perform anomaly detection on the test set data. We expect to get higher F1 score and RECALL score.

### II. Datasets 
- Describing your dataset  
This dataset has 11 features.  
datetime - Represents dates and times of the moment when the value is written to the database (YYYY-MM-DD hh:mm:ss)  
Accelerometer1RMS - Shows a vibration acceleration (Amount of g units)  
Accelerometer2RMS - Shows a vibration acceleration (Amount of g units)  
Current - Shows the amperage on the electric motor (Ampere)  
Pressure - Represents the pressure in the loop after the water pump (Bar)  
Temperature - Shows the temperature of the engine body (The degree Celsius)  
Thermocouple - Represents the temperature of the fluid in the circulation loop (The degree Celsius)  
Voltage - Shows the voltage on the electric motor (Volt)  
RateRMS - Represents the circulation flow rate of the fluid inside the loop (Liter per minute)  
anomaly - Shows if the point is anomalous (0 or 1)  
changepoint - Shows if the point is a changepoint for collective anomalies (0 or 1)  
![image](https://github.com/zzzcyy/AI-X_Deep-Learning_anomaly-detection/blob/main/img/data.png)  
![image](https://github.com/zzzcyy/AI-X_Deep-Learning_anomaly-detection/blob/main/img/anomaly_display.png)
[https://github.com/waico/SKAB#datasets](url)
### III. Methodology
- Explaining your choice of algorithms (methods)  
IsolationForest Algorithm: Isolation Forest is an algorithm for data anomaly detection. It detects anomalies using isolation (how far a data point is from the rest of the data), rather than modeling the normal points. It was initially developed by Fei Tony Liu and Zhi-Hua Zhou in 2007. The significance of his research lies in its deviation from the mainstream philosophy underpinning most existing anomaly detectors at the time, where all the normal instances are profiled before anomalies are identified as instances that do not conform to the distribution of the normal instances. Isolation forest introduces a different method that explicitly isolates anomalies using binary trees, demonstrating a new possibility of a faster anomaly detector that directly targets anomalies without profiling all the normal instances. The algorithm has a linear time complexity with a low constant and a low memory requirement, which works well with high volume data.

### IV. Evaluation & Analysis
- Graphs, tables, any statistics (if any)
- (1) Evaluation method  
For the binary classification problem of anomaly detection. Typically there are four situations.In the first case, the prediction is positive and the actual positive is also called true positive (TP). In the second case, the prediction is positive but the actual negative is called false positive (FP). In the third case, The prediction is negative and the actual positive is called false negative (FN). In the last case, the prediction is negative and the actual is negative, which is called true negative (TN). Each sample can only belong to these four cases A certain kind, there will be no other possibility.Next we can define accuracy, recall, precision and F1score.  
![image](https://github.com/zzzcyy/AI-X_Deep-Learning_anomaly-detection/blob/main/img/accuracy.PNG)  
![image](https://github.com/zzzcyy/AI-X_Deep-Learning_anomaly-detection/blob/main/img/precision.PNG)  
![image](https://github.com/zzzcyy/AI-X_Deep-Learning_anomaly-detection/blob/main/img/recall.PNG)  
![image](https://github.com/zzzcyy/AI-X_Deep-Learning_anomaly-detection/blob/main/img/f1.PNG)  
For anomaly detection tasks, the larger the value of recall, the stronger the ability of the model to detect anomalies. The larger the F1score, it means that the model has a good ability to identify abnormal points and normal points.  
- (2) Graphs and results  
![image](https://github.com/zzzcyy/AI-X_Deep-Learning_anomaly-detection/blob/main/img/result.png)  
This image shows the result of the model prediction. Orange lines represent outliers predicted by the model, and blue lines represent true outliers. We can see that the model can distinguish outliers very well, but at the same time it will also misclassify some normal points as outliers. The precision corresponding to this picture is 0.58, the recall is 0.84, and the F1score is 0.68.  
- (3) Change the parameters of the model  
The isolation forest model has four main parameters. n_estimator, contamination, max_feature and max_samples.
![image](https://github.com/zzzcyy/AI-X_Deep-Learning_anomaly-detection/blob/main/img/parameters.PNG)  
![image](https://github.com/zzzcyy/AI-X_Deep-Learning_anomaly-detection/blob/main/img/search_model.PNG)  
We try to process the data with different parameter values and try to find the optimal model parameters. We found the best configuration are n_estimator:100, contamination:0.16, max_feature:0.2, and max_samples:0.9. Under this parameter setting, the best recall is 0.92, and the best F1score is 0.73.

### V. Related Work (e.g., existing studies)
- Tools, libraries, blogs, or any documentation that you have used to do this project.  
Dataset: [https://github.com/waico/SKAB#datasets](url)  
Method: Liu F T, Ting K M, Zhou Z H. Isolation forest[C]//2008 eighth ieee international conference on data mining. IEEE, 2008: 413-422.
### VI. Conclusion: Discussion  
In this project, we used the isolation forest algorithm to detect anomalies on a small dataset. As far as the final result is concerned, the effect is very general. But in the process, we became more familiar with the data processing method and the use of the sklearn library. We also try to adjust the parameters of the model to improve the effect of the model.  
Member 1：code    
Member 2: code  
Member 3: analysis  
Member 4: youtube record
