# DraftFPL Database (RUGFPL2023)

Developed a comprehensive database capable of storing weekly player statistics sourced
from user-selected teams via the Fantasy Premier League API
- Leveraged Pandas to extract, transform and load player and statistics into a
PostgreSQL database, ensuring data integrity and efficiency.
___
An advantage of having stored this database in SQL, is because of its connection
to Tableau. For each year, I intend to keep this database running for each year we play
so that we have a historical record of standings /players. Having this database is also handy
since at the end of the year i would like to make an infographic of the whole league - highlighting
top performers, who got fleeced in a trade ,etc. But for now (GW 25 out of GW 38), I have made a visualization that 
shows the points distribution of each team grouped by position.

![image](https://github.com/amboym/DraftFPLDB/assets/162647158/cf636c3c-7c87-431b-905a-67d3adf52f54)
