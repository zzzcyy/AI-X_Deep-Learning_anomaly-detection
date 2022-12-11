# AI-X_Deep-Learning_anomaly-detection
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

### V. Related Work (e.g., existing studies)
- Tools, libraries, blogs, or any documentation that you have used to do this project.
### VI. Conclusion: Discussion
