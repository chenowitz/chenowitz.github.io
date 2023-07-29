## Features featured in the smartphone dataset and how they were generated
1. Separated acceleration into gravity-based and movement-based components
2. Pre-calculated several metrics and additional features for the data using the accelerometer signal
3. Processed the raw data using an FFT to gain frequency domain data

### Signal Processing and Windowing


### Features
#### Signal Magnitude Area (SMA)
For an accelerometer signal, the signal magnitude area (SMA) is calculated using the area under the magnitude of the RMS of all the three axes. It is primarily used **for distinguishing between rest and movement periods** Chung, W. Y., Purwar, A., & Sharma, A. (2008, August). It also has a proven and widely accepted linear relation with the energy expenditure (Carús, J. L., Peláez, V., López, G., & Lobato, V. (2012). <\br>
Alternatives to SMA have been suggested, including jerk-based inactivity magnitude (JIM). JIM is also calculated from the acceleration signal, but at a sampling rate of 1Hz as opposed to 50Hz, the typical rule of thumb frequency for sampling human motion.

𝑓𝑠𝑚𝑎=1𝑇∫𝑇0|𝑥(𝑡)−𝑎𝑥|+|𝑦(𝑡)−𝑎𝑦|+|𝑧(𝑡)−𝑎𝑧|𝑑𝑡

#### Entropy

#### Single-Pair Correlation
#### Jerk
#### Kurtosis

### 1. Suggest hypotheses about the causes of observed phenomena

Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium, totam rem aperiam, eaque ipsa quae ab illo inventore veritatis et quasi architecto beatae vitae dicta sunt explicabo. 

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

## Feature importance based on the smartphone dataset
The Random Forest Classifier, *X* test and *Y* test all ranked
The top 10 most important features were:
1.
2.
3.
4.
5.
6.
7.
8.
9.
10.
In general, ______ tends to be important for predicting ______

# Sources
Carús, J. L., Peláez, V., López, G., & Lobato, V. (2012). JIM: a novel and efficient accelerometric magnitude to measure physical activity. Studies in health technology and informatics, 177, 283–288.

Chung, W. Y., Purwar, A., & Sharma, A. (2008, August). Frequency domain approach for activity classification using accelerometer. In 2008 30th Annual International Conference of the IEEE Engineering in Medicine and Biology Society (pp. 1120-1123). IEEE.


For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).
