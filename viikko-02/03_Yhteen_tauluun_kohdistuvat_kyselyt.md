# Yhteen tauluun kohdistuvat kyselyt

### Tehtävä 1

Tee kysely, joka tulostaa kaikki sarakkeet goal-talusta.
```sql
SELECT * FROM goal;
```
![Screenshot1](Screenshot1.png)

### Tehtävä 2
Tee kysely, joka tulostaa nimen ja tyypin kaikista Suomessa sijaitsevista lentokentistä. Suomen maatunnus on: FI.
```sql
SELECT name, type FROM airport WHERE country = 'FI';
```
<img src="Screenshot2.png" width="350" height="400" alt="">

### Tehtävä 3
Tee kysely, joka tulostaa suomalaisten lentokenttien nimet aakkosjärjestyksessä. Suomen maatunnus: FI
```sql
SELECT name FROM airport WHERE country = 'FI' ORDER BY name;
```
![Screenshot3](Screenshot3.png) 
