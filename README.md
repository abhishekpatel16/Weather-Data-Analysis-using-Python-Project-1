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
weather['Wind Speed_km/h'].unique()
```

2. **Find the number of times when the 'Weather is exactly Clear'**
```python
weather[weather['Weather'] == 'Clear'].shape[0]
```

3. **Find the number of times when the 'Wind Speed was exactly 4 km/h'**
```python
weather[weather['Wind Speed_km/h'] == 4].shape[0]
```

4. **Find out all the Null Values in the data**
```python
weather.isnull().sum()
```

5. **Rename the column name 'Weather' of the dataframe to 'Weather Condition'**
```python
weather.rename(columns={'Weather': 'Weather Condition'}, inplace=True)
```

6. **What is the mean 'Visibility'?**
```python
weather['Visibility_km'].mean()
```

7. **What is the Standard Deviation of 'Pressure'?**
```python
weather['Press_kPa'].std()
```

8. **What is the Variance of 'Relative Humidity'?**
```python
weather['Rel Hum_%'].var()
```

9. **Find all instances when 'Snow' was recorded**
```python
weather[weather['Weather Condition'].str.contains('Snow')]
```

10. **Find all instances when 'Wind Speed is above 24' and 'Visibility is 25'**
```python
weather[(weather['Wind Speed_km/h'] > 24) & (weather['Visibility_km'] == 25)]
```

11. **What is the Mean value of each column against each 'Weather Condition'?**
```python
weather.groupby('Weather Condition').mean()
```

12. **What is the Minimum & Maximum value of each column against each 'Weather Condition'?**
```python
weather.groupby('Weather Condition').min()
weather.groupby('Weather Condition').max()
```

13. **Show all the Records where Weather Condition is Fog**
```python
weather[weather['Weather Condition'] == 'Fog']
```

14. **Find all instances when 'Weather is Clear' or 'Visibility is above 40'**
```python
weather[(weather['Weather Condition'] == 'Clear') | (weather['Visibility_km'] > 40)]
```

15. **Find all instances when:**
  - A. 'Weather is Clear' and 'Relative Humidity is greater than 50'  
  - OR  
  - B. 'Visibility is above 40'
```python
weather[((weather['Weather Condition'] == 'Clear') & (weather['Rel Hum_%'] > 50)) | (weather['Visibility_km'] > 40)]
```

