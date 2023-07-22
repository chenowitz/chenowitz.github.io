## Analyzing human activity data collected from a smartphone (via Kaggle)

**Project description:** I used a publicly available dataset from Kaggle to get a better feel for activity classification based on IMU data.

### 1. The dataset

The original dataset consisted of smartphone data from a Samsung Galaxy S II worn about the waist by 30 volunteers between the ages of 19 and 48. Each individual performed six activities: walking, walking upstairs, walking downstairs, sttting, standing, and laying. 

Triaxial accelerometer and gyroscope data was captured at a constant rate of 50Hz. The experimenters video-recorded the trials and manually labeled the activities. These sensor signals were then preprocessed through the application of noise filters and then resampled in fixed-width sliding windows of 2.56 seconds with 50% overlap (128 readings/window). The entire dataset contains samples from 10299 time steps (after resampling).

In addition, acceleration was separated into gravitational and body motion components using a Butterworth low-pass filter. A cutoff frequency of 0.3 Hz was used as the threshold for the gravitational contribution, which was assumed to be low frequency compared to body motion contributions.

The experimenters also included other features from the time and frequency domains for a total of 261 features.
 
<p align="center">
<img src="images/dog_imu_analysis/raw_data.png" description="Sample of the raw data"/>
 <em>Sample of the raw data</em>
</p>


#### 2. Class distribution and data split
The data was already pre-divided into separate train and test CSVs with approximately 70% of the data in the training set and 30% of the data in the test set.

The data are slightly biased toward stationary activities, but overall, there is not a vast discrepancy between the number of samples in the 6 classes.

<p align="center">
<img src="images/human_activity_smartphone/class_distribution_counts.png" alt="app-screen" width="500" /> </br>
</p>

### 3. Data exploration
#### Summary statistics
TODO: insert image
#### Dimensionality reduction

##### PCA
##### LDA
#### Non-linear data visualization
##### t-SNE
#### Feature selection via a Random Forest Classifier
Random Forest Classifers are often used for 
### 4. Model selection and parameters
Based on initial data exploration, it seemed like a linear model had the potential to perform well on this dataset.
#### Linear SVM
SVMs aim to 
##### Non-linear kernels - just for kicks
#### Basic Neural Network
##### Hyperparameters
##### Tuning with Optuna

### 5. Result
Overall, the final bi-directional LSTM achieved a 84% accuracy on the test set.  

The final model was trained in 40 epochs. Further epochs showed an emerging gap between training and validation sets, indicating overfitting.  

<p align="center">
<img src="images/dog_imu_analysis/accuracy_iteration_3.png" alt="app-screen" width="500"/>
</p>

However, given the relatively few number of samples in the validation set, the loss curve was still rather noisy.    

<p align="center">
<img src="images/dog_imu_analysis/loss_iteration_3.png" alt="app-screen" width="500"/>
</p>

#### Confusion matrix

<p align="center">
<img src="images/dog_imu_analysis/confusion_matrix_iteration_3.png" alt="app-screen" width="500" />
<img src="images/dog_imu_analysis/f1_score_table_iteration_3.png" alt="app-screen" width="500"/>
</p>


### Further experiments
This was intended to be a quick-and-dirty attempt at activity classification using an RNN. There is [literature](https://www.researchgate.net/publication/337629344_A_Bidirectional_LSTM_for_Estimating_Dynamic_Human_Velocities_from_a_Single_IMU) to suggest that high level feature extraction using a CNN before applying a bi-direction LSTM is beneficial to model performance in the case of a single IMU. Additionally, it would be interesting to test different LSTM variants to see which variant yielded the best performance.
 
<!---
```javascript
if (isAwesome){
  return true
}
```

### 2. Assess assumptions on which statistical inference will be based

```javascript
if (isAwesome){
  return true
}
```

### 3. Support the selection of appropriate statistical tools and techniques

<img src="images/dummy_thumbnail.jpg?raw=true"/>

### 4. Provide a basis for further data collection through surveys or experiments

Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium, totam rem aperiam, eaque ipsa quae ab illo inventore veritatis et quasi architecto beatae vitae dicta sunt explicabo. 

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/). --->
