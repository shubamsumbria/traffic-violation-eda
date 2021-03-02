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
10. stop_duration - Detained time for violators approx
11. drugs_related_stop - Whether person was involved in drugs crime or not

### Libraries Used:
- <a><img src="https://pandas.pydata.org/docs/_static/pandas.svg" alt="Seaborn" align="center" width="100"/></a>
- <a><img src="https://matplotlib.org/_static/logo2_compressed.svg" alt="matplotlib" align="center" width="100"/></a>
- <a><img src="https://seaborn.pydata.org/_static/logo-wide-lightbg.svg" alt="Seaborn" align="center" width="100"/></a>
- **missingno**

### Data Cleaning:

#### Checking Missing Values in Dataset:
<a><img src="https://github.com/shubamsumbria66/traffic-violation-eda/blob/main/graphs/plot01.png?raw=true" align="center" width="720"/></a>

- As in the above graph, `country_name` and `search_type` columns contain almost all NaN values. we have to drop these two columns.
- All other columns have almost similar patterns of missing values, we have to drop rows from these columns.
- Some missing values are to remain in `driver_age` column. We have to fill these missing values using median.
- After cleaning, we again have to check the remaining missing values.

<a><img src="https://github.com/shubamsumbria66/traffic-violation-eda/blob/main/graphs/plot02.png?raw=true" align="center" width="720"/></a>

- Now our dataset looks perfect for further analysis.

### Data Analysis:

1. Age Distribution

<a><img src="https://github.com/shubamsumbria66/traffic-violation-eda/blob/main/graphs/plot03.png?raw=true" width="420"/></a>

- It can be obsev=rved that both male and female drivers aged between 20 to 40 are doing maximum violations, while those above 16 are committing them minimally. It is also evident from the plot that the trend of violations and age group for one gender group follows that of other. This implies to the fact that the violations are independent of the gender of a person, obviously considering all other parameters constant.

2. Distribution in Violation Type

<a><img src="https://github.com/shubamsumbria66/traffic-violation-eda/blob/main/graphs/plot04.png?raw=true" width="420"/></a>

- Undoubtedly, the traffic violations, as per this dataset, occur the most due to speeding issues at a bar of 60.5% of all other reasons for violations.

3. Hours in Which Speed Violated

<a><img src="https://github.com/shubamsumbria66/traffic-violation-eda/blob/main/graphs/plot06.png?raw=true" width="420"/></a>

- It is observable from the plot that for the most frequent reason of violations, i.e. 'over- speeding', most violations occur during 8:00 am and 4:00 pm, while it being lower for after midnight and late evenings.

4. Hours in Which Vehicle Stopped

<a><img src="https://github.com/shubamsumbria66/traffic-violation-eda/blob/main/graphs/plot05.png?raw=true" width="420"/></a>

- It is quite obvious that people tend to violate traffic rules for multiple reasons, be it hurry or urgency, inadequate driving skills, etc. So, for a loose analysis, considering only 'hurry' as a reason for violations, we can deduce forthwritten from this plot. It is also noteworthy that this assumption isn't entirely irrational, because 60.5% of the violations occur due to over-speeding (refer second plot). Also, this plot is high in contrast to previous bar plot, pointing to the fact that most of the overall violations at almost every hour of a day is due to 'over-speeding'. Hence, statistically, we are covering for most of the violators.
  From 10:00 pm in the night, up until 2:00 am in the morning, a high number of violations occur! A possibile explaination for this might be people returning home or travelling to parties, celebrations, etc. Another important observation can be the highest of all (on an average) violations between 8:00 am to 3:00 pm. A possibility for this may be the conventional work hours of public during these hours, and that there may arise a number of situations in this case for 'over- speeding'. One must also note the considerable dip in violations particularly at 12:00 noon in this interval. Lastly, for all of the hours in a day, females always have had far lesser violation cases than males. There can be many possibilities for this, a few of them being, there are lesser female drivers than male drivers, or the possibilities suggested above don't follow with both genders, OR maybe 'females' are just 'better drivers'!

5. Traffic Violation Distribution Based on Race

<a><img src="https://github.com/shubamsumbria66/traffic-violation-eda/blob/main/graphs/plot07.png?raw=true" width="420"/></a>

- Segregating the total violations into race of the violators, it is evident from this plot that the white, black and hispanic contribute together to almost 97% of the total violations. Among these, people with white race background violate the most with a participation of 74.4% of total. A very obvious reason for this may be the population distribution among differen race of people, i.e. since there are most white, any dataset is prone to have more observations for violations from this category. Although, it must be kept in mind that there can be multiple other reasons for this trend as well, and this is mere empirical judgement.

6. Age Group Involve in Drugs

<a><img src="https://github.com/shubamsumbria66/traffic-violation-eda/blob/main/graphs/plot08.png?raw=true" width="400"/></a>

- People in their 20s, i.e. of agegroup 20-30 are observed to be involved in drugs a lot more than those of any other age- group. This also explains the high number of violation records of this age group, as in first plot. This also gives weight to the fact that 'drugs' is an important element of the equation, and must be considered for traffic violation predictions.

7. Stop Duration Based on Race

<a><img src="https://github.com/shubamsumbria66/traffic-violation-eda/blob/main/graphs/plot09.png?raw=true" width="420"/></a>

- This mapping makes it quite obvious that people with hispanic and/ or black race background are made to stop the most, for a potential violation case than any other race. Secondly, it is quite surprising that although white people have recorded to be violating traffic rules the most, they arn't stopped comparitively enough.

8. Correlation Heatmap

<a><img src="https://github.com/shubamsumbria66/traffic-violation-eda/blob/main/graphs/plot11.png?raw=true" width="420"/></a>

- This figure is representative of dependency of 'drug- based' cases with searches conducted for various types of violation types or reasons. As is followed in all of the violation types, most of the total searches conducted do not turn out to be of people involved in drugs. Although a small proportion of them do fall in 'drug- involvement category'. It is interesting to note that this relation is independent of the type of traffic violation commited.

9. Total Search Conduct vs. Drug Related Stop

<a><img src="https://github.com/shubamsumbria66/traffic-violation-eda/blob/main/graphs/plot10.png?raw=true" width="420"/></a>

- This bar plot also follows similar trend to that of previos figure, except only the factorisation of total searches committed into time (yearly) in one and into violation type in the other.

10. Arrested vs. Not Arrested (Before Search Conduct)

<a><img src="https://github.com/shubamsumbria66/traffic-violation-eda/blob/main/graphs/plot12.png?raw=true" width="420"></a>


11. Arrested vs. Not Arrested (After Search Conduct)

<a><img src="https://github.com/shubamsumbria66/traffic-violation-eda/blob/main/graphs/plot13.png?raw=true" width="350"></a>
