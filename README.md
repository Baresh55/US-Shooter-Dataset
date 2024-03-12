1.	BETWEEN 1970 AND 2022, WHICH YEARS HAD THE HIGHEST SHOOTING INCIDENTS?

Considering that the relevant data was in 2 different tables i.e. incident and shooter, my query utilized the incident id execute a LEFT. I used the COUNT (*) function to count the number of rows and thereby establish an incident count which I grouped by year and ordered in DESC order by incident count. I further applied a LIMIT to restrict the output to 5 years. The results indicate that the years with the most incidents are 2021, 2022, 2019, 2018 and 2020.

2.	WHAT WEAPON TYPES ACCOUNT FOR THE MOST FATALITIES?

This encompassed 2 tables namely, victim and weapon. The query therefore referenced the incident id to execute a LEFT JOIN. I used the COUNT function to count the number of injuries which I filtered down to Fatal using the WHERE statement. I further grouped by weapon and ordered by fatality count in DESC. Lastly I applied a LIMIT OF 7 since the weapons type were 7. From the chart above, the weapons that account for the highest fatalities are Handguns, shotguns and rifles

3.	HOW DOES SHOOTERS RACE COMPARE TO VICTIM’S RACE FOR THE DIFFERENT STATES WITH THE HIGHEST INCIDENT COUNTS?

In this case, I had to compare data from 3 tables, incident, shooter and victim. As has been the case, my query used the incident id to execute a left join. The results returned many unknown race in both shooters and victims race columns so I utilized the WHERE statement to filter them out. Subsequently I grouped by state, shooters race and victims race then ordered by incident count in DESC to identity states with the highest incidents. Lastly, I applied a LIMIT to retrieve only the 10 highest incidents. The results indicate that in all states except CA where it was white on black, the shooters and victims belonged to the same race.

4.	WHICH RACE IS RESPONSIBLE FOR THE MOST SHOOTINGS AND WHAT IS THAT ATTRIBUTED TO?


To retrieve this information, I had to compare data from the, incident and shooter tables. My query used the incident id to execute a LEFT JOIN. To establish the most shootings, I used the COUNT function. Subsequently, I used the COUNTIF function to count the occurrences where the value is 1 or Yes. I further added the SAFE CAST function to convert string values to INT64 in the bullied, domestic violence, gang related and preplanned columns of the incident table. Lastly I used the WHERE statement to filter out null, unknown and N/A from the incident table columns. The results of the query indicate that blacks white and Hispanics are the races with the highest shooting incidents. If further indicates that for blacks and Hispanics, gang related is the major cause of shootings, while for whites its preplanned.

5.	WHAT IS THE AVERAGE SHOOTING FATALITY AND WHICH SCHOOLS HAVE HAD ABOVE AVERAGE FATALITIES?

The query retrieved data from the shooter table and victim table and incorporated three nested queries. 
Query1, involved first creating a table expression called ‘Top Schools’ and then establishing the fatality count using the COUNT function. I further applied a LEFT JOIN using the incident id to connect both tables and specified in the WHERE statement to filter out Fatal from injuries.
Query2 also required me to create a table expression titled ‘Average fatality’ followed by a calculation of average fatality count using the AVG function.
Query3, joined the Top Schools and Average fatality tables from query 1 and 2 using 1=1. In the absence of a unique value in both tables, this matches every row on table 1 with every row in table 2. Lastly I applied the WHERE function to filter fatality count greater than the average fatality. The results indicate that, sandy hook elementary school and Robb Elementary School are the only 2 schools with above average shootings

6.	FOR THE DIFFERENT CITIES, HOW MANY INCIDENTS WERE COMMITTED BY SHOOTERS WITH A CRIMINAL HISTORY VIS A VIS THOSE WITHOUT?

I examined the incident and shooter table and performed a LEFT JOIN using incident id in order to execute my query. Using the COUNT function, I established the number of shootings and grouped them by city and criminal history. I also applied the ORDER BY function to return results in DESC order. Finally, I applied a LIMIT of 15 to restrict the large output. For the 15 selected cities with the highest incident count, 8 had no criminal history while 7 shooters had a criminal history

