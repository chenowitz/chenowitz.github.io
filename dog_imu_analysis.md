## Analyzing dog IMU from Kaggle

**Project description:** I used a publicly available dataset from Kaggle to get a better feel for activity classification based on IMU data.

### 1. Preprocessing the dataset

The original dataset consisted of IMU data from 45 dogs of different breeds. 
The authors of the original study chose to perform classification using feature engineering followed by a linear classifier. I wanted to see if I could acheive comparable results using an LSTM.  

The original dataset was a little wonky to interpret in that the experimenters assigned the dogs one of 7 tasks and then manually annotated behaviors that the dog was actually exhibiting during that assigned task. The number of classes that they chose to classify in their paper doesn't completely match all the behaviors that they annotated in their raw data. 

<img src="images/dog_imu_analysis/raw_data?raw=true"/>
Sample of the raw data

To simplify matters, I decided that all samples where one of the annotated behaviors was the same as the assigned task qualified as a legitimate instance of that activity.

<img src="images/dummy_thumbnail.jpg?raw=true"/>
Instance where the assigned task was "walk" and the experimenters noted that one of three observed behaviors was walking

#### Class distribution and data split
The distribution between activity classes was relatively uniform. Therefore, no corrections were made for a skewed dataset.
<img src="images/dog_imu_analysis/class_distribution_bar_graph.png?raw=true"/>
<img src="images/dog_imu_analysis/class_distribution_numbers.png?raw=true"/>

A typical train/validation/test breakdown is usually 80%/10%/10%, meaning that there would be roughly 37 dogs in the training set, 4 in the validation set, and 4 in the test set.

However, the learning curves from one particular iteration suggested that the validation data was underrepresenatived of the training data. 

I chose to adjust the data split to 33 dogs in the training set, 6 in the validation set, and 6 in the test set.

### Model selection and parameters



### Result
 

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
