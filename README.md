# Traffic Violation EDA 
This is Python based Exploratory Data Analysis on traffic dataset to find out different trends in order to reduce traffic violations.

### About Dataset:
This dataset contains around 65k+ traffic related violation records.

#### Attribute Information:
1. stop_date - Date of violation
2. stop_time - Time of violation
3. driver_gender - Gender of violators
4. driver_age - Age of violators
5. driver_race -Race of violators
6. violation - Category of violation
7. search_conducted - Whether search is conducted or not in True and False form
8. stop_outcome - Result of violation
9. is_arrested - Whether person was arrested or not in True and False form
10. stop_duration- Detained time for violators approx
11. drugs_related_stop - Whether person was involved in drugs crime or not

### Libraries Used:
- <a><img src="https://pandas.pydata.org/docs/_static/pandas.svg" alt="Seaborn" align="center" width="100"/></a>
- <a><img src="https://matplotlib.org/_static/logo2_compressed.svg" alt="matplotlib" align="center" width="100"/></a>
- <a><img src="https://seaborn.pydata.org/_static/logo-wide-lightbg.svg" alt="Seaborn" align="center" width="100"/></a>
- **missingno**

### Data Cleaning:

#### Checking Missing Values in Dataset:
<a><img src="https://github.com/shubamsumbria66/traffic-violation-eda/blob/main/graphs/plot01.png?raw=true" align="center" width="720"/></a>

- As in the above graph, *country_name* and *search_type* columns contain almost all NaN values. we have to drop these two columns.
- All other columns have almost similar patterns of missing values, we have to drop rows from these columns.
- Some missing values are to remain in *driver_age* column. We have to fill these missing values using median.
- After cleaning, we again have to check the remaining missing values.

<a><img src="https://github.com/shubamsumbria66/traffic-violation-eda/blob/main/graphs/plot02.png?raw=true" align="center" width="720"/></a>

- Now our dataset looks perfect for further analysis.

### Data Analysis:

1. Age Distribution

<a><img src="https://github.com/shubamsumbria66/traffic-violation-eda/blob/main/graphs/plot03.png?raw=true" width="420"/></a>

--

2. Distribution in Violation Type

<a><img src="https://github.com/shubamsumbria66/traffic-violation-eda/blob/main/graphs/plot04.png?raw=true" width="420"/></a>

--

3. Hours in Which Vehicle Stopped

<a><img src="https://github.com/shubamsumbria66/traffic-violation-eda/blob/main/graphs/plot05.png?raw=true" width="420"/></a>

--

4. Hours in Which Speed Violated

<a><img src="https://github.com/shubamsumbria66/traffic-violation-eda/blob/main/graphs/plot06.png?raw=true" width="420"/></a>

--

5. Traffic Violation Distribution Based on Race

<a><img src="https://github.com/shubamsumbria66/traffic-violation-eda/blob/main/graphs/plot07.png?raw=true" width="420"/></a>

--

6. Age Group Involve in Drugs

<a><img src="https://github.com/shubamsumbria66/traffic-violation-eda/blob/main/graphs/plot08.png?raw=true" width="400"/></a>

--

7. Stop Duration Based on Race

<a><img src="https://github.com/shubamsumbria66/traffic-violation-eda/blob/main/graphs/plot09.png?raw=true" width="420"/></a>

--

8. Total Search Conduct vs. Drug Related Stop

<a><img src="https://github.com/shubamsumbria66/traffic-violation-eda/blob/main/graphs/plot10.png?raw=true" width="420"/></a>

--

9. Correlation Heatmap

<a><img src="https://github.com/shubamsumbria66/traffic-violation-eda/blob/main/graphs/plot11.png?raw=true" width="420"/></a>

--

10. Arrested vs. Not Arrested (Before Search Conduct)

<a><img src="https://github.com/shubamsumbria66/traffic-violation-eda/blob/main/graphs/plot12.png?raw=true" width="420"></a>

--

11. Arrested vs. Not Arrested (After Search Conduct)

<a><img src="https://github.com/shubamsumbria66/traffic-violation-eda/blob/main/graphs/plot13.png?raw=true" width="350"></a>

--

### Conclusion:
--

