# MaxAbsScaler:
MaxAbsScaler scales each feature by its maximum absolute value.  
It is mainly used when your data is sparse (lots of zeros) and you want to preserve the zeros.  
It scales the data into a range between -1 and 1.  

# Formula:
$$x_{scaled} = \frac{x}{|x_{max}|}$$

# RobustScaler:
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
