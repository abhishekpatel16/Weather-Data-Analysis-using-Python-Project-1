# Weather-Data-Analysis-using-Python-Project-1

## Project Overview

**Project Title**: Weather Data Analysis

**Dataset**: Hourly weather data in CSV format

**Tool Used**: Python (Pandas)

## Functionalities You Will Learn

- Reading CSV files with Pandas
- Data cleaning and preprocessing
- Handling missing/null values
- Renaming columns
- Filtering and conditional selection
- Statistical analysis (mean, standard deviation, variance)
- GroupBy operations

## Project Structure

### Dataset Description
The Weather Dataset is a time-series dataset with per-hour information about the weather conditions at a specific location. It includes the following columns:
- Date/Time
- Temperature (Temp_C)
- Dew Point Temperature (Dew Point Temp_C)
- Relative Humidity (Rel Hum_%)
- Wind Speed (Wind Speed_km/h)
- Visibility (Visibility_km)
- Pressure (Press_kPa)
- Weather Conditions

### Questions Solved Using Pandas

1. **Find all the unique 'Wind Speed' values in the data**
```python
data['Wind Speed_km/h'].unique()
```

2. **Find the number of times when the 'Weather is exactly Clear'**
```python
data[data.Weather == 'Clear']
```

3. **Find the number of times when the 'Wind Speed was exactly 4 km/h'**
```python
data[data['Wind Speed_km/h'] == 4]
```

4. **Find out all the Null Values in the data**
```python
data.isnull().sum()
```

5. **Rename the column name 'Weather' of the dataframe to 'Weather Condition'**
```python
data.rename(columns = {'Weather' : 'Weather Condition'}, inplace= True)
```

6. **What is the mean 'Visibility'?**
```python
data.Visibility_km.mean()
```

7. **What is the Standard Deviation of 'Pressure'?**
```python
data.Press_kPa.std()
```

8. **What is the Variance of 'Relative Humidity'?**
```python
data['Rel Hum_%'].var()
```

9. **Find all instances when 'Snow' was recorded**
```python
data[data['Weather Condition'].str.contains('Snow')]

```

10. **Find all instances when 'Wind Speed is above 24' and 'Visibility is 25'**
```python
data[(data['Wind Speed_km/h'] > 24) & (data['Visibility_km'] == 25)]
```

11. **What is the Mean value of each column against each 'Weather Condition'?**
```python
data.groupby('Weather Condition').mean(numeric_only= True)
```

12. **What is the Minimum & Maximum value of each column against each 'Weather Condition'?**
```python
data.groupby('Weather Condition').min()
data.groupby('Weather Condition').max()
```

13. **Show all the Records where Weather Condition is Fog**
```python
data[data['Weather Condition'] == 'Fog']
```

14. **Find all instances when 'Weather is Clear' or 'Visibility is above 40'**
```python
data[(data['Weather Condition'] == 'Clear') | (data['Visibility_km'] > 40)]
```

15. **Find all instances when:**
  - A. 'Weather is Clear' and 'Relative Humidity is greater than 50'  
  - OR  
  - B. 'Visibility is above 40'
```python
data[(data['Weather Condition'] == 'Clear') & (data['Rel Hum_%'] > 50) | (data['Visibility_km'] > 40)]
```

