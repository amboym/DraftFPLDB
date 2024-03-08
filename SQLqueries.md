### Unique Players 

SELECT 
	COUNT(DISTINCT name) AS unique_players
from fpl23

## Output 
![image](https://github.com/amboym/DraftFPLDB/assets/162647158/a14b46f8-c3ba-4c5f-bf59-091005e6ba4c)


### Top 5 xG's - in each position
- One of footballs indicator for good form is xG, It provides a numerical value representing the likelihood of a particular shot resulting in a goal based on various factors such as shot location, angle, distance from the goal.

SELECT 
    name,
    position_y,
    SUM(goals_scored) AS total_goals_scored,
    SUM(expected_goals) AS total_expected_goals
FROM 
    fpl23
GROUP BY 
    name, position_y
ORDER BY 
    total_expected_goals DESC
LIMIT 10;




![image](https://github.com/amboym/DraftFPLDB/assets/162647158/6348b398-4e4a-4d6c-9013-78aeeab90beb)


### Which owner has the most players with yellow cards?

SELECT
    owner,
    SUM(CASE WHEN yellow_cards > 0 THEN 1 ELSE 0 END) AS total_yellow_cards
FROM
    fpl23
GROUP BY
    owner
ORDER BY
    total_yellow_cards DESC;

![image](https://github.com/amboym/DraftFPLDB/assets/162647158/ef4ea700-ecc2-4ce7-97fd-e7cc9b633fc2)


