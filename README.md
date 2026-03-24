# 1: StandardScaler:
This method centers the data around a Mean of 0 and a Standard Deviation of 1. 
It transforms the data into a "Normal Distribution" shape.
# Formula:
$$x_{scaled} = \frac{x - \mu}{\sigma}$$
(Where $\mu$ is the Mean and $\sigma$ is the Standard Deviation)


# 2: MinMaxScaler:
This method scales the data to a fixed range, usually 0 to 1. 
It is very sensitive to outliers because it uses the absolute Minimum and Maximum values.
# Formula:
$$x_{scaled} = \frac{x - x_{min}}{x_{max} - x_{min}}$$


# 3: MaxAbsScaler:
MaxAbsScaler scales each feature by its maximum absolute value.  
It is mainly used when your data is sparse (lots of zeros) and you want to preserve the zeros.  
It scales the data into a range between -1 and 1.  

# Formula:
$$x_{scaled} = \frac{x}{|x_{max}|}$$

# 4: RobustScaler:
RobustScaler is the "Bodyguard" of scalers. 
It is used when your data has Outliers (extreme values). 
Unlike StandardScaler or MinMaxScaler, it uses the Median and Interquartile Range (IQR) instead of the Mean,
so outliers don't pull the scale away.

# Formula:
$$x_{scaled} = \frac{x - Median}{IQR}$$

(Where $IQR = 75^{th} \text{ Percentile} - 25^{th} \text{ Percentile}$) 
* Median: The middle value of the data.
* IQR: The range where the middle 50% of your data lives.
* Why use it? If you have a few crazy high or low numbers (outliers),
  this scaler ignores them and focuses on the "normal" part of the data.


# When to use which method?
Method,Best Condition to Use
MinMaxScaler,Use when you know the exact boundaries (like Image Pixels 0-255) and have no outliers.
StandardScaler,Use when your data follows a Normal Distribution (Bell Curve) and for most Linear models.
MaxAbsScaler,Use when your data is Sparse (has many Zeros) to keep the zeros as zeros.
RobustScaler,Use when your data has many Outliers that you don't want to remove.
