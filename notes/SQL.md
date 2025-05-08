# SQL Query Overzicht

Dit document bevat een verzameling van veelgebruikte SQL-query's met uitleg over wat ze doen. Handig als naslag bij het werken met relationele databases.

---

# Selecteert alle rijen en kolommen uit een tabel

SELECT \* FROM table_name;

# Selecteert specifieke kolommen uit een tabel

SELECT id, title, release_date
FROM movies;

# Filtert rijen op basis van een voorwaarde

SELECT \* FROM movies WHERE popularity > 50;

# Filtert op een jaartal en sorteert resultaten op populariteit (aflopend)

SELECT popularity, title
FROM movies
WHERE release_date LIKE '%2004%'  
ORDER BY movies.popularity DESC;

# Haalt de hoogste waarde op uit een kolom

SELECT MAX(vote_average) FROM movies;

# Groepeert records en telt hoeveel er per taal zijn

SELECT original_language, COUNT(original_language)
FROM movies
GROUP BY original_language;

# Telt het totaal aantal films in de tabel

SELECT COUNT(\*) FROM movies;

# Berekent het gemiddelde van de kolom vote_average

SELECT AVG(vote_average)
FROM movies;

# Formatteert de release_date als DD/MM/YYYY voor film met id 13

SELECT DATE_FORMAT(release_date, '%d/%m/%Y') AS `DD/MM/YYYY`
FROM movies
WHERE id = 13;

# Geeft een lijst van unieke talen waarin films zijn uitgebracht

SELECT original_language
FROM movies
GROUP BY original_language;
