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