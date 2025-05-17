# SQL Query Overzicht

Dit document bevat een verzameling van veelgebruikte SQL-query's met uitleg over wat ze doen. Handig als naslag bij het werken met relationele databases.

---

# Waar staat CRUD voor?

```sql
CREATE READ UPDATE DELETE
```

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

## JOIN

```sql
SELECT movies.title, actors.name FROM movies JOIN actors ON movies.id = actors.movie_id WHERE movies.id < 6;
```

---

## Datum formatteren naar dd/mm/jjjj

```sql
SELECT n_voornaam AS voornaam, Date_Format(N_gebdatum, "%d-%m-%y") AS Datum FROM namen;
```

---

## BTW uitrekenen doormiddel van een berekening

```sql
SELECT (a_kosten / 1.21) AS  kosten Excl BTW FROM activiteiten;
```

---

## Het gemiddelde uitrekenen AVG functie

```sql
SELECT AVG(a_kosten) FROM activiteiten;
```

---

## Huidige tijd aangeven

```sql
SELECT NOW();
```

```sql
SELECT CURDATE(), CURTIME();
```

```sql
SELECT CURRENT_DATE(), CURRENT_TIME();
```

---

# Verschil in datum aangeven

```sql
SELECT DATEDIFF(now(), "2007-04-01");
```

```sql
SELECT YEAR(CURRENT_DATE) - YEAR("2007-04-01");
```

---

## De INSERT INTO statement wordt gebruikt om nieuwe records(rijen) in te voegen in een tabel

```sql
INSERT INTO activiteiten (a_naam, a_dag, a_kosten) VALUES("Zwemschool Kikkerles", "di", 42.00)
```

---

## Data wijzigen

```sql
UPDATE activiteiten SET a_dag = "wo", a_kosten 29,99 WHERE a_naam = "scouting vereneging hallo";
```

---

## Een record oftwel rij verwijderen

```sql
DELETE FROM namen WHERE n_voornaam = "Esther" AND n_achternaam = "Gerards;
```

```sql
DELETE FROM namen WHERE n_nr = 2;
```

---

## Alle records binnen een tabel verwijderen zonde de tabel te verwijderen

```sql
DELETE FROM table_name;
```

```sql
DELETE FROM producten;
```

---

## Met een DROP TABLE statement verwijderen je een tabel

```sql
DROP TABLE producten;
```
