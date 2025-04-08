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


**By - Abhishek Patel**

**Email ID: abhishek.skpatel@gmail.com** |
**LinkedIn: [linkedin.com/in/abhishekpatel16/](https://www.linkedin.com/in/abhishekpatel16/)**

```
