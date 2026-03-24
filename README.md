# MaxAbsScaler:
MaxAbsScaler scales each feature by its maximum absolute value.  
It is mainly used when your data is sparse (lots of zeros) and you want to preserve the zeros.  
It scales the data into a range between -1 and 1.  

# Formula:
$$x_{scaled} = \frac{x}{|x_{max}|}$$


