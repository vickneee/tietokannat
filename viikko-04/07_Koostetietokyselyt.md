# Koostetietokyselyt

### Tehtävä 1

Kuinka korkealla sijaitsee korkeimmalla sijaitseva lentokenttä?
```sql
SELECT MAX(elevation_ft)
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
