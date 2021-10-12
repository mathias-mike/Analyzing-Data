# Ford GoBike Trip Data Analysis
## by Michael Mathias


## Dataset

The Ford GoBike Trip dataset includes information about individual rides made in a bike-sharing system covering the greater San Francisco Bay area. Some cleaning was done on the dataset to address the following issues;
#### Quality Issues
* Erroneous data types `["start_time", "end_time", "start_station_id", "end_station_id", "bike_id", "member_birth_year", "user_type", "member_gender", "bike_share_for_all_trip"]`.
* Inconsistent column names `["user_type", "member_birth_year", "member_gender"]`.
* Multiple columns used to encode same variable `"duration_sec"` and `["start_time", "end_time"]`.
* Difficulty interpreting duration.
* Engineer new features, `user_age`, `distance`, `time_of_dat`, `day_of_week`, `log_distance` and `log_user_age`.

#### Tidy Issues
* Transfer station information to station table.

## Summary of Findings

In the exploration of the dataset I found that most people tend to spend around 4 - 5  and around 10 minutes on bike trips and that most bike trips are taking 8 AM and 5 PM which is when most people go to work and leave from work respectively, this kind of shows that most user of the dataset set are actually working people who use this bike share program as a means to commute to work. Futher validation of this was shown when I ploted this distribution in a heatmap in a bivariate case of both time_of_day and day_of_week, the peak of activity around 8 AM and 5 PM vanished on weekends. I also observed that unsubscribed customers tend to spend more time on bike trips than subscribed customers and that most customers tend to use the bike share service to get some exercise and they spend more time per trip on weekends than on weekdays.

Assides the main findings, I also observed how far spread the Ford gobike stations are covering some really large area, some more than 60km but then I observed that most people, though, tend to return bikes to stations in close proximity of where they took it some even back to the initial start station. And I also noticed old people use this service as well, even people older than 120 years.


## Key Insights for Presentation

For the presentation, I focus on just the relationship between user_type, time_of_day, day_of_week and duration and I will also try to see how this features relate to user_age, I will leave out most of the other variables. I start by introducing the duration variable, followed by the pattern in the distribution of user_type, time_of_day and day_of_week. Then I will plot the relationship between each of this variable with duration.

Afterwards I will show relationship between user_age variable, time_of_day and day_of_week.