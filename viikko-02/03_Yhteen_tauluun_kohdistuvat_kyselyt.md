# Yhteen tauluun kohdistuvat kyselyt

### Tehtävä 1

Tee kysely, joka tulostaa kaikki sarakkeet goal-talusta.
```sql
SELECT * 
FROM goal;
```
![Screenshot3_1](Screenshot3_1.png)

### Tehtävä 2

Tee kysely, joka tulostaa nimen ja tyypin kaikista Suomessa sijaitsevista lentokentistä. Suomen maatunnus on: FI.
```sql
SELECT name, type 
FROM airport 
WHERE iso_country = 'FI';
```
![Screenshot3_2](Screenshot3_2.png)

### Tehtävä 3

Tee kysely, joka tulostaa suomalaisten lentokenttien nimet aakkosjärjestyksessä. Suomen maatunnus: FI.
```sql
SELECT name 
FROM airport 
WHERE iso_country = 'FI' ORDER BY name;
```
![Screenshot3_3](Screenshot3_3.png)

### Tehtävä 4

Tee kysely, joka tulostaa nimen ja tyypin kaikista Suomessa sijaitsevista lentokentistä. Järjestä tulos ensisijaisesti tyypin mukaan ja toissijaisesti nimen mukaan.
```sql
SELECT name, type 
FROM airport 
WHERE iso_country = 'FI' ORDER BY type, name;
```
![Screenshot3_4](Screenshot3_4.png)

### Tehtävä 5

Tee kysely, joka tulostaa kaikki F-kirjaimella alkavat maan nimet country-taulusta.
```sql
SELECT name 
FROM country 
WHERE name LIKE 'F%';
```
![Screenshot3_5](Screenshot3_5.png)

### Tehtävä 6

Tee kysely, joka tulostaa kaikki country-taulun maiden nimet, joissa esiintyy F-kirjain.

```sql
SELECT name 
FROM country 
WHERE name LIKE '%F%';
```
![Screenshot3_6](Screenshot3_6.png)

### Tehtävä 7

Missä locationissa Vesa sijaitsee?
```sql
SELECT location 
FROM game 
WHERE screen_name = 'Vesa';
```
![Screenshot3_7](Screenshot3_7.png)

### Tehtävä 8

Kuinkan paljon Ilkka on kuluttanut CO2 budjettia?
```sql
SELECT co2_consumed 
FROM game 
WHERE screen_name = 'Ilkka';
```
![Screenshot3_8](Screenshot3_8.png)

### Tehtävä 9

Kuinka paljon alkuperäinen CO2 budjetti on (tulosta CO2 budjetin arvo vain kerran)?
```sql
SELECT DISTINCT co2_budget 
FROM game;
```
![Screenshot3_9](Screenshot3_9.png)
