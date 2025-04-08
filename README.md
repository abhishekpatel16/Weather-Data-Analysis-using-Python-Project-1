# Weather-Data-Analysis-using-Python-Project-1
Weather Data Analysis using Python 🌦️
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
- Weather

![data](https://github.com/abhishekpatel16/Weather-Data-Analysis-using-Python-Project-1/blob/main/images/data.png)


### Questions Solved Using Pandas

1. **Find all the unique 'Wind Speed' values in the data**
```python
data['Wind Speed_km/h'].unique()
```
![Q.1](https://github.com/abhishekpatel16/Weather-Data-Analysis-using-Python-Project-1/blob/main/images/Q.1.png)


2. **Find the number of times when the 'Weather is exactly Clear'**
```python
data[data.Weather == 'Clear']
```
![Q.2](https://github.com/abhishekpatel16/Weather-Data-Analysis-using-Python-Project-1/blob/main/images/Q.2.png)


3. **Find the number of times when the 'Wind Speed was exactly 4 km/h'**
```python
data[data['Wind Speed_km/h'] == 4]
```
![Q.3](https://github.com/abhishekpatel16/Weather-Data-Analysis-using-Python-Project-1/blob/main/images/Q.3.png)


4. **Find out all the Null Values in the data**
```python
data.isnull().sum()
```
![Q.4](https://github.com/abhishekpatel16/Weather-Data-Analysis-using-Python-Project-1/blob/main/images/Q.4.png)


5. **Rename the column name 'Weather' of the dataframe to 'Weather Condition'**
```python
data.rename(columns = {'Weather' : 'Weather Condition'}, inplace= True)
```
![Q.5](https://github.com/abhishekpatel16/Weather-Data-Analysis-using-Python-Project-1/blob/main/images/Q.5.png)


6. **What is the mean 'Visibility'?**
```python
data.Visibility_km.mean()
```
![Q.6](https://github.com/abhishekpatel16/Weather-Data-Analysis-using-Python-Project-1/blob/main/images/Q.6.png)


7. **What is the Standard Deviation of 'Pressure'?**
```python
data.Press_kPa.std()
```
![Q.7](https://github.com/abhishekpatel16/Weather-Data-Analysis-using-Python-Project-1/blob/main/images/Q.7.png)


8. **What is the Variance of 'Relative Humidity'?**
```python
data['Rel Hum_%'].var()
```
![Q.8](https://github.com/abhishekpatel16/Weather-Data-Analysis-using-Python-Project-1/blob/main/images/Q.8.png)


9. **Find all instances when 'Snow' was recorded**
```python
data[data['Weather Condition'].str.contains('Snow')]
```
![Q.9](https://github.com/abhishekpatel16/Weather-Data-Analysis-using-Python-Project-1/blob/main/images/Q.9.png)


10. **Find all instances when 'Wind Speed is above 24' and 'Visibility is 25'**
```python
data[(data['Wind Speed_km/h'] > 24) & (data['Visibility_km'] == 25)]
```
![Q.10](https://github.com/abhishekpatel16/Weather-Data-Analysis-using-Python-Project-1/blob/main/images/Q.10.png)


11. **What is the Mean value of each column against each 'Weather Condition'?**
```python
data.groupby('Weather Condition').mean(numeric_only= True)
```
![Q.11](https://github.com/abhishekpatel16/Weather-Data-Analysis-using-Python-Project-1/blob/main/images/Q.11.png)


12. **What is the Minimum & Maximum value of each column against each 'Weather Condition'?**
```python
data.groupby('Weather Condition').min()
data.groupby('Weather Condition').max()
```
![Q.12](https://github.com/abhishekpatel16/Weather-Data-Analysis-using-Python-Project-1/blob/main/images/Q.12%20a.png)
![Q.12](https://github.com/abhishekpatel16/Weather-Data-Analysis-using-Python-Project-1/blob/main/images/Q.12%20b.png)



13. **Show all the Records where Weather Condition is Fog**
```python
data[data['Weather Condition'] == 'Fog']
```
![Q.13](https://github.com/abhishekpatel16/Weather-Data-Analysis-using-Python-Project-1/blob/main/images/Q.13.png)


14. **Find all instances when 'Weather is Clear' or 'Visibility is above 40'**
```python
data[(data['Weather Condition'] == 'Clear') | (data['Visibility_km'] > 40)]
```
![Q.14](https://github.com/abhishekpatel16/Weather-Data-Analysis-using-Python-Project-1/blob/main/images/Q.14.png)


15. **Find all instances when:**
  - A. 'Weather is Clear' and 'Relative Humidity is greater than 50'  
  - OR  
  - B. 'Visibility is above 40'
```python
data[(data['Weather Condition'] == 'Clear') & (data['Rel Hum_%'] > 50) | (data['Visibility_km'] > 40)]
```
![Q.15](https://github.com/abhishekpatel16/Weather-Data-Analysis-using-Python-Project-1/blob/main/images/Q.15.png)


Sure! Here's the complete **README.md** code for your **Weather Data Analysis using Python** project, ready to copy and paste into your GitHub repository:

```markdown
# Weather Data Analysis using Python 🌦️

*A Beginner-Friendly Project in Data Analytics (Part of Big Data Analysis)*

---

## 📌 Project Overview

**Title**: Weather Data Analysis using Python  
**Dataset**: Hourly weather data (CSV format)  
**Tools Used**: Python, Pandas  

This project focuses on analyzing hourly weather data from a CSV file using Python and the Pandas library. It's ideal for beginners learning data analysis, data cleaning, and basic statistical techniques.

---

## 📁 Dataset Description

The Weather Dataset is a **time-series dataset** that provides **hourly weather information** from a specific location. The dataset includes the following columns:

- `Date/Time`
- `Temp_C` – Temperature in Celsius
- `Dew Point Temp_C`
- `Rel Hum_%` – Relative Humidity in percentage
- `Wind Speed_km/h`
- `Visibility_km`
- `Press_kPa` – Atmospheric Pressure
- `Weather` – Describes weather conditions

📸 **Sample Data Preview**:  
![data](https://github.com/abhishekpatel16/Weather-Data-Analysis-using-Python-Project-1/blob/main/images/data.png)

---

## 🚀 What You'll Learn

By completing this project, you will gain hands-on experience with:

- Reading and loading data with Pandas (`read_csv`)
- Inspecting and analyzing datasets
- Handling missing/null values
- Renaming columns
- Filtering with conditions
- Basic statistics (mean, std dev, variance)
- Grouping data with `groupby()`
- String operations with Pandas

---

## 🧠 Analysis and Insights (Questions Solved)

### 1. Find all the unique 'Wind Speed' values
```python
data['Wind Speed_km/h'].unique()
```
![Q.1](https://github.com/abhishekpatel16/Weather-Data-Analysis-using-Python-Project-1/blob/main/images/Q.1.png)

---

### 2. Count the number of times the weather was exactly 'Clear'
```python
data[data.Weather == 'Clear']
```
![Q.2](https://github.com/abhishekpatel16/Weather-Data-Analysis-using-Python-Project-1/blob/main/images/Q.2.png)

---

### 3. Find how many times wind speed was exactly 4 km/h
```python
data[data['Wind Speed_km/h'] == 4]
```
![Q.3](https://github.com/abhishekpatel16/Weather-Data-Analysis-using-Python-Project-1/blob/main/images/Q.3.png)

---

### 4. Check for null values in the dataset
```python
data.isnull().sum()
```
![Q.4](https://github.com/abhishekpatel16/Weather-Data-Analysis-using-Python-Project-1/blob/main/images/Q.4.png)

---

### 5. Rename the column 'Weather' to 'Weather Condition'
```python
data.rename(columns = {'Weather' : 'Weather Condition'}, inplace=True)
```
![Q.5](https://github.com/abhishekpatel16/Weather-Data-Analysis-using-Python-Project-1/blob/main/images/Q.5.png)

---

### 6. Calculate the mean visibility
```python
data.Visibility_km.mean()
```
![Q.6](https://github.com/abhishekpatel16/Weather-Data-Analysis-using-Python-Project-1/blob/main/images/Q.6.png)

---

### 7. Find the standard deviation of pressure
```python
data.Press_kPa.std()
```
![Q.7](https://github.com/abhishekpatel16/Weather-Data-Analysis-using-Python-Project-1/blob/main/images/Q.7.png)

---

### 8. Compute the variance of relative humidity
```python
data['Rel Hum_%'].var()
```
![Q.8](https://github.com/abhishekpatel16/Weather-Data-Analysis-using-Python-Project-1/blob/main/images/Q.8.png)

---

### 9. Find all instances when 'Snow' was recorded
```python
data[data['Weather Condition'].str.contains('Snow')]
```
![Q.9](https://github.com/abhishekpatel16/Weather-Data-Analysis-using-Python-Project-1/blob/main/images/Q.9.png)

---

### 10. Filter records where wind speed > 24 km/h and visibility = 25 km
```python
data[(data['Wind Speed_km/h'] > 24) & (data['Visibility_km'] == 25)]
```
![Q.10](https://github.com/abhishekpatel16/Weather-Data-Analysis-using-Python-Project-1/blob/main/images/Q.10.png)

---

### 11. Mean of each column for every weather condition
```python
data.groupby('Weather Condition').mean(numeric_only=True)
```
![Q.11](https://github.com/abhishekpatel16/Weather-Data-Analysis-using-Python-Project-1/blob/main/images/Q.11.png)

---

### 12. Minimum & Maximum values of each column by weather condition
```python
data.groupby('Weather Condition').min()
data.groupby('Weather Condition').max()
```
![Q.12a](https://github.com/abhishekpatel16/Weather-Data-Analysis-using-Python-Project-1/blob/main/images/Q.12%20a.png)
![Q.12b](https://github.com/abhishekpatel16/Weather-Data-Analysis-using-Python-Project-1/blob/main/images/Q.12%20b.png)

---

### 13. Show all records where the weather condition is 'Fog'
```python
data[data['Weather Condition'] == 'Fog']
```
![Q.13](https://github.com/abhishekpatel16/Weather-Data-Analysis-using-Python-Project-1/blob/main/images/Q.13.png)

---

### 14. Find all instances where weather is 'Clear' or visibility is above 40
```python
data[(data['Weather Condition'] == 'Clear') | (data['Visibility_km'] > 40)]
```
![Q.14](https://github.com/abhishekpatel16/Weather-Data-Analysis-using-Python-Project-1/blob/main/images/Q.14.png)

---

### 15. Find all instances where:
- Weather is 'Clear' **and** Relative Humidity > 50  
**OR**  
- Visibility > 40
```python
data[(data['Weather Condition'] == 'Clear') & (data['Rel Hum_%'] > 50) | (data['Visibility_km'] > 40)]
```
![Q.15](https://github.com/abhishekpatel16/Weather-Data-Analysis-using-Python-Project-1/blob/main/images/Q.15.png)

---

## ✅ Conclusion

This project is a great starting point for beginners in Data Science and Analytics. By analyzing real-world weather data, you get hands-on practice in cleaning, exploring, and extracting insights using Python and Pandas.

---

**Feel free to fork, modify, and enhance the project! 🚀**

```


