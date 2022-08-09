-- Request #1

-- Events that include the word "toastmaster"

SELECT 
    event_name tm_events
FROM
    event
WHERE
    event_name LIKE ('%toastmaster%');
 
 -- The total number of Toastmasters events on LetsMeet
 
SELECT 
    COUNT(event_name) tm_events
FROM
    event
WHERE
    event_name LIKE ('%toastmaster%');


-- Toastmaster events alongside cities in which they are hosted 

SELECT 
    event_name tm_events, city
FROM
    event
        JOIN
    grp ON event.group_id = grp.group_id
        JOIN
    city ON grp.city_id = city.city_id
WHERE
    event_name LIKE ('%toastmaster%'); 

-- Exact counts for how particular cities host toastmasters events 

SELECT 
    COUNT(event_name) tm_events, city
FROM
    event
        JOIN
    grp ON event.group_id = grp.group_id
        JOIN
    city ON grp.city_id = city.city_id
WHERE
    event_name LIKE ('%toastmaster%')
GROUP BY city;
