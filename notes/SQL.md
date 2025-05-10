# SQL Query Overzicht

Dit document bevat een verzameling van veelgebruikte SQL-query's met uitleg over wat ze doen. Handig als naslag bij het werken met relationele databases.

---

## Selecteert alle rijen en kolommen uit een tabel

```sql
SELECT * FROM table_name;
```

---

## Selecteert specifieke kolommen uit een tabel

```sql
SELECT id, title, release_date
FROM movies;
```

---

## Filtert rijen op basis van een voorwaarde

```sql
SELECT * FROM movies WHERE popularity > 50;
```

---

## Filtert op een jaartal en sorteert resultaten op populariteit (aflopend)

```sql
SELECT popularity, title
FROM movies
WHERE release_date LIKE '%2004%'
ORDER BY movies.popularity DESC;
```

---

## Haalt de hoogste waarde op uit een kolom

```sql
SELECT MAX(vote_average) FROM movies;
```

---

## Groepeert records en telt hoeveel er per taal zijn

```sql
SELECT original_language, COUNT(original_language)
FROM movies
GROUP BY original_language;
```

---

## Telt het totaal aantal films in de tabel

```sql
SELECT COUNT(*) FROM movies;
```

---

## Berekent het gemiddelde van de kolom vote_average

```sql
SELECT AVG(vote_average)
FROM movies;
```

---

## Formatteert de release_date als DD/MM/YYYY voor film met id 13

```sql
SELECT DATE_FORMAT(release_date, '%d/%m/%Y') AS `DD/MM/YYYY`
FROM movies
WHERE id = 13;
```

---

## Geeft een lijst van unieke talen waarin films zijn uitgebracht

```sql
SELECT original_language
FROM movies
GROUP BY original_language;
```

---

## Som van een kolom

```sql
SELECT SUM(popularity) FROM movies;
```

---

## INNER JOIN

```sql
SELECT movies.title, actors.name FROM movies INNER JOIN actors ON movies.id = actors.movie_id WHERE movies.id < 6;
```
