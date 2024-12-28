## Module 1 - BiteDetection
In this project, I detected which second bite was taken and calculated the number of chews performed on every bite.

We collected smartwatch data and plotted it to verify which parameters to use.​ Graphs looked like below:
<img width="900" alt="image" src="https://github.com/user-attachments/assets/6b452451-9651-45e4-bff9-c4fc74d48e92" />
<img width="900" alt="image" src="https://github.com/user-attachments/assets/276326c4-c656-41f7-85f9-ca6be512edb0" />
<img width="900" alt="image" src="https://github.com/user-attachments/assets/53387e0a-51b1-4764-ba41-72681e4a28a3" />

We finalized on 4 parameters: Gravity, acceleration, quaternion, rotation.

Applied low pass filter.

Sampling rate of 100 Hz and step size of 50.
Window of 250 for a bite.
From complete data we recognized every set of data(windows) in which bite is taken we calculated the features and labeled them as “Bite Taken” = YES.
Also, collected random data in which we are not taking bite and marked them as “Bite Taken” = NO.
Now we have the processed data.
Trained it using RandomForestClassifier. Accuracy of 97.65.

## Testing of Module 1
If new data is provided as input. Then the algorithm try to detect the window in which the bite was taken.
Process data
Find features and match it.
RandomForestClassifier detects if bite was taken in the window of data or not.
Calculated Seconds at which bites were taken.

## Module 2 - Chew rate calculation

Collected data from airpod.
Processed it using low pass filter.
Detected the jitters to detect the bites.

![image](https://github.com/user-attachments/assets/d9711067-9a6b-43e3-94c0-3fe8168c9a89)

# OUTPUT
Chewing Rate: 51.45 motions/min​
FromSeconds:0 Seconds At which current bite was Taken: 2.75​
Number of Chews in the interval: 2​
​
Chewing Rate: 51.45 motions/min​
FromSeconds:2.75 Seconds At which current bite was Taken: 11.5​
Number of Chews in the interval: 8​
![image](https://github.com/user-attachments/assets/3daa0353-35b3-4ee3-9a31-8e86490efc45)








