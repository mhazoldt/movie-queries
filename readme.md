SELECT * FROM movies.movies;

SELECT movieid, title FROM movies.movies LIMIT 10;

SELECT * FROM movies.movies WHERE movieid = 485;

SELECT movieid FROM movies.movies WHERE title = 'Made in America (1993)';

SELECT * FROM movies.movies ORDER BY title LIMIT 10;

SELECT * FROM movies.movies WHERE title LIKE '%2002%';

SELECT * FROM movies.movies WHERE genres LIKE '%Comedy%';

SELECT SUBSTRING_INDEX(SUBSTRING_INDEX(title, '(', -1), ')', 1) AS year_released, title FROM movies.movies WHERE title LIKE '%GodFather%' LIMIT 1;

SELECT SUBSTRING_INDEX(SUBSTRING_INDEX(title, '(', -1), ')', 1) AS year_released, title, genres FROM movies.movies WHERE genres LIKE '%Comedy%' AND SUBSTRING_INDEX(SUBSTRING_INDEX(title, '(', -1), ')', 1) = '2000';

SELECT * FROM movies.movies WHERE genres LIKE '%Comedy%' AND genres LIKE '%Horror%';

SELECT SUBSTRING_INDEX(SUBSTRING_INDEX(title, '(', -1), ')', 1) AS year_released, title, genres FROM movies.movies WHERE title LIKE '%super%' AND (SUBSTRING_INDEX(SUBSTRING_INDEX(title, '(', -1), ')', 1) = '2001' OR SUBSTRING_INDEX(SUBSTRING_INDEX(title, '(', -1), ')', 1) = '2002');