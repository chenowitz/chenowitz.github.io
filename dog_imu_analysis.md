## Analyzing dog IMU from Kaggle

**Project description:** I used a publicly available dataset from Kaggle to get a better feel for activity classification based on IMU data.

### 1. Preprocessing the dataset

The original dataset consisted of IMU data from 45 dogs of different breeds. 
The authors of the original study chose to perform classification using feature engineering followed by a linear classifier. I wanted to see if I could acheive comparable results using an RNN without additional feature engineering.  

The original dataset was a little wonky to interpret. The experimenters assigned the dogs one of 7 tasks and then manually annotated behaviors that the dog actually performed during the assigned task. They did not make all of these annotated behaviors actual classes for their activity classification.

<img src="images/dog_imu_analysis/raw_data.png"/>
Sample of the raw data  

<img src="images/dog_imu_analysis/time_series_dog_16_ax.png"/>
Time-series data for an individual dog

To simplify matters, I decided that all samples where one of the annotated behaviors was the same as the assigned task qualified as a legitimate instance of that activity.

<img src="images/dummy_thumbnail.jpg?raw=true"/>
Instance where the assigned task was "walk" and the experimenters noted that one of three observed behaviors was walking

#### Class distribution and data split
The distribution between activity classes was relatively uniform. Therefore, I didn't take any additional measures to change the class distribution of the dataset.  

<p align="center">
<img src="images/dog_imu_analysis/class_distribution_bar_graph.png" alt="app-screen" width="500" />
<img src="images/dog_imu_analysis/class_distribution_numbers.png" alt="app-screen" width="500"/>
</p>

A typical train/validation/test breakdown is usually 80%/10%/10%, meaning that there would be roughly 37 dogs in the training set, 4 in the validation set, and 4 in the test set.

Due to the low number of samples, I chose to adjust the data split slightly to include 33 dogs in the training set, 6 in the validation set, and 6 in the test set.

### Model selection and parameters
RNNs have the ability to____. I chose an LSTM because_____ and specifically, 

### Result
Overall, the final bi-directional LSTM achieved a X% accuracy on the test set.  

The final model was trained in X epochs. Further epochs showed an emerging gap between training and validation sets, indicating overfitting.  

<p align="center">
<img src="images/dog_imu_analysis/accuracy_iteration_3" alt="app-screen" width="500"/>
</p>

However, given the relatively few number of samples in the validation set, the loss curve is rather noisy.    

<p align="center">
<img src = "images/dog_imu_analysis/loss_iteration_3" alt="app-screen" width="500"/>
</p>

#### Confusion matrix

<p align="center">
<img src="images/dog_imu_analysis/class_distribution_bar_graph.png" alt="app-screen" width="500" />
<img src="images/dog_imu_analysis/class_distribution_numbers.png" alt="app-screen" width="500"/>
</p>


### Further experiments
This was intended to be a quick-and-dirty attempt at activity classification using an RNN. There is literature to suggest that high level feature extraction using a CNN before applying a bi-direction LSTM is beneficial to model performance in the case of a single IMU. (https://www.researchgate.net/publication/337629344_A_Bidirectional_LSTM_for_Estimating_Dynamic_Human_Velocities_from_a_Single_IMU)
 

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

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).
