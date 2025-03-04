# Measures of Central Tendency

### Mean

$$
\overline{x} = \frac{1}{n} \sum_{i=1}^{n} x_i
$$
where \( \overline{x} \) is the mean, \( x_i \) are the individual values, and \( n \) is the number of values.

### Median

If the number of observations (n) is even, the median is the average of the two middle values:
$$
\text{Median} = \frac{x_{\left( \frac{n}{2} \right)} + x_{\left( \frac{n}{2} + 1 \right)}}{2}
$$


### Mode

### Percentile
Number of values below a certain threshold.  
40 percentile means 40 percent of values lie below that threshold.  

### Quartiles  
Q1 - 25th percentile  - lower percentile    
Q2 - 50th percentile  
Q3 - 75th percentile  - upper percentile



### Inter Quartile Range (IQR)  
IQR = Q3 - Q1

### Min

### Max

# Finding Outliers using Quartiles

### Lower Bound  
Q1 - 1.5* IQR (Inter quartile range)

### Upper Bound
Q3 + 1.5*IQR

### Outliers
values lower than LB or higher than UB.

# Measures of Dispersion

### Range
### Variance  
The sample variance is given by:
$$
s^2 = \frac{1}{n-1} \sum_{i=1}^{n} (x_i - \overline{x})^2
$$
where \( s^2 \) is the sample variance, \( x_i \) are the individual values, \( \overline{x} \) is the sample mean, and \( n \) is the number of values in the sample.

### standard deviation  
The sample standard deviation is given by:
$$
s = \sqrt{\frac{1}{n-1} \sum_{i=1}^{n} (x_i - \overline{x})^2}
$$
where \( s \) is the sample standard deviation, \( x_i \) are the individual values, \( \overline{x} \) is the sample mean, and \( n \) is the number of values in the sample.

### z- score (used for standardization)  
The Z-score is given by:
$$
z = \frac{x - \mu}{\sigma}
$$
where \( z \) is the Z-score, \( x \) is the individual value, \( \mu \) is the mean, and \( \sigma \) is the standard deviation.


### Confidence Interval (CI)

# Correlation Coefficient(-1 to +1)


### Pearson correlation coefficient
### Speaman's rank correlation


```python

```
