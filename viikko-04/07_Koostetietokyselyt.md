# Koostetietokyselyt

### Tehtävä 1

Kuinka korkealla sijaitsee korkeimmalla sijaitseva lentokenttä?
```sql
SELECT max(elevation_ft)
FROM airport;
```
![Screenshot7_1](Screenshot7_1.png)

### Tehtävä 2

Tee kysely, joka listaa kunkin maanosan, ja niissä sijaitsevien maiden määrän.
```sql
SELECT continent, count(*)
FROM country
GROUP BY continent;
```
![Screenshot7_2](Screenshot7_2.png)

### Tehtävä 3

Tulosta pelaajien nimimerkit ja pelaajien saavuttamien säätilatavoitteiden lukumäärät.
```sql
SELECT screen_name, count(*)
FROM game
JOIN goal_reached ON game.id = goal_reached.game_id
GROUP BY screen_name;
```
![Screenshot7_3](Screenshot7_3.png)

### Tehtävä 4

Mikä nimimerkki on kuluttanut vähiten hiilijalanjälkeä?

Vihje2: Vaikka kysely kohdistuu yhteen tauluun tarvitset sisäkyselyä.
```sql
SELECT screen_name
FROM game
WHERE co2_consumed in(
    SELECT min(co2_consumed)
    FROM game
);
```
![Screenshot7_4](Screenshot7_4.png)

### Tehtävä 5

Tulosta maan nimi ja lentokenttien lukumäärä kyseisessä maassa. Järjestä tulokset siten, että ylimpänä listassa ovat maat, joissa on eniten lentokenttiä. Ota mukaan vain 50 eniten lentokenttiä sisältävää maata.
```sql
SELECT country.name, count(*)
FROM airport, country
WHERE airport.iso_country = country.iso_country
GROUP BY country.iso_country
ORDER BY count(*) DESC
LIMIT 50;
```
![Screenshot7_5](Screenshot7_5.png)

### Tehtävä 6
