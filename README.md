# Mock-SQL-3   


1: Market-Analysis- II 


Write a solution to find for each user whether the brand of the second item (by date) they sold is their favorite brand. If a user sold less than two items, report the answer for that user as no. It is guaranteed that no seller sells more than one item in a day.

Return the result table in any order.
--------------------------------------------------------------------------------------------------------


SELECT user_id
FROM Users
WHERE user_id IN (SELECT DISTINCT user_id FROM Orders)
AND join_date BETWEEN '2019-01-01' AND '2019-12-31';





--------------------------------------------------------------------------------------------------------

2:  Tournament Winners 

The winner in each group is the player who scored the maximum total points within the group. In the case of a tie, the lowest player_id wins.

Write a solution to find the winner in each group.

Return the result table in any order.





--------------------------------------------------------------------------------------------------------

SELECT winner FROM Matches
GROUP BY winner
HAVING COUNT(*) >= ALL(SELECT COUNT(*) FROM Matches GROUP BY winner);






--------------------------------------------------------------------------------------------------------
