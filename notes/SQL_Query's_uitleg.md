# SQL Query Overzicht

Dit document bevat een verzameling van veelgebruikte SQL-query's en commando's, met korte uitleg over wat elke query doet. Deze queries helpen bij het ophalen, filteren, groeperen en sorteren van data uit een database.

### Veelgebruikte SQL Query's:

- **SELECT \* FROM table_name:** Haalt alle records op uit de opgegeven tabel.
- **SELECT id, title, release_date FROM movies:** Haalt alleen de specifieke velden (`id`, `title`, `release_date`) uit de tabel `movies`.
- **WHERE:** Gebruikt om data te filteren op basis van een voorwaarde (bijv. `popularity > 50`).
- **ORDER BY:** Sorteert de resultaten op een bepaalde kolom in oplopende (`ASC`) of aflopende volgorde (`DESC`).
- **MAX():** Haalt de maximale waarde van een bepaalde kolom op (bijv. hoogste `vote_average`).
- **COUNT():** Telt het aantal records in een tabel of de hoeveelheid bepaalde waarden.
- **GROUP BY:** Groepeert de resultaten op basis van een kolom en voert aggregatieoperaties uit zoals `COUNT()`.
